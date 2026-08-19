---
name: deslop
description: >-
  Remove AI slop from prose and code — the merged canon of the field's most
  effective deslop/humanizer skills (blader/humanizer, stop-slop, fuck-slop,
  no-ai-slop, humanize-writing, Rossmann's rules, story-deslop, cursor/deslop
  and others), deduplicated and reworked. Use when the user wants to deslop,
  humanize, de-AI, or naturalize text; remove AI patterns, tells, or "AI smell"
  from writing; check whether text reads as AI-generated; or clean AI slop from
  a code diff. For UI/design slop use the hallmark skill instead.
---

# Deslop

Slop is the absence of a decision — the statistically likeliest filler standing where a
choice should have been made. That is the test for every finding: *was this chosen?* The
same construction, picked deliberately in the author's voice, is not slop. The goal is
never "clean" text; it is text where every word survived a decision.

Two facts shape the method:

1. **You cannot see your own slop.** Slop patterns are artifacts of preference tuning,
   not vocabulary mistakes — the model that produces them rates them as good writing on
   re-read. Verification is therefore mechanical (re-scan with the checks in
   [references/checks.md](references/checks.md)), never impressionistic.
2. **Overcorrection is also slop.** Scrubbed-flat prose, fake typos, forced slang, and
   mechanical long/short sentence alternation are their own recognizable genre. Voice
   is protected before anything is subtracted.

## Scope

This skill governs **delivered prose** — text a reader consumes *as writing*: copy, posts,
essays, emails, marketing, narrative documentation, anything whose job is to be read.

It does not govern **working documents** — reference files, specs, agent and skill
instructions, changelogs, schemas, routing tables, navigation furniture. There a character
is doing structural work, not rhetorical work: a `·` separating two links in a table is not
an aside, and a dash setting off a column label is not a dramatic pause. Applying the
typographic rules there produces churn without a reader who benefits.

The test: *is this read as writing, or read to find something?* Only the first is in scope.
Everything below — the dash budget and middle-dot ban especially, since they are about a
reader's ear for machine prose — assumes the first. This skill's own reference files are
out of scope by that rule, and are written accordingly.

## Modes

| Mode | Trigger | What happens |
| --- | --- | --- |
| **Edit** (default) | text to deslop/humanize | Full process below; rewrite delivered with a short change note |
| **Detect** | "is this AI?", "find the tells" | Name patterns, quote the lines. Never output an "AI likelihood" score — named patterns are evidence, detectors are guesses. Do not edit. |
| **Code** | a diff or "deslop this code" | Code checklist below, diff-scoped |
| **UI** | pages, components, styling | Route to the `hallmark` skill — do not improvise UI rules here |

## Principles

1. **Protect voice first.** Before editing, list 3–5 voice signals to preserve
   (vocabulary level, cadence, bluntness, humor, uncertainty style, digressions,
   punctuation habits). A user-supplied writing sample overrides every default in this
   skill, including the dash budget. See [references/voice.md](references/voice.md).
2. **Delete first, rewrite second.** Most slop guards nothing — cut it. Rewrite only
   what carries meaning. Cap total deletion at ~25% of the piece; past that you are
   gutting content, not removing slop.
