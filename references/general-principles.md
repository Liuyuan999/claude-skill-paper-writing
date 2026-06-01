# General Principles of Paper Writing

A consolidated, actionable digest from the canonical sources. Use this as the baseline for
any paper; layer the house style and the paper-type playbook on top.

---

## Process

1. **Write early — the paper develops the idea.** Don't wait for a "finished" result.
   Drafting forces clarity and exposes what you don't understand (Peyton Jones, "Don't
   wait: write").
2. **Draft via recursive bullets**: section outline → paragraph outline → key ideas →
   sentences, getting feedback at each stage (Farquhar/Foerster).
3. **Use readers carefully.** Each person can read your paper fresh only once. Recruit both
   experts and non-experts; ask "*where did you get lost?*" not "any typos?". Send a draft
   to the competition: "could you check I describe your work fairly?" — they are often your
   referees.
4. **Revise hard.** Read it aloud; print and mark in red. "At first, cut words. Later, cut
   sentences and subsections." Good writing is rewriting (Zobel).

## The one idea

- Have exactly **one "ping"**: one clear, sharp, *reusable* insight useful to the reader.
- State it 100% explicitly — don't make readers guess. If you have several ideas, write
  several papers (Peyton Jones).

## Abstract (≈4 sentences)

A one-paragraph version of the paper that serves three audiences (casual reader, expert
deciding whether to read on, past reader recalling the work). The classic four moves:

1. **Problem** — what problem does the paper address?
2. **Why it matters** — why is it interesting/important?
3. **What you did/achieved** — your approach and result, including your single most
   remarkable number if empirical.
4. **What follows** — the consequence or takeaway.

Open with a claim everyone agrees with, then state something many would find surprising
(Steinhardt).

## Introduction (~1 page — referees often decide accept/reject here)

It does two things: **describe the problem** and **state contributions**.

- **Describe the problem with a concrete example**, not generalities. Avoid the "molehill"
  opening ("Programs often have bugs. It is important to eliminate them [1–6]…"). Lead with
  a specific instance that makes the problem vivid.
- **State contributions as a refutable bulleted list, written first** — the list drives the
  whole paper. Each bullet must be falsifiable ("We *prove* the method converges at rate
  O(1/√T) (Section 4)", not "We *study* convergence") and **forward-reference** its section.
- Cover **Widom's five questions**: (1) What is the problem? (2) Why is it interesting and
  important? (3) Why is it hard / why do naive approaches fail? (4) Why hasn't it been
  solved (why are prior solutions inadequate)? (5) What are the key components of your
  approach and results, and the limitations?
- Every claim in the intro must be backed by evidence elsewhere; forward-reference it.
- **Cut filler**: "increasingly important", "much recent interest", "with the rise of…".
- **No "the rest of this paper is organized as follows."** Weave forward references into the
  narrative instead.

## Figures

- **Figure 1 is the most important figure** — many readers go straight to it. Use it to
  convey the core idea (a method cartoon, a Pareto front, a landscape). Place it top of
  page 1–2, near the abstract/intro.
- Figures: vector/PDF, fully labeled, legible in black-and-white, placed near first
  reference. Describe each figure correctly in the text — triple-check axes and trends.

## Body & method

- **Intuition before formalism**; examples before the general case. Don't open a section
  with dense algebra.
- Take the **most direct route to the idea** — do not recapitulate your personal journey of
  discovery.
- Aim to make the method/contribution clear by ~page 3 ("If your methods section starts
  after page 3, rearrange things").
- Every section tells the story of the *results*, not how you got them.

## Related work — later, and methodological

- Place it **after** you have presented your idea (early placement is incomprehensible to a
  reader who doesn't yet know your contribution, and it gets between the reader and your
  idea).
- Organize **by theme / "the diff"** between your work and the field — not a paper-by-paper
  list ("Smith did X, Jones did Y").
- Be **generous**: "credit is not like money." Acknowledge competitors warmly and state
  your own weaknesses. Never misrepresent prior work.

## Theory

- **Few theorems** — ideally 1, rarely more than 3. A long list dilutes the ping.
- Naming: **Theorem** = main result; **Proposition** = involved but secondary; **Lemma** =
  routine stepping stone; **Corollary** = follows easily.
- **State the full set of assumptions inside each theorem.** Give complete proofs (body or
  appendix) with a **proof sketch** and cross-references.
- Disclose how robust the result is to violated assumptions.
- **Avoid "mathiness"** — math that impresses rather than clarifies. Test every theorem:
  *"Would I rely on this to make predictions or to get a system working?"* (Lipton &
  Steinhardt).

## Experiments

- Ask **"what worked and why"**, not just "how well". The strongest empirical papers use
  **error analysis, ablations, and robustness checks** (to hyperparameters and datasets).
- Compare against **naive, prior, and alternative** baselines.
- Report **error bars / significance**, **compute** (hardware, per-run and total), and full
  hyperparameters and how they were chosen.
- Be explicit about which problems are **open vs. solved**.

## Reproducibility / checklist

- Claims in abstract/intro must match actual results and scope.
- State limitations and the full set of assumptions.
- Release code/data with exact commands and environment.
- Report statistical significance and compute. (See `checklists.md`.)

## Local style

- **Be precise**: swap vague "performance" for "accuracy" or "wall-clock time".
- **Be concise**: wordiness wastes page-limited space.
- **Simple sentences**; one idea each.
- **Consistent terminology**: refer to the same thing the same way every time.
- Avoid **nominalizations** ("perform an evaluation of" → "evaluate"), nonreferential
  "this/it/that", and "etc." / "for various reasons" (give the reasons).
- Define each term once, before first use.
- LaTeX: `\citet` for "Smith (2001) shows…", `\citep` for "(Smith, 2001)"; never
  "(Smith, 2001) shows…". Put `\label` after `\caption`.
- Read Strunk & White; Zobel, *Writing for Computer Science*.

## Reviewing & reviews

- Treat every review as "gold dust." When a reviewer misunderstands, **fix the paper so the
  misunderstanding can't recur** — don't argue "I meant X." (See `rebuttals.md` for the
  full response playbook.)

---

## Sources

- Simon Peyton Jones, *How to Write a Great Research Paper* — https://simon.peytonjones.org/great-research-paper/
- Jennifer Widom, *Tips for Writing Technical Papers* — https://cs.stanford.edu/people/widom/paper-writing.html
- Sebastian Farquhar, *How to Write ML Papers* — https://sebastianfarquhar.com/on-research/2024/11/04/how_to_write_ml_papers/ (building on Jakob Foerster, *How To ML Paper* — https://www.jakobfoerster.com/how-to-ml-paper)
- Jacob Steinhardt, *Advice for Authors* — https://jsteinhardt.stat.berkeley.edu/blog/advice-for-authors
- Lipton & Steinhardt, *Troubling Trends in ML Scholarship* — https://arxiv.org/abs/1807.03341
- NeurIPS Paper Checklist — https://neurips.cc/public/guides/PaperChecklist
- Justin Zobel, *Writing for Computer Science*
- Devi Parikh et al., *How we write rebuttals* — https://deviparikh.medium.com/how-we-write-rebuttals-dc84742fece1
