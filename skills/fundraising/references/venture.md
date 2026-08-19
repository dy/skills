# Venture — raising from investors

The deck is the most over-taught artifact in this field and the least decisive. Seven near-identical "10-slide framework" skills exist publicly; none of them will fix a raise. What decides a raise is whether an investor can verify a real signal, whether someone credible has already committed, and whether the market is big enough to return their fund. This file covers those.

## Understand the allocator before you pitch them

A VC's behavior is downstream of their own fund structure, not of your merit. Kupor's central point: with roughly 2% management fee, 20% carry, and a ten-year fund life, a fund needs outcomes that can return the *whole fund*. That single constraint explains most rejections that feel personal.

**The power law is the whole game.** The Horsley Bridge dataset of about 7,000 investments (1985–2014) found roughly 6% of deals produced 60% of returns. Correlation Ventures, across 21,000 and later 27,000 deals, found roughly 65% of venture investments return less than the capital put in, with the top 4% returning more than 10x. Consequences you should internalize:

- **A good business in a small market is a rational "no."** It cannot return the fund. This is not a judgment about quality and arguing quality won't move it.
- **Investors fear missing the winner as much as backing the loser.** Graham names this symmetry, and it's the mechanism behind every real (not performed) FOMO dynamic.
- **Individual "pattern-matching" claims deserve skepticism.** With returns this skewed, a single partner sees too few outlier draws in a career to distinguish skill from luck statistically. Weight the fund's structure over the partner's self-narrative.

One quantified process finding worth knowing: Wiltbank & Boeker's Kauffman-backed study of 3,097 angel investments found deals where the investor did **more than 20 hours of due diligence returned 5.9x** versus substantially less for lighter diligence. Investors who dig are not obstacles; they are the ones who make money and they will dig.

## The signal that actually moves money

**Traction, expressed as a growth rate rather than an absolute.** YC's guidance is to optimize the weekly rate; Graham's often-cited benchmark is roughly 5–7% per week pre-Series-A. Whether or not that exact figure fits your business, the principle holds: a small number growing fast beats a larger number that is flat, because the first is a slope and the second is a point.

**A committed lead.** See the SKILL.md physics section. CB Insights quantified the inverse: when a seed lead does *not* follow on, Series A odds fall to roughly 27%. The absence of a signal is itself a loud signal, which is why you should understand your existing investors' follow-on intentions *before* you open a round.

**Warm introductions.** Directionally much better than cold, but treat the circulating multipliers as folklore. The honest version: a warm intro transfers a small amount of someone's credibility and gets your material read, nothing more. It does not survive contact with weak numbers.

**What the deck data actually supports.** DocSend's platform data across a few hundred startups found decks reviewed for more than four minutes convert to meetings materially better, and that founders backed by a firm closed roughly twice the money in less time contacting far fewer investors. Real data, but from a vendor selling deck analytics, on a self-selecting population. Directionally right, not precise.

## The deck, briefly

Kawasaki's discipline still holds: roughly ten slides, twenty minutes, thirty-point type, and investors evaluate a large market, an unfair advantage, and a team that has done it before, in about that order. Everything else on a slide is decoration.

The one rule worth more than the template: **every number must be identical across the deck, the memo, the model, and the data room.** Inconsistent numbers are the fastest way to lose a diligence process, because they force the investor to distrust all your numbers, not just the wrong one.

**Do not build another deck from a generic template when a good reviewer exists.** For rubric-based deck critique, `OneWave-AI/claude-skills` (pitch-deck-reviewer) does structured scoring, objection prediction and benchmarking. For fundraise process management — Q&A prep, investor updates, week-by-week planning — `tjboudreaux/cc-skills-vc-fundraising` is small but well-sourced.

## Running the round

**Decide first whether to raise.** Graham's "default alive or default dead": does current growth reach profitability before the money runs out? A default-alive company raising is negotiating from strength; a default-dead company raising is negotiating against a clock the investor can see. Overhiring, often investor-encouraged, is what converts the first into the second.

**Two phases (Graham).** Phase one: collect soft commitments broadly, without over-negotiating terms, because your leverage is lowest and your information is worst. Phase two, once real momentum exists: become selective, close the lead, set terms. Founders who try to run phase two first stall, because selectivity without demand is just slowness.

**Sequence.** Lead first, then the round fills behind it. Do not announce a round you have not anchored.

**Scarcity.** A round genuinely has a size, and a closing date genuinely arrives. State those plainly. Performing urgency you do not have is a material misrepresentation, not a tactic.

## Terms literacy (enough to not get hurt)

Feld & Mendelson reduce term sheets to two axes, and reading them this way prevents most founder mistakes:

- **Economics** — valuation, liquidation preference (1x non-participating is the standard to hold for; participating preferred double-dips), option pool size and *whether it's carved out pre- or post-money* (a pre-money pool is a price cut disguised as a governance detail), anti-dilution.
- **Control** — board composition, protective provisions, drag-along, vesting including founder vesting.

Valuation is the number founders fixate on and control is the one that determines whether they still run the company in four years. **This is not legal advice.** A term sheet goes to a lawyer who does this for a living, always.

## The alternative you should actually consider

The entire canon above assumes venture is the goal. For most companies it should not be.

**Bootstrapping is a real strategy, not a consolation.** 37signals is the best-documented case: profitable since 1999, no outside board, publicly disclosed economics for years, and an explicit argument that growth-at-all-costs is a choice rather than a requirement of building software.

**Revenue-based and hybrid instruments exist but have not reached capital-markets scale.** Calm Company Fund and indie.vc built explicit alternatives to the growth-or-die model. Note the honest data point: when indie.vc tried to raise a fourth fund on that model, roughly 80% of its LP base declined to continue. That says nothing about whether the model served its founders well, and everything about institutional appetite for it. Both facts matter to a founder choosing a path.

## Watch out

- **The whole canon is survivorship bias.** Feld, Kupor, Calacanis, Kawasaki, Graham — all successful people describing what they did, with no control group of founders who did the same and failed. Every named rule here is a heuristic corroborated by repetition across independent practitioners, not a finding. Treat the famous origin stories (the cereal boxes) as contingent tactics retold as templates.
- **Pitch theater is now an industry.** An entire coaching layer optimizes founder *performance* independent of the underlying business. A pitch that works and a business that works are different targets, and only one of them survives diligence.
- **Raising is not an achievement.** It is taking on a permanent obligation and, usually, a board. The press cycle around funding announcements systematically obscures this.
- **Never invent a lead.** "We have strong interest from a top-tier fund" when you do not is the single most common founder lie and it is discoverable in one phone call between investors who talk to each other constantly.