3. **Rewrite by meaning, never by paraphrasing the pattern.** Ask what the sentence
   is *for*, then say that plainly. A paraphrase that preserves the move ("the real X
   is Y" for "not X but Y") is a new finding, not a fix — the banned escape hatches
   are listed in [references/structures.md](references/structures.md).
4. **Fake-profound lines are deleted, not re-metaphored.** Replacing one purple kicker
   with a better metaphor reproduces the disease.
5. **Never invent facts.** Specificity comes from the source or from the author.
   Where a concrete detail is missing, leave `[ADD: which study? what year?]` — never
   a plausible-sounding fill. Before delivering, answer explicitly: *does the rewrite
   state any fact, name, number, date, or citation not present in the source?*
6. **One strong finding beats three weak ones.** Bold + scare quotes + a dash aside on
   the same phrase is one stacked tell, not three. Consolidate before reporting.
7. **Every rule carries its exemption.** House-style Title Case, genuine tricolons,
   term-definition bullets in docs, a single "however" — the exemption columns in the
   reference files are as binding as the rules.
8. **Match the register.** Reddit, academic, docs, and marketing have different fatal
   tells and different legitimate structures — check the register guide in
   [references/voice.md](references/voice.md) before flagging.

## Process (Edit mode)

1. **Read whole, capture voice.** Read the full piece once. Note register + audience.
   Write down the 3–5 protected voice signals.
2. **Scan.** Sweep against [references/patterns.md](references/patterns.md) (surface
   tells), [references/structures.md](references/structures.md) (structural moves), and
   the mechanical checks in [references/checks.md](references/checks.md). Collect
   findings with quotes.
3. **Triage.** Apply exemptions; consolidate stacked tells; drop anything that is a
   defensible authorial choice or a protected voice signal.
4. **Rewrite.** Delete-first. Per finding: what is this sentence for? Say that, in the
   author's voice. No escape-hatch paraphrases.
5. **Verify mechanically.** Re-run the scan against your own output. Any hit is a new
   finding. Loop at most 3 passes; if a passage still fires, rewrite it from the bare
   claim in plain declarative sentences.
6. **Fact check.** Answer the invented-facts question from Principle 5.
7. **Deliver.** Final text plus a change note of at most 8 lines, grouped by pattern.
   If the note needs more than 8 lines, you changed too much — reconsider.

## Quick checks (30 seconds, before delivering)

- Any middle-dot separator (`·`) or em-dash (—)? In delivered prose, never use either;
  both are top AI tells. Use normal punctuation or layout for lists and navigation. When
  a dash is genuinely warranted, make it an en-dash (–). Dash budget stays near 0 (≤2 in
  a long piece); never swap a dash for parentheses, restructure the sentence instead.
  (Voice sample overrides. Working documents are out of scope — see Scope.)
- Any "not X but Y" — or any of its escape-hatch paraphrases?
- Any inanimate noun performing a human action ("the data tells us")?
- Three items where two would do? Three sentences of the same length in a row?
- Any sentence that sounds like a pull-quote? Delete it.
- Opener that clears its throat ("Here's the thing")? Ending that recaps or reassures?
- Any bold mid-prose, emoji in headings, `**Label:** restatement` bullets?
- Any fact, number, or name the source doesn't contain?
- Would the author actually say this sentence out loud?

## Code mode

Scope: the diff (`git diff main` or this session's changes), not the whole repo. Keep
behavior unchanged; minimal focused edits; match the file's existing style. Remove:

- **Comments a human wouldn't write** — narrating the obvious, explaining the change
  to a reviewer ("// added to handle the new case"), restating the next line. Keep only
  comments stating what the code cannot: constraints, whys, workarounds.
- **Defensive bloat** — try/catch, null checks, and validation abnormal for that area,
  especially on trusted/already-validated codepaths; generic `except Exception` /
  empty catch blocks.
- **Type evasion** — `any` casts and assertions used to silence the checker instead of
  fixing the type.
- **Placeholder naming** — `data`, `result`, `temp`, `handleData`, `Manager`/`Helper`
  suffixes carrying no specificity.
- **Ceremony** — zero-information docstrings, single-use wrapper layers, speculative
  abstraction, dead code, debug leftovers, README boilerplate ("This project aims
  to..."), emoji in code or docs.
- **Any other style inconsistent with the file.**

Run the tests after. Report in 1–3 sentences.

## Credits

Merged and reworked from: [blader/humanizer](https://github.com/blader/humanizer)
(Siqi Chen; the Wikipedia "Signs of AI writing" lineage — also the root of the Zed,
Hermes, jpeggdev, softaworks, and humanizer-zh forks),
[hardikpandya/stop-slop](https://github.com/hardikpandya/stop-slop),
[juliusbrussee fuck-slop](https://github.com/juliusbrussee/skills),
[petergyang/no-ai-slop](https://github.com/petergyang/no-ai-slop),
[jpeggdev/humanize-writing](https://github.com/jpeggdev/humanize-writing),
[realrossmanngroup/no_ai_slop_writing_rules](https://github.com/realrossmanngroup/no_ai_slop_writing_rules),
[nousresearch/hermes-agent humanizer](https://github.com/nousresearch/hermes-agent),
[worldwonderer/oh-story-claudecode story-deslop](https://github.com/worldwonderer/oh-story-claudecode),
[cursor/plugins deslop](https://github.com/cursor/plugins), and
[brianlovin/agent-config deslop](https://github.com/brianlovin/agent-config).
All doctrine belongs to its authors; this is a transformative merge with attribution.
