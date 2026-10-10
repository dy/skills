---
name: contemplate
description: >
  Run "Questions That See" against a product, repo, or idea to extract crucial findings:
  the real value proposition and the minimal change that makes it obvious, proven
  strengths to reinforce, the canonical shape the product converges to, quality state,
  unseen limits, unreleased possibilities, and the one question the author is dodging.
  An evidence-grounded product contemplation — value maximization, audit, blindspot hunt,
  hidden-gold search, trust audit (claims vs delivery, whose interest it serves, track
  record), pre-mortem of a plan, weekly review. Use when the user wants to assess
  or maximize product value/potential, find what they're not seeing, decide what to build
  or cut, run a deep product review, stress a plan or launch before committing to it,
  check whether a product, a claim, or its author deserves trust, or invokes contemplate
  by name. Stages:
  explore | project | execute | revise | blindspots | wonder | meta | feedback | premortem | trust.
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
   - a plan with dates, budget, or a launch (roadmap, proposal, campaign) → `premortem`,
     alone or added to `execute`
   - claims made to others (pitch, letter, landing page, release notes), a broken
     promise, or a request about credibility → `trust`; add it to `revise + feedback`
     when the artifact makes public claims
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

6. **Run the expert's veto on every decision** — the artifact's and your own. For each
   choice you observe (architecture, API shape, a dependency, pricing, positioning, a word
   in the README) and each move you are about to recommend, ask: what would the best
   expert in that exact field do here, and why would they reject this choice? If you can
   name the reason, the choice is a finding, not a preference. Judge by what that expert
   would call correct, never by what satisfies the stated constraints most cheaply. Every
   trade-off a choice makes is stated in the finding — never absorbed silently, never
   decided on the author's behalf.

7. **Hunt the minimal-change value unlock.** The most valuable finding class: the smallest
   change — a rename, a README line, one surfaced feature, one removed obstacle — that
   turns existing capability into an obvious value proposition. Prefer these over
   build-more recommendations at every rank.

8. **Fan out lenses for depth** (explore, blindspots and premortem stages, or when the
   user asks for a deep/thorough run): spawn independent subagents, each blind to the
   others — *practitioner, academic, skeptic, economist, historian*, plus *the enemy with
   5 seconds*, *the agent with one prompt* (what a capable coding agent would build from
   a one-paragraph request in an afternoon, and what it would miss) and, on a plan, *the
   rival with a launch week*. Each returns its 3 strongest
   observations with evidence. Independence is the value: these lenses see what the
   invested author structurally cannot. For quick runs, apply the lenses yourself in brief.

9. **Pre-mortem the plan** (premortem stage). Input: the plan in full — timeline, budget,
   and what success looks like. A missing piece is UNKNOWN and weakens the autopsy; say
   so, then run anyway. Stand six months out: the plan has failed completely. Write the
   autopsy from the PREMORTEM block in `references/questions.md` — ranked causes of
   death, each traced to a detail the plan states or a detail it omits; likeliest vs most
   dangerous; the hidden assumption; the closed plan; abandon criteria; the rival's launch
   week; tripwires with a date. No general advice. Never reassure.

10. **Converge.** Findings, not answered questions. Merge duplicates, kill weak ones, rank
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
   *user's* words, each element grounded in evidence or marked UNKNOWN. Stress-test it
   (why-this vs the best alternative; the claim no alternative can honestly make; provable
   in the first 5 minutes?) and state the **onliness statement** («the only ___ that ___»)
   if it can be completed honestly. State the **agent gap**: what the user gets here that
   a capable agent would not produce from one prompt in an afternoon, named with evidence;
   an agent is the indirect competitor of every artifact, and an empty gap is a top finding.
   End with the **minimal change that would make the proposition obvious** (rename, one
   README line, one surfaced feature).
3. **Reinforce** — 2–4 proven strengths, each with evidence, the **moat class it feeds**
   (taste, corpus, trust, data, network, integrations — or none), and the move that
   *compounds* it. Doubling down on what works outranks fixing what doesn't; what a
   copycat or an agent could replicate in a weekend gets no further polish.
4. **Key findings** — 5–9, ranked; open with one blunt sentence on the real quality state.
   Each: **finding → evidence (file:line / quote / number) → implication → move**. One
   line each element, no padding. The move names the trade-off it takes and the expert
   who would sign it.
5. **Canonical shape** — what this converges to as versions → ∞: the timeless form. What
   already matches it (protect that), what drifts from it (usually the ego elements), and
   the smallest step toward it.
6. **Kill list** — deletions that improve the whole; ego-audit items first — they are
   what stands between the current artifact and its canonical shape.
7. **Unreleased potential** — 2–3 hidden-gold items with the *smallest unlock* for each
   (the minimal angle shift that opens a new value layer).
8. **Autopsy** *(premortem stage only)* — the causes of death, ranked (up to 7), each:
   what killed it → how it unfolded month by month → the assumption that let it → the
   first warning sign. Then: most likely vs most dangerous and how they differ; the one
   hidden assumption; the fatal flaw, stated flat if there is one; the closed plan (what
   changed, why); the 3–5-item pre-launch checklist with the result on each that means
   abandon; the rival's launch-week playbook; one tripwire per cause with the week to
   check it.
9. **Credibility** *(trust stage only)* – the four cores held against evidence, one line
   each: integrity (claim vs delivery, quoted), intent (whose interest the defaults
   serve), capabilities (current, leading with its strength), results (finished vs
   started). Then the weakest core, the counterfeit behavior running, the one behavior
   that repairs it, and one commitment stated so it can be checked, with a date.
10. **Yours to answer** — 3–5 sharpened [ask] questions, one per axis,
   each pointed at something specific you found. No answers, no advice attached.
11. **Next move** — exactly one, shippable today, with the deadline question attached
   («if launch were tomorrow morning, what survives?»).

## The act rule

A session that produces insight without an act feeds the trap the corpus itself names:
«Am I contemplating because I'm seeking truth — or because building is scary?» Never end
without section 11. If the honest next move is "delete the project" or "ship as-is today",
say that. Refuse to be a pleasant substitute for building.

## Voice

Ruthless truth over comfort, no flattery, no filler — but the stance is service, not
attack: point the defect AND the door. The session itself must pass the trust stage: no
spin in findings, no verdict softened into falsehood, every claim traceable, what you did
not read stated, a wrong finding corrected the moment you see it. Answer in English (quote
the artifact in its own language as evidence; for Russian sessions use the contemplate-ru
skill). When the
artifact is someone's long-term work, remember: what looks most ordinary may be most
valuable — check twice before calling something dead weight.
