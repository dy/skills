# Mechanical checks

The model that produced slop cannot see it on re-read — its preference tuning rates the
patterns as good writing. So verification runs on searches and counts, not impressions.
Grep hits are **leads, not verdicts**: every hit still gets triaged against the
exemptions. But a verification pass with zero mechanical checks is not a verification
pass.

## Hard artifacts — zero tolerance, 100% confidence

Literal string leaks from AI tool internals. Any occurrence is machine-generated text
pasted unread; delete the artifact and re-check the surrounding claims against sources.

```
oaicite            contentReference       attributableIndex
turn0search        turn1search            citeturn
grok_card          filecite               ::contentReference
```

```sh
grep -rEn 'oaicite|contentReference|attributableIndex|turn[0-9]search|citeturn|grok_card' .
```

## Regex catalog

Runnable as `grep -Ein '<pattern>' file`. Case-insensitive; triage every hit.

```sh
# Binary contrast + escape hatches
grep -Ein "not (just|only|merely|simply) .{3,60}(but|it's|it is)|isn't the problem|the answer isn't|less about .{3,40} than|the real .{3,30} is|the question isn't" $F

# Tier-1 vocabulary
grep -Ein "\b(delve|tapestry|testament|paradigm shift|leverag(e|ing)|synergy|myriad|plethora|beacon|multifaceted|game.chang|cutting.edge|ever.evolving|seamless)\b" $F

# Throat-clearing, filler, hedging
grep -Ein "here's the thing|it's worth noting|at the end of the day|in today's|let me be clear|it turns out|in order to|due to the fact" $F

# Decorative middle dots and dashes (em, en, double-hyphen as dash)
grep -En "·|—|–| -- " $F

# Bold mid-prose (outside headings) and label-bullets
grep -En "^[^#].*\*\*[^*]+\*\*" $F
grep -En "^\s*[-*] \*\*[^*]+:?\*\*" $F

# Emoji in headings
grep -En "^#{1,6} .*[\x{1F300}-\x{1FAFF}\x{2600}-\x{27BF}]" $F   # (PCRE: grep -P)

# Chatbot leakage
grep -Ein "hope this helps|would you like|let me know if|great question|you're absolutely right|certainly!" $F
```

## Statistical thresholds

Flags, not verdicts — human writing occasionally trips one; tripping several converges
on machine text.

Thresholds apply to **delivered prose**. Working documents (reference files, specs, agent
instructions, tables) are out of scope — see SKILL.md → Scope. Run these on the draft a
reader will read, not on the scaffolding around it.

| Signal | Threshold |
| --- | --- |
| Middle-dot separator (`·`) | never outside mathematics or an established house style |
| Em-dash (—) | never in delivered prose; use an en-dash (–) if a dash is warranted |
| En-dash budget | 0 in short copy (< ~150 words), ≤2 in a long piece |
| Sentence-length monotony | 3+ consecutive sentences within ±4 words of each other |
| Burstiness floor | no sentence under 8 or over 30 words in 500 words of prose |
| Hedge density | >8 hedges per 1000 words in declarative writing |
| Paragraph uniformity | all paragraphs within ±15% of the same length |
| Transition-opener density | >30% of paragraphs opening with a transition word |
| Rule-of-three density | `\b\w+, \w+, and \w+\b` firing more than ~1/300 words |

Sentence-length distribution in one line:

```sh
tr '.' '\n' < $F | awk 'NF{print NF}' | sort -n | uniq -c
```

Healthy prose shows a spread (4-word sentences and 30-word sentences); a hump centered
on 15–22 with no outliers is a tell.

## The verification loop

1. Rewrite complete → run the regex catalog and threshold checks **on your own
   output**.
2. Every hit that survives triage is a new finding. Fix by meaning (see
   [structures.md](structures.md) — escape-hatch paraphrases count as hits).
3. Loop. **Cap at 3 passes.** If a passage still fires on pass 3, stop patching it:
   extract the bare claim the passage exists to make, and rewrite it from scratch as
   plain declarative sentences in the author's voice.
4. Never conclude "this reads human now" from impression. The loop ends when the
   mechanical scan is clean or every remaining hit has a named exemption.

## Optional score

When the user wants a number (self-assessment only — never as an "AI detector" verdict
on third-party text): five dimensions × 10.

| Dimension | 10 looks like |
| --- | --- |
| Directness | claims land without setups, reversals, or hedging ceremony |
| Rhythm | length varies with content; no metronome, no forced staccato |
| Trust | no hand-holding, no recap, no reassurance; reader treated as smart |
| Authenticity | voice signals intact; opinions where the register allows them |
| Density | every sentence adds a fact, image, or step; nothing tautological |

Below 35/50: revise before delivering.
