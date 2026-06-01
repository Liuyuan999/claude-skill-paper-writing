# Playbook: ~5-Page Short Conference Paper

**Target venues:** ICASSP, EUSIPCO, many workshops, and short/extended-abstract tracks.
**Length:** ~4–5 pages including references (venue-dependent). Two-column. Very tight.

Combine with: `general-principles.md`, `house-style.md`, `abstract-and-intro.md`, plus
`theory-writing.md` *or* `experiments.md` depending on the paper's nature.

---

## Mindset: one contribution, one result

A short paper is **not** a compressed long paper — it is a single, sharp contribution. Pick
**one** idea and **one** headline result (one theorem *or* one decisive experiment).
Everything that doesn't serve that gets cut. The bar is "interesting and correct", not
"comprehensive".

## Section skeleton (suggested, two-column, ~5 pp incl. refs)

1. **Abstract** — 3–4 sentences: context → gap → method (acronym) → the one result. [—]
2. **Introduction** (~0.75 pp) — problem + a *short* application phrase, the gap, the idea,
   and a compact contribution statement (prose or 2–3 bullets). Fold light related-work
   here. **Figure 1** if it earns its space.
3. **Method / Formulation** (~1.5–2 pp) — formulation (Eq. 1), the proposed method /
   reformulation, **Algorithm 1** if it fits. State assumptions tersely.
4. **Result** (~1 pp) — *either* the single theorem (informal; proof deferred to a longer
   version / brief sketch) *or* the key experiment with a clear table/figure + error bars.
5. **Conclusion** (~0.25 pp) — one or two sentences; point to the extended version.
6. **References.**

## Emphasize

- **Ruthless cutting** — "first cut words, then sentences and subsections." Every sentence
  earns its place.
- **One clear takeaway** stated in the abstract and delivered once.
- A single, legible **Figure 1 or one table** that carries the result.
- Pointer to an **extended/arXiv version** for full proofs/experiments
  ("Full proofs and additional experiments appear in the extended version [link].").

## De-emphasize / cut

- Full proofs (defer to extended version; at most a one-line sketch).
- Extra experiments, ablations beyond the essential one, large hyperparameter tables.
- Long related-work surveys — a few key citations, thematic, one or two sentences.
- Second theorems, second acronyms, second figures that don't carry the result.

## Pitfalls

- **Cramming a 10-page paper into 5** — produces dense, unreadable text. Drop scope instead.
- Spending the page budget on background rather than the contribution.
- Stating a theorem with no proof and no pointer to one.
- Overclaiming generality the single result doesn't support.
- Figures too small to read in two-column format — simplify, don't shrink.
