# Writing the Experiments / Results Section

For both experimental papers and the empirical section of theory papers. The goal is to
*convince a skeptic*, not to showcase.

---

## Framing: "what worked and why", not just "how well"

The strongest empirical sections answer:
- **What** is the claim this experiment tests? (one per experiment)
- **Why** does the method work — which component is responsible?
- **How well** — quantified, with uncertainty.

State the claim first, then the evidence. Each experiment should map to a contribution.

## Baselines

Compare against three kinds:
1. **Naive** baseline (the obvious thing / no-op) — shows the problem is non-trivial.
2. **Prior state of the art** — the methods you claim to beat or match.
3. **Alternatives / your own variants** — to isolate where the gain comes from.

Be fair: tune baselines as carefully as your method; report the tuning protocol.

## Ablations & analysis (this is what separates strong papers)

- **Ablations**: remove/replace each component to show it matters. One row per design
  choice.
- **Error analysis**: where and why does the method fail? Categorize failure modes.
- **Sensitivity / robustness**: vary hyperparameters, dataset, scale, seed. Show the method
  isn't brittle.
- **Identify the real source of gains** — don't let an unrelated change (more compute,
  better tuning) masquerade as the contribution.

## Reporting standards

- **Error bars / significance.** Report mean ± std (or CIs) over multiple seeds; state how
  many runs and whether the band is std or standard error. For close comparisons, a
  significance test.
- **Compute.** Hardware type, memory, per-run and total compute (including failed/
  preliminary runs).
- **Hyperparameters.** Full settings, search space, and *how* they were chosen (val split,
  not test). Put exhaustive tables in the appendix.
- **Reproducibility.** Release code/data with exact commands and environment; add the
  code-availability line.

## Ordering & presentation

- **Synthetic / toy problems first** (they isolate the mechanism and verify the theory),
  **then real benchmarks**. This is the group convention and reads well for theory papers.
- Group results by claim, each under a high-level signpost sentence.
- **Comparison table** (group style): rows = methods incl. a "**(ours)**" row; columns =
  properties (single-loop / Hessian-free / convergence / assumption) and/or metrics; ✓/✗ for
  qualitative properties, numbers (bold best) for quantitative.

## Figures & tables

- **Figure 1** carries the headline result or the method idea (see `abstract-and-intro.md`).
- Vector/PDF, fully labeled axes with units, legible in grayscale, legend not covering data.
- **Describe every graph correctly in the text** — name the exact lines/points that support
  the claim, and triple-check the trend you state matches the plot. Mis-describing a figure
  is a common, credibility-damaging error.
- Reference each figure/table near where it appears; place at top of page.

## What to defer to the appendix

Full hyperparameter tables, additional datasets, extra ablations, dataset/licensing
details, and per-seed numbers. Keep the main text to the experiments that directly support
the contributions.

## Honesty

- Report negative/mixed results where relevant; state limitations.
- Distinguish solved vs. open problems.
- Don't cherry-pick seeds or hide variance.

## Self-check

- Does each experiment test a stated claim mapped to a contribution?
- Are naive, prior, and alternative baselines all present and fairly tuned?
- Are there ablations isolating the source of the gain?
- Error bars, compute, and full hyperparameters reported?
- Is every figure described correctly and reproducibly in the text?
