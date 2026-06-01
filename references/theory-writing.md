# Writing Theory: Assumptions, Theorems, Proofs

For theoretical papers in optimization / ML. Pair with `house-style.md` for the group's
notation and the penalty-reformulation pattern.

---

## The result hierarchy

| Environment   | Use for |
|---------------|---------|
| **Theorem**   | Your main result(s). Keep these scarce. |
| **Proposition** | An involved but secondary result. |
| **Lemma**     | A short/routine stepping stone toward a theorem. |
| **Corollary** | Something that follows easily from a theorem. |
| **Definition**| Formal objects/notation. |
| **Assumption**| Numbered standing conditions, reused by reference. |
| **Observation** / **Example** | (Group style) lightweight insights and instances. |

**Few theorems.** Ideally **one** main theorem, rarely more than three. A long list of
theorems dilutes the paper's one idea. Promote supporting results to lemmas/propositions.

## Assumptions

- **Number them and state them tersely**, then reuse by reference ("Under Assumptions 1–2…").
- **State the full set of assumptions inside each theorem statement** (or name them
  explicitly: "Under Assumptions 1–3, …"). A reader must see exactly what is assumed without
  hunting.
- Order from weakest/most-standard to strongest/most-novel. Flag which are standard
  (smoothness, Lipschitz gradients, bounded variance) vs. your contribution (e.g., a relaxed
  **flatness** or **PL** condition).
- After the main theorem, **discuss robustness**: what breaks if an assumption is violated,
  and which assumptions are essential vs. for convenience.

Common conditions in this area, weakest-to-strongest intuition:
- Smoothness / Lipschitz continuous gradients (`L`-smooth).
- Bounded gradient variance (stochastic setting).
- Polyak–Łojasiewicz (PL) — gives linear-rate-like behavior without convexity.
- Flatness conditions — relaxations the group introduces to avoid strong convexity of the
  lower level.
- (Strong) convexity — strongest; avoid assuming it if a PL/flatness relaxation suffices.

## Theorem statements

- **Foreground the rate/complexity in big-O** in the statement itself: e.g. "converges to
  an ε-stationary point in O(ε^{-1.5}) iterations", "O(1/√n) population risk",
  "O(γ^{-1}) penalty gap". Quote the headline rate in the abstract too.
- Define every symbol in the statement (or point to where it's defined).
- State the conclusion in terms the reader cares about (stationarity, optimality gap,
  generalization), not just an internal quantity.

Template:
```
Theorem 1 (informal). Under Assumptions 1–3, choosing step sizes <α, β> and penalty
γ = <schedule>, Algorithm 1 produces iterates {x_t} satisfying
    (1/T) Σ_t E‖∇F_γ(x_t)‖² ≤ O(<rate in T, ε, γ>).
Consequently, <interpretation: ε-stationarity in O(ε^{-c}) iterations>.
```
Provide a **formal version** in the appendix with all constants, and an **informal version**
in the body if constants would obscure the message.

## Proofs

- In the body, give a **proof sketch**: the key lemmas, the main inequality chain, and the
  one idea that makes it work. Cross-reference the full proof in the appendix.
- In the appendix, give **complete proofs** with all constants and steps.
- Build in **redundancy**: remind the reader what each symbol means; a single typo shouldn't
  break comprehension.
- State each lemma so it is reusable and independently checkable; reference the equation
  numbers it relies on.

## The penalty-reformulation pattern (group workhorse)

A recurring template for bilevel / constrained problems:

1. **Reformulate.** Replace the hard constraint (e.g., lower-level optimality
   `y ∈ argmin_z g(x,z)`) with a penalty:
   ```
   F_γ(x, y) := f(x, y) + γ · ( g(x, y) − min_z g(x, z) ).
   ```
2. **Relate** the penalized problem to the original — bound the gap (e.g., an
   `O(γ^{-1})` bias) and show stationary points of `F_γ` map to (approximate) solutions of
   the original.
3. **Analyze the landscape / error bound** of `F_γ` under your named assumption
   (PL / flatness), establishing the descent/convergence of a single-loop method.
4. **Tune `γ`** (fixed or scheduled) to trade bias against conditioning, yielding the final
   complexity.

When writing it: introduce `F_γ` early, motivate why the penalty avoids Hessian-vector
products / nested loops, then carry `F_γ` through the analysis.

## Avoiding "mathiness"

- Don't use mathematics that **impresses rather than clarifies**. Every theorem must convey
  a reusable insight.
- **The test:** *"Would I rely on this result to make a prediction or to get a system
  working?"* If not, reconsider whether it belongs.
- Don't conflate technical and informal uses of a term (e.g., "robust", "optimal") — define
  the technical sense and use it consistently.
- Prefer one clean theorem with a clear message over many ornate ones.

## Notation discipline

- Fix notation in a Preliminaries section; keep it consistent everywhere (see the notation
  table in `house-style.md`).
- Remind readers of variables not seen recently ("the dual variable λ", not just "λ").
- Euclidean norm `‖·‖` by default; declare any other norm.
- Write per-sample vs. empirical objects distinctly (`f_{z,m}` vs. `f_{S,m}`).

## Self-check

- Is there exactly one headline theorem, with supporting results demoted to lemmas?
- Are all assumptions stated inside/next to the theorem and discussed for robustness?
- Is the rate in big-O visible in both the abstract and the theorem?
- Does the body have a proof sketch and the appendix a complete proof?
- Does every theorem pass the "would I rely on it" test?
