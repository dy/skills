# skills

Agent skills by [@dy](https://github.com/dy). Work with any agent supported by the [skills CLI](https://skills.sh) (Claude Code, Cursor, Copilot, OpenCode, …).

```sh
npx skills add dy/skills --skill artbureau
npx skills add dy/skills --skill contemplate
npx skills add dy/skills --skill marketing
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

## marketing

High-converting marketing from the verified direct-response canon — offers, copy, positioning, persuasion, distribution. Grounded in evidence-verified masters (Schwartz, Caples, Hopkins, Ogilvy, Hormozi, Dunford, Berger, Cialdini), each framework audited for credibility — no guru hype.

## License

[Krishnized license](https://github.com/krishnized/license) — do everything as an offering.
