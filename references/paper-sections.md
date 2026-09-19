# Section-Specific Writing

Use the paper's actual contribution and evidence to choose structure. Do not force fixed page allocations, sentence counts, or contribution counts.

## Title

- Name the problem and the technical contribution.
- Include a method name only when it helps identification.
- Avoid claims such as efficient, scalable, optimal, or robust unless the paper defines and establishes them.
- Keep the scope no broader than the results.

## Abstract

- State the problem and the technical gap without generic field promotion.
- Name the method or analytical idea precisely.
- State the strongest formal result with its setting and criterion.
- State the strongest empirical result with its benchmark, metric, or computational regime.
- Keep formal claims, empirical observations, and interpretation distinct.
- Do not add citations, a roadmap, generic implications, or a limitations sentence by default.

## Introduction

- Define the problem early enough that the contribution is interpretable.
- Explain the actual technical obstacle, not a generic statement that the problem is challenging.
- Position the method against the closest technical alternatives.
- State contributions as specific deliverables tied to sections, theorems, algorithms, or experiments.
- Avoid marketing labels, application litanies, fake reviewer questions, and obligatory `best of both worlds` framing.
- Use a motivating example or figure only when it exposes the core obstacle or idea.

## Related work

- Organize by methodological family and technical axis.
- Compare problem class, assumptions, oracle access, algorithm structure, guarantees, and empirical protocol.
- Treat the closest work in enough detail to make the paper's delta checkable.
- Do not write one paragraph per paper.
- Use [literature-positioning.md](literature-positioning.md) for the comparison workflow.

## Problem formulation and notation

- Define decision variables, spaces, objectives, constraints, data distributions, and oracle access.
- Define the target solution or stationarity notion before stating a guarantee.
- Separate the original problem from surrogate, penalized, relaxed, or empirical objectives.
- Declare norms, dimensions, randomness, expectations, and indexing conventions.
- Introduce only notation used by the argument.

## Assumptions

- State each condition in a form that can be checked and cited.
- Explain the mathematical consequence used later.
- Say where the condition holds only when this helps interpret scope or provides a verifiable example.
- Do not call an assumption standard as a substitute for explaining its role.
- Do not defend an assumption against an imagined objection.

## Method and algorithm

- State the object being optimized or approximated.
- Explain the update or subproblem before giving pseudocode when the mechanism is not obvious.
- Keep pseudocode, equations, step sizes, indexing, oracle calls, and implementation description consistent.
- Distinguish the abstract algorithm from implementation choices.
- State what is exact, approximate, stochastic, projected, or solved to tolerance.

## Theory

- State the theorem in the same regime analyzed by the proof.
- Make the target criterion and complexity measure explicit.
- Give the proof idea and the role of each supporting lemma.
- Separate equivalence, approximation, convergence, and complexity results.
- Use [optimization-theory.md](optimization-theory.md) for optimization-specific guidance.

## Experiments and results

- State the question each experiment answers.
- Describe the protocol needed to interpret the comparison.
- Report observations before broader interpretation.
- Tie ablations and scaling studies to specific method or theory claims.
- Do not narrate every table cell.
- Use [experiment-reporting.md](experiment-reporting.md) for design and quantitative prose.

## Conclusion

- Synthesize what the paper establishes.
- Preserve the scope and claim category used in the body.
- Do not introduce new results, mechanisms, citations, applications, or future-work boilerplate.
- Include a limitation or open question only when it is substantive and useful.

## Appendix

- Match theorem names, assumptions, notation, and constants used in the main text.
- Include complete proofs and auxiliary results needed to verify the main claims.
- Separate supplementary theory, implementation details, and additional experiments.
- Make every appendix item reachable from the main paper when it supports a claim.
