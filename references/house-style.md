# House Style — Tianyi Chen / Lisha Chen / Quan Xiao / Liuyuan Jiang

The "house style" of this collaboration (centered on Tianyi Chen, with Lisha Chen, Quan
Xiao, Liuyuan Jiang) is highly consistent across their bilevel-optimization and
multi-objective-learning theory papers. Match these patterns when the user is in the group
or wants this style. All templates below are **paraphrased patterns** — generate fresh
prose, never paste from their published papers.

Representative papers to mirror (for tone, not text):
- *Beyond Value Functions: Single-Loop Bilevel Optimization under Flatness Conditions*, NeurIPS 2025 — arXiv:2507.20400
- *A Primal-Dual-Assisted Penalty Approach to Bilevel Optimization with Coupled Constraints*, NeurIPS 2024 — arXiv:2406.10148
- *Three-Way Trade-Off in Multi-Objective Learning*, JMLR 2024 — arXiv:2305.20057
- *FERERO: A Flexible Framework for Preference-Guided Multi-Objective Learning*, NeurIPS 2024 — arXiv:2412.01773
- *Unlocking Global Optimality in Bilevel Optimization*, ICLR 2025 — arXiv:2408.16087
- *On Penalty-Based Bilevel Gradient Descent Method*, Math. Programming 2025 — arXiv:2302.05185

---

## 1. Abstract — fixed 4-move arc (one paragraph)

1. **Context / importance** — name the paradigm and where it matters.
   > *"Bilevel optimization, a hierarchical optimization paradigm, has gained significant
   > attention in machine learning, notably in [applications]."*
2. **Gap / pain point** — a "However,…" sentence naming a concrete deficiency of prior
   methods (Hessian-vector products, nested loops, restrictive assumptions, no global
   guarantees).
   > *"However, due to the nested structure, most existing algorithms require either
   > Hessian-vector computation or nested loops, which …"*
3. **Proposal** — "In this paper / In this work, we propose …" naming the method, usually
   with a **coined acronym**.
   > *"In this paper, we propose [ACRONYM], a single-loop method that …"*
4. **Guarantee + evidence** — "we prove the convergence …" then "experiments demonstrate
   superior efficiency." **Theory claim precedes the experimental claim.**

Journal versions append a **Keywords** line.

## 2. Introduction flow (stereotyped — follow this order)

1. **Opening sentence** defines the paradigm generically.
2. **Application litany with dense citation clusters** — a signature tic:
   > *"…such as meta-learning [.,.], hyperparameter optimization [.], model pruning [.],
   > reinforcement learning [.], fine-tuning LLMs [.], and diffusion models [.]."*
3. **Early numbered problem formulation** — write the main problem as a display equation
   (Eq. (1)) on page 1–2, with objective signatures inline. For bilevel:
   > min_{x} f(x, y)  s.t.  y ∈ S*(x) = argmin_{y} g(x, y),   with f, g : R^{d_x}×R^{d_y} → R.
4. **Two-camp prior-art taxonomy** — partition existing work into two named families
   (e.g., "nested/AID-based" vs. "penalty/constrained"; "static" vs. "dynamic weighting"),
   then position the paper relative to both.
5. **Italicized / parenthesized research question**, answered affirmatively:
   > *(Q1) Can we design a single-loop, Hessian-free method with provable convergence?*
   > "Our answer is **affirmative**."
6. **"Best of both worlds" positioning** against the two camps.
7. **Early conceptual figure** (page 1–2): Pareto front, update-scheme cartoon, or loss
   landscape.
8. **Comparison table** vs. prior methods in applied/experimental papers — columns like
   *Single-loop / Hessian-free / Convergence / Assumptions*, with a "(ours)" row of ✓/✗.

## 3. Contributions — two coexisting formats

