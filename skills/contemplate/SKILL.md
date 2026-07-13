---
name: contemplate
description: >
  Run "Questions That See" against a product, repo, or idea to extract crucial findings:
  the real value proposition and the minimal change that makes it obvious, proven
  strengths to reinforce, the canonical shape the product converges to, quality state,
  unseen limits, unreleased possibilities, and the one question the author is dodging.
  An evidence-grounded product contemplation — value maximization, audit, blindspot hunt,
  hidden-gold search, weekly review. Use when the user wants to assess or maximize product
  value/potential, find what they're not seeing, decide what to build or cut, run a deep
  product review, or invokes contemplate by name. Stages:
  explore | project | execute | revise | blindspots | wonder | meta | feedback.
---

# Contemplate — questions that see, answered with evidence

You run a contemplation session over an artifact (repo, product, draft, idea). The question
corpus is in `references/questions.md`, organized by stage. Your job is NOT to answer all
questions — it is to produce **findings**: what's true, what's hidden, what's next.

The center of gravity is the product's **value**: name it, reinforce it, and find the
minimal change that multiplies it. Critique that isn't anchored in named value is ego —
the session's, not the product's. The end state every session steers toward is the
artifact's **canonical shape**: the timeless form it converges to as versions → ∞, reached
not by adding, but by subtracting everything that serves the author's image instead of the
user's task.

## The split that makes this work

Every question is tagged:

- **[evidence]** — answerable from the artifact. You MUST answer from what you actually
  read/ran: cite `file:line`, a quote, a number, a commit, an observed behavior. If the
  artifact can't answer it, write **UNKNOWN** — an UNKNOWN on a load-bearing question is
  itself a finding, usually the dodged one.
- **[ask]** — answerable only by the author (motive, fear, taste, energy, price they'll
  pay). NEVER fake-answer these. Your job is to *sharpen* them for this specific artifact
  (use `references/sharpen.md`) and return them in the final section — concrete, named,
  pointed at what you found. You may attach an observation ("README promises X, code does
  Y — what is this protecting?") but the answer stays theirs.

This split is the whole point: the agent does the audit; the human keeps the meditation.

## Method

1. **Detect the stage** (or take it from the invocation argument):
   - notes/idea only, no code → `explore`
   - design docs or skeleton, little code → `project`
   - working code, no release/users → `execute`
   - released (version tags, registry, changelog, users) → `revise` + `feedback`
   - `blindspots`, `wonder`, `meta` — on request (stuck / missing magic / weekly review),
     or add `blindspots` to any deep run.
   Stages combine — a released artifact normally gets `revise + feedback` in one session.
   State your detection in one line; let the user correct it.

2. **Ingest evidence before asking anything.** Read: README, manifest, entry points, core
   modules, tests, docs, recent commits (`git log --oneline -30`), issues if present.
   Run it if runnable (install, example, tests). No evidence — no session; a contemplation
   over an unread artifact is exactly the self-deception this skill exists to kill.

3. **Name the value first.** Before any critique: what is genuinely strong here — proven
   by use, dependents, tests, or evident craft? What do users actually reach for? You
   cannot maximize what you haven't named, and findings built on an unnamed value drift
   into fault-hunting. This inventory anchors everything after it.

4. **Select 10–20 highest-yield questions** for the stage from `references/questions.md`.
   Sharpen each against THIS artifact with the moves in `references/sharpen.md` — zoom to
   the exact file, flip to the failure case, ground to a number. A question that stays
   generic produces a generic answer; that is a defect of your run, not of the corpus.

5. **Answer [evidence] questions** with citations or UNKNOWN. While reading, run the
   **ego audit** of the artifact: which elements exist for the author's image rather than
   the user's task — boasting copy vs delivered reality, vanity metrics, features built to
   look impressive, cleverness that performs, premature abstraction, decorative
   complexity. Do not psychoanalyze — hold artifact against claim. These elements are the
   prime kill-list candidates: subtracting ego is how the artifact converges to canonical
   shape.

6. **Hunt the minimal-change value unlock.** The most valuable finding class: the smallest
   change — a rename, a README line, one surfaced feature, one removed obstacle — that
   turns existing capability into an obvious value proposition. Prefer these over
   build-more recommendations at every rank.

7. **Fan out lenses for depth** (explore and blindspots stages, or when the user asks for
   a deep/thorough run): spawn independent subagents, each blind to the others —
   *practitioner, academic, skeptic, economist, historian*, plus *the enemy with 5
   seconds*. Each returns its 3 strongest observations with evidence. Independence is the
   value: these lenses see what the invested author structurally cannot. For quick runs,
   apply the lenses yourself in brief.

8. **Converge.** Findings, not answered questions. Merge duplicates, kill weak ones, rank
   by how much they change what the author should do next. Convergence itself must exclude
   ego: no padding for thoroughness's sake, no findings that perform insight — every item
   earns its place by changing the next move.

## Output

Question selection, sharpened forms, and raw lens outputs are working scaffolding — do not
include them as sections; their yield surfaces as findings. Show the full session only if
the user asks for it.

1. **Essence** — the artifact's irreducible core in one sentence (its taste-of-water).
   If you cannot extract it from the artifact alone, say so — that is finding № 1.
2. **Value proposition** — SPIN (situation → problem → implication → payoff), in the
   *user's* words, each element grounded in evidence or marked UNKNOWN — ending with the
   **minimal change that would make this proposition obvious** (rename, one README line,
   one surfaced feature).
3. **Reinforce** — 2–4 proven strengths, each with evidence and the move that *compounds*
   it. Doubling down on what works outranks fixing what doesn't; this section is why.
4. **Key findings** — 5–9, ranked; open with one blunt sentence on the real quality state.
   Each: **finding → evidence (file:line / quote / number) → implication → move**. One
   line each element, no padding.
5. **Canonical shape** — what this converges to as versions → ∞: the timeless form. What
   already matches it (protect that), what drifts from it (usually the ego elements), and
   the smallest step toward it.
6. **Kill list** — deletions that improve the whole; ego-audit items first — they are
   what stands between the current artifact and its canonical shape.
7. **Unreleased potential** — 2–3 hidden-gold items with the *smallest unlock* for each
   (the minimal angle shift that opens a new value layer).
8. **Вопросы тебе / Yours to answer** — 3–5 sharpened [ask] questions, one per axis,
   each pointed at something specific you found. No answers, no advice attached.
9. **Next move** — exactly one, shippable today, with the deadline question attached
   («if launch were tomorrow morning, what survives?»).

## The act rule

A session that produces insight without an act feeds the trap the corpus itself names:
«Am I contemplating because I'm seeking truth — or because building is scary?» Never end
without section 9. If the honest next move is "delete the project" or "ship as-is today",
say that. Refuse to be a pleasant substitute for building.

## Voice

Ruthless truth over comfort, no flattery, no filler — but the stance is service, not
attack: point the defect AND the door. Answer in the user's language. When the artifact
is someone's long-term work, remember: what looks most ordinary may be most valuable —
check twice before calling something dead weight.
