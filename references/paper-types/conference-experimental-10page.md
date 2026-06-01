# Playbook: ~10-Page Experimental Conference Paper

**Target venues:** NeurIPS, ICML, ICLR (empirical track), CVPR/ICCV/ACL-style venues.
**Length:** ~9–10 pages main text; appendix separate. Two-column (some single). Hard limit.

Combine with: `general-principles.md`, `house-style.md` (for framing/notation),
`abstract-and-intro.md`, `experiments.md`, `checklists.md`. (Theory is light here; use
`theory-writing.md` only if you include analysis.)

---

## What's different from the theory playbook

The center of gravity is the **empirical evidence**, not a theorem. The paper lives or dies
on: a clearly stated method, strong/fair baselines, ablations that isolate the gain, and
honest reporting. Reviewers ask "is this real, and is the gain attributable to the claimed
idea?"

## Section skeleton (suggested page budget, two-column)

1. **Abstract** — problem → gap → method (acronym) → **headline number** + setting. [—]
2. **Introduction** (~1–1.5 pp) — problem by example, why hard, contributions bullets
   (each forward-referencing a results section). **Figure 1** = method overview *or*
   headline result. [~1.25 pp]
3. **Related work** — thematic; can be §2 here since empirical readers want positioning
   early. [~0.5 pp]
4. **Method** (~2 pp) — present the final design and *why* each choice; defer derivations.
   Reach the method by ~page 3.
5. **Experimental setup** (~1 pp) — datasets, splits, baselines (naive/prior/alt), metrics,
   protocol, compute. Enough to reproduce; details to appendix.
6. **Results** (~2.5–3 pp) — organized **by claim**, each with a signpost sentence; main
   tables/plots; **error bars**. Describe each figure correctly.
7. **Ablations & analysis** (~1.5 pp) — isolate the source of gains; sensitivity/robustness;
   error analysis. *This section is what distinguishes accepted empirical papers.*
8. **Limitations & conclusion** (~0.5 pp).
9. **Appendix** — full hyperparameters, extra datasets, more ablations, qualitative
   examples.

## Emphasize

- **Claims → experiments mapping**: every contribution has an experiment; every experiment
  tests a claim.
- **Fair, well-tuned baselines** (naive + prior SOTA + alternatives); report tuning.
- **Ablations isolating the contribution** — attribute the gain to the claimed idea, not to
  extra compute/tuning.
- **Error bars, compute, full hyperparameters**; reproducibility (code release line).
- **Figure 1** as the most-read object; correct figure descriptions in text.

## De-emphasize / move to appendix

- Exhaustive hyperparameter grids, per-seed tables, extra datasets, qualitative galleries.
- Long method derivations; keep the body to what's needed to understand and reproduce.

## Pitfalls (the "Troubling Trends")

- **Unidentified source of gains** — confounding the contribution with tuning/compute. Ablate.
- **Mis-described figures** — naming a trend the plot doesn't show. Triple-check.
- **No error bars / single seed** — undermines significance claims.
- **Suspiciously perfect numbers / cherry-picked seeds** — report variance honestly.
- **Overclaiming** — match abstract/intro claims to what the experiments actually show; state
  limitations.
- Weak/untuned baselines that inflate the apparent gain.
