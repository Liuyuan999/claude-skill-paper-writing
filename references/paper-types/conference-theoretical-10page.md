# Playbook: ~10-Page Theoretical Conference Paper

**Target venues:** NeurIPS, ICML, ICLR, AISTATS, COLT.
**Length:** ~9–10 pages main text (venue-dependent), references and appendix excluded or
separate. Two-column (some single). Hard limit — be ruthless.

Combine with: `general-principles.md`, `house-style.md`, `theory-writing.md`,
`abstract-and-intro.md`, `experiments.md`, `checklists.md`.

---

## The budget problem

The main text is a *trailer*, not the full movie: the proofs live in the appendix. The 10
pages must (1) deliver the one idea, (2) state the headline theorem, (3) give a convincing
proof sketch, and (4) show experiments that corroborate the theory. Everything else moves to
the appendix.

## Section skeleton (suggested page budget, two-column)

1. **Abstract** (4-move arc). [—]
2. **Introduction** (~1–1.5 pp) — paradigm + application litany, Eq. (1), two-camp prior
   art, italicized research question + "affirmative", **§1.1 contributions (C1/C2/…)** with
   optional **T1/T2** challenges. **Figure 1** here. [~1.25 pp]
3. **Preliminaries / Problem formulation** (~0.75 pp) — notation, definitions, assumptions
   (full statements). [~0.75 pp]
4. **Method** — reformulation (e.g., penalty `F_γ`) + **Algorithm 1** (boxed). Get here by
   ~page 3. [~1.5 pp]
5. **Main results** — the **single headline theorem** (informal in body, formal in
   appendix), with a **proof sketch** naming the key lemmas and the main inequality. [~2 pp]
6. **Experiments** — synthetic-then-real; the plots/tables that corroborate the theory. [~2 pp]
7. **Related work** — thematic, "the diff", generous. Can be earlier if short. [~0.5 pp]
8. **Conclusion** (~0.25 pp).
9. **Appendix** (separate) — full proofs, auxiliary lemmas, extra experiments, hyperparams.

## Emphasize

- **One ping, one theorem.** Resist adding a second theorem; demote to lemma/appendix.
- **Proof sketch quality** — reviewers judge correctness from the sketch + spot-checks of
  the appendix. Make the key step legible.
- **Rate in big-O** in abstract, intro, and theorem.
- **Figure 1** carrying the idea; a **comparison table** vs. prior methods
  (single-loop / Hessian-free / rate / assumption, with "(ours)" row).
- Theory-before-experiments ordering.

## De-emphasize / move to appendix

- Full proofs, all constants, auxiliary lemmas.
- Extended experiments, full hyperparameter tables, additional datasets.
- Long background a competent reader already knows.

## Pitfalls

- Methods section starting after page 3 → restructure.
- Stating assumptions far from the theorem → restate them in/next to it.
- Overfull related work crowding out the idea → trim, make thematic, move later.
- A proof sketch that's just "see appendix" → give the actual key idea.
- More than one coined acronym or more than ~3 theorems → dilution.
- Forgetting the venue's mandatory checklist/reproducibility statement.
