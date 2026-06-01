# Playbook: Theoretical Journal Paper

**Target venues:** JMLR, Mathematical Programming, SIAM J. Optimization, IEEE Transactions
on Signal Processing, IEEE TPAMI, Foundations & Trends.
**Length:** no hard page limit; typically 25–60+ pages including full proofs. Single column.

Combine with: `general-principles.md`, `house-style.md`, `theory-writing.md`,
`abstract-and-intro.md`, `checklists.md`.

---

## What makes the journal version different from the conference version

- **Full proofs in the main body** (or clearly structured, but complete) — not banished to a
  terse appendix. Constants spelled out.
- **More complete results**: tighter rates, additional regimes, removed assumptions,
  extended experiments.
- **"Preliminary version" note**: if it extends a conference paper, add a footnote/section:
  *"A preliminary version of this work appeared at [conference, year]. This version adds
  [new theorem / removed assumption / new experiments]."* Be explicit about the delta.
- **Keywords line** after the abstract.
- **Self-contained**: a reader shouldn't need the conference paper.

## Section skeleton

1. **Abstract** (4-move arc) + **Keywords**.
2. **Introduction** — fuller than conference: paradigm + applications, formulation (Eq. 1),
   two-camp prior art, research questions, contributions (C1/C2/…), and a **detailed
   related-work** treatment can live here or in its own §2 (journals tolerate, even expect,
   a thorough related-work section).
3. **Preliminaries / Problem formulation** — notation, definitions, assumptions stated in
   full.
4. **Main results** — reformulation, algorithm(s), then theorems with **complete proofs**
   (or proof sketches in body + full proofs in a clearly labeled appendix section). Multiple
   regimes/corollaries are welcome here (unlike the conference one-theorem discipline).
5. **Discussion** — interpretation of rates, comparison table vs. prior bounds, when
   assumptions hold, limitations.
6. **Experiments** — synthetic first, then real; more extensive than the conference version.
7. **Conclusion** + future work.
8. **Appendices** — auxiliary lemmas, full proofs, extra experiments.

## Emphasize

- Completeness and rigor: every constant, every step.
- A **comparison-of-bounds table** (rates, assumptions, loop structure vs. prior work).
- Clear statement of the theoretical contribution over the conference version.

## De-emphasize / pitfalls

- Don't pad with the conference paper's compressed phrasing; expand and clarify.
- Avoid an unfocused sprawl — even at journal length, keep the one ping; structure many
  results around it.
- Don't let proofs become unreadable walls; use lemma decomposition and signposting.
- Reviewers are experts and thorough — loose constants or hand-waved steps will be caught.
