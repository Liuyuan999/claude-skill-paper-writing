# Literature and Novelty Positioning

This is a compact workflow for related work in ML, optimization, theoretical ML, and algorithms. It is not a systematic-review protocol.

## Define the comparison

Begin with the paper's exact technical claim. Convert broad novelty language into comparison axes that can be checked.

For optimization, common axes include:

- constrained or unconstrained problem
- continuous or discrete variables
- convex, nonconvex, strongly convex, PL, or other structure
- exact or approximate lower-level solution
- first-order, second-order, Hessian-vector, projection, or linear-optimization access
- single-loop or nested updates
- value-function, implicit-differentiation, penalty, primal-dual, or surrogate approach
- deterministic or stochastic setting
- asymptotic convergence or finite-time complexity
- stationarity, feasibility, optimality, approximation, or regret criterion
- iteration count and each oracle count

Compare only axes that matter to the claimed contribution.

## Source verification

Use primary papers and official publication records. Verify title, authors, venue, year, problem setting, assumptions, theorem statement, complexity, and experimental protocol before relying on them.

Do not generate citation keys or bibliographic details from memory. If only a secondary description is available, mark the characterization as provisional.

## Internal comparison matrix

For each close paper, record:

`family | problem | assumptions | oracle | algorithm | guarantee | criterion | complexity | experiments | source location`

Add a note when a field is absent or unclear. Do not convert unclear into no.

## Synthesis workflow

1. Identify the closest work.
2. Cluster papers by methodological family.
3. State what each family assumes.
4. State what each family guarantees.
5. State differences in oracle and computational model.
6. Mark comparisons that are not apples to apples.
7. Map agreements, contradictions, and unresolved gaps.
8. Formulate the precise gap filled by the current paper.

Write by family and technical distinction. A paragraph should synthesize several sources around one comparison axis. Do not produce a sequence of isolated paper summaries.

## Gap discipline

A gap can be:

- an unstudied problem regime
- a stronger guarantee under comparable conditions
- a weaker assumption for the same guarantee
- a cheaper oracle model for the same criterion
- a method that removes a concrete computational bottleneck
- empirical evidence under a regime not previously evaluated
- a contradiction between existing results that the paper resolves

Do not define a gap as a missing application, acronym, or implementation detail unless that is the actual contribution.

## Apples-to-apples checks

Before writing `improves`, `matches`, or `requires weaker assumptions`, verify that the compared results use compatible:

- problem classes
- output criteria
- accuracy definitions
- stochastic guarantees
- oracle models
- hidden parameter dependence
- initialization and regularity conditions

When more than one axis changes, describe the trade-off instead of declaring dominance.

## Related-work prose

- Give the closest work enough detail to make the delta checkable.
- State prior results directly and accurately.
- State the current paper's difference after the family is defined.
- Avoid dismissive labels and generic praise.
- Avoid priority claims unless the search supports them.
