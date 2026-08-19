# skills

Agent skills by [@dy](https://github.com/dy). Work with any agent supported by the [skills CLI](https://skills.sh) (Claude Code, Cursor, Copilot, OpenCode, …).

```sh
npx skills add dy/skills --skill artbureau
npx skills add dy/skills --skill contemplate
npx skills add dy/skills --skill deslop
npx skills add dy/skills --skill fundraising
npx skills add dy/skills --skill marketing
npx skills add dy/skills --skill public-relations
```

English skills answer in English; `artbureau-ru` and `contemplate-ru` are full-Russian variants (отвечают по-русски).

## artbureau

Expert review of any text, interface, layout, typography, identity, or photograph — in the school of the two most influential Russian design practices.

Distilled from the complete published doctrine, ~3000 pages read in full:

- **Артемий Лебедев** — [Ководство](https://www.artlebedev.ru/kovodstvo/sections/) §0–191, studio philosophy and landmark works ([artlebedev.ru](https://www.artlebedev.ru))
- **Максим Ильяхов** — all 652 советы on text and инфостиль ([bureau.ru/soviet/ilyahov](https://bureau.ru/soviet/ilyahov/))
- **Илья Бирман** — all 698 советы on interface ([bureau.ru/soviet/ilyabirman](https://bureau.ru/soviet/ilyabirman/))
- **Артём Горбунов** — all 1225 советы on layout, typography, taste ([bureau.ru/soviet/ag](https://bureau.ru/soviet/ag/))
- **Сергей Колпаков и Паша Чикин** — all 235 советы on photography and icons ([bureau.ru/soviet/kolpakov-chikin](https://bureau.ru/soviet/kolpakov-chikin/))

Reviews land as verdict → defects (each with its fix) → what works → redo. Severity order: meaning > honesty > structure > convention > spacing > typography > polish. Russian variant: `artbureau-ru`.

All doctrine belongs to its authors — Art Lebedev Studio and Bureau Gorbunov. This skill is a transformative distillation with citations; read the originals, they are excellent.

## contemplate

Evidence-grounded product contemplation — runs [Questions That See](https://github.com/dy/contemplation) against a repo, product, or idea and returns crucial findings: essence, value proposition with the minimal change that makes it obvious, proven strengths to reinforce, the canonical shape the product converges to, kill list (ego-audit first), unreleased potential, and the one question you're dodging.

The split that makes it work: **[evidence]** questions are answered from the artifact itself (file:line citations or UNKNOWN — and a load-bearing UNKNOWN is itself a finding); **[ask]** questions — motive, fear, taste, price — are never fake-answered, only sharpened and returned to you. The agent does the audit; you keep the meditation. Stages: explore · project · execute · revise · blindspots · wonder · meta · feedback. Every session ends in one next move, shippable today — insight without an act is refused. Russian variant: `contemplate-ru`.

## deslop

Remove AI slop from prose and code — the merged canon of the field's most effective deslop/humanizer skills ([blader/humanizer](https://github.com/blader/humanizer), [stop-slop](https://github.com/hardikpandya/stop-slop), [fuck-slop](https://github.com/juliusbrussee/skills), [no-ai-slop](https://github.com/petergyang/no-ai-slop), [humanize-writing](https://github.com/jpeggdev/humanize-writing), [Rossmann's rules](https://github.com/realrossmanngroup/no_ai_slop_writing_rules), [story-deslop](https://github.com/worldwonderer/oh-story-claudecode), [cursor/deslop](https://github.com/cursor/plugins) and others), deduplicated into ~45 patterns and reworked around the ideas the field gets right but rarely combines:

- **You cannot see your own slop** — verification is a mechanical regex/threshold re-scan loop (≤3 passes), never the model grading its own output; escape-hatch paraphrases ("the real X is Y" for "not X but Y") count as new findings.
- **Voice first** — 3–5 voice signals captured and protected before anything is subtracted; a writing sample overrides every default.
- **Delete first, rewrite second** — within deletion ceilings; fake-profound kickers are deleted, never re-metaphored.
- **Never invent facts** — missing specificity becomes a visible `[ADD: which?]` placeholder, not a plausible fill.
- **Every rule carries its exemption** — stacked tells consolidate into one finding; overcorrection (fake typos, forced slang, scrubbed-beige prose) is treated as slop too.

Modes: edit (default) · detect (names patterns, quotes lines — refuses "AI likelihood" scores) · code (diff-scoped: comments a human wouldn't write, defensive bloat, `any`-casts, placeholder names). Eight-register guide (reddit ≠ docs ≠ LinkedIn). All doctrine belongs to its authors — this is a transformative merge with attribution.

## marketing

High-converting marketing from the verified direct-response canon — offers, copy, positioning, persuasion, content strategy, distribution. Grounded in evidence-verified masters (Schwartz, Caples, Hopkins, Ogilvy, Hormozi, Dunford, Berger, Cialdini, Bernays), each framework audited for credibility — no guru hype.

Two things it does that most marketing advice doesn't. It decides **what a page should say** before how to say it — a repertoire of content blocks chosen by the objection each one retires (who this is NOT for, the cost of inaction, "why pay if I can do it myself", the ladder from attribute to value), fed by customer-verbatim harvesting and a systematic angle engine instead of a blank page. And it **grades its own advice**: every common tactic carries a verdict traced to primary sources, so specificity, two-sided messaging, benign-envy comparison and comparative ads are marked supported, while fake countdown timers, the odd-number headline rule, the "give 2 of 3 and they persuade themselves" move, and "video lifts conversion 80%" are marked folklore, legally risky, or fabricated — each with the trace back to where the number was invented.

## fundraising

Raise money — from investors or from donors — by building the conditions where capital wants to come to you, then running the ask as a disciplined process. Covers both branches, which share a spine and almost nothing else: startup/venture, and nonprofit/philanthropy.

The governing finding is Panas's: donors who gave a million dollars or more already believed before anyone asked. **The ask converts belief; it does not create it.** So the ideal raise has no pitch, and the work is upstream. The best-evidenced lever in the whole field says the same thing structurally — List & Lucking-Reiley's field experiment on a real capital campaign found that announcing a larger share of the goal already committed raised both participation and total dollars *more than linearly*, which is the quiet phase and the lead investor as one mechanism, independently evidenced in each branch. Field experiments outrank folklore throughout: a matching gift works but a bigger match ratio buys nothing (Karlan & List), overhead aversion is fixed by having a lead donor underwrite overhead rather than by cutting it (Gneezy et al., *Science*), peer anchors work but only aspirational-and-reachable ones on the undecided middle (Shang & Croson; Frey & Meier), and the identifiable-victim principle behind "show one face, not statistics" failed to replicate. Roughly four out of five first-time donors never give again, so retention outranks acquisition almost always. Manufactured inevitability — fake oversubscription, an uncommitted "lead", undocumented impact — is fraud, and the mechanisms only work because the signals are costly and true.

## public-relations

Earn third-party credibility, and protect reputation when it is under attack. Advertising is you talking about yourself; PR is arranging for someone else to, which is why every shortcut that fakes the third party destroys what it was trying to produce.

Built to the gap: organizational **crisis communications** had no agent skill at all — what exists under that name is the inverse, newsroom protocols for covering someone else's crisis. The spine is Ma & Zhan's meta-analysis: what you are blamed for correlates with reputation at r = −.54, what you say about it at r = .23. **Conduct outranks messaging roughly two to one**, which is the least flattering and most useful finding in the field. Apology, sympathy and compensation test as statistically indistinguishable (Coombs & Holladay), so the meeting-consuming "do we apologize" fight is a false dilemma; disclosing before you're discovered measurably beats being caught; and crises are diagnosed by attributed responsibility (Coombs' SCCT) before any strategy is chosen. Also covers how coverage actually happens — the Cardiff churnalism data, what journalist surveys say they want (under 200 words, before noon, beat-relevant), exclusive versus embargo, newsjacking and its failure mode — plus honest measurement, since AVE is formally discredited. The exposé canon is included as the reason the ethics line exists, not as a playbook. For tactical B2B journalist pitching, it points at `coreyhaines31/marketingskills` rather than rebuilding it.

## License

[Krishnized license](https://github.com/krishnized/license) — do everything as an offering.