- **Conference (NeurIPS/ICML/ICLR):** a `§1.1 Our main results` / `Our contributions`
  subsection. Often a labeled list with bold lead-ins coded **C1) / C2) / C3)**, and a
  *separate* list of technical challenges coded **T1 / T2** — separating *what we deliver*
  from *what was hard*.
  > **C1)** The penalty reformulation has a benign landscape (Section 3). …
  > Technically we address: **T1)** unbounded multipliers; **T2)** lack of strong convexity.
- **Verbs are uniform:** *we propose, we establish, we prove, we show*; for surprising
  results, *"perhaps surprisingly, we find …"*.

## 4. Problem formulation, assumptions, theorems

- Heavy use of formal environments: `Assumption`, `Definition`, `Lemma`, `Theorem`, plus the
  group's distinctive **`Observation`** and **`Example`** environments.
- **Assumptions numbered, stated tersely, reused by reference** ("Under Assumption 1…").
  Standard ones: smoothness/Lipschitz gradients; lower-level strong convexity or the
  **Polyak–Łojasiewicz (PL)** condition; newer papers introduce relaxed **flatness
  conditions** as their named assumption.
- **Theorem statements foreground explicit rates in big-O**: O(1/√n) population risk,
  O(γ^{-1}) penalty gap, O(ε^{-1.5}) complexity — often already quoted in the abstract.
- **Penalty reformulation is the recurring workhorse**: reformulate a constrained/bilevel
  problem as min_x F_γ(x) := f(x,y) + γ·(g(x,y) − min_z g(x,z)), then analyze the
  landscape / error bound of the reformulation. (See `theory-writing.md`.)

## 5. Section organization (typical theory paper)

1. Introduction (with §1.1 "Our main results"/"Our contributions" + "Prior art" subsection)
2. Problem formulation / Preliminaries (Pareto optimality or bilevel definitions, notation)
3. Proposed reformulation + Algorithm (boxed `Algorithm 1`)
4. Theoretical analysis (assumptions → lemmas → main theorem)
5. Experiments (synthetic toy problems first, then real benchmarks)
6. Conclusion
- Extensive appendices with full proofs (papers run 30–79 pages total).
- Journal versions add: *"A preliminary version of this work appeared at [conf]."*
- A **code-availability line** ("Code is available at github.com/…") is standard.

## 6. Notation conventions

**Bilevel**
- Upper-/lower-level variables: `x, y` (sometimes `u, v`).
- Upper-level objective `f`, lower-level `g`.
- Lower-level solution set `S*(x)` or `Y*(x)`; hyper-objective `φ(x)` or `F(u)`.
- Penalty constant `γ`; penalized objective `F_γ`, `F̃_γ`.

**Multi-objective**
- Model parameter `x` or `θ ∈ R^d` (or `R^q`).
- `M` objectives indexed `m ∈ [M]`, where `[M] = {1,…,M}`.
- Vector objective `F(x) = [f_1(x), …, f_M(x)]`; cone `C` for the partial order.
- Pareto front / Pareto stationarity language.

**General**
- Dimensions `d_x, d_y` (or `d_1, d_2`); gradients `∇_x f`; Euclidean norm `‖·‖` by default;
  rates in `O(·)`.
- Per-sample vs. empirical objectives written explicitly: `f_{z,m}` (per-datum) vs.
  `f_{S,m}` (empirical).

## 7. Stylistic fingerprints to imitate

- **One coined acronym per method**, expanded on first use, reused throughout.
- **"However,"** as the standard pivot into the gap.
- **"Perhaps surprisingly,"** to flag a counter-intuitive theorem.
- **Italicized/parenthesized research questions** answered "affirmative".
- **Two-camp taxonomy** of prior work, then "best of both worlds".
- **Theory-before-experiments** ordering in both abstract and body.
- **Dense citation clusters** attached to application lists.

## 8. What to avoid (even in this style)

- Don't let the application litany become padding — keep it to one sentence with tight
  clusters.
- Don't multiply theorems; the group foregrounds **one** main result with supporting lemmas.
- Don't coin more than one acronym per method.
- Keep "However," / "Perhaps surprisingly," to one use each — overuse reads as a tic.
