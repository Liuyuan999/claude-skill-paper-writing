# Optimization and Theory Writing

Use this reference for optimization, theoretical ML, and algorithmic analysis.

## Result chain

Make the logical chain visible:

`problem -> assumptions -> reformulation or method -> lemmas -> convergence -> complexity -> interpretation`

Each result should have a role. A lemma should discharge a condition or establish a bound used later. A theorem should answer a paper-level question. A complexity corollary should follow from the convergence bound under a stated parameter choice and cost model.

## Problem setup

Define:

- variable spaces and feasible sets
- deterministic or stochastic objectives
- the available oracle or information model
- the target stationarity, optimality, feasibility, or approximation criterion
- exact and approximate subproblems
- norms and dimensions that affect constants or rates

For bilevel problems, distinguish the original problem, lower-level solution map, value function, penalized or constrained reformulation, and the implemented surrogate. Do not use these objectives interchangeably.

## Assumption writing

State assumptions tersely and explain their mathematical role near first use.

Prefer:

`Assumption 2 ensures that the lower-level solution is unique and that the value-function gradient is well defined.`

Avoid:

`While Assumption 2 may seem restrictive, it is commonly adopted in the literature.`

When useful, give a concrete setting where the condition holds. Do not claim that one condition implies another without verifying the direction and additional requirements.

Keep distinct:

- convexity and strong convexity
- PL inequalities and quadratic growth
- error bounds and gradient domination
- KL properties and a specific KL exponent
- smoothness and Lipschitz continuity of the function
- Lipschitz continuity of gradients, Hessians, or solution maps
- submodularity and modularity

## Reformulation and equivalence

For a value-function, penalty, primal-dual, or relaxation argument, separate:

1. the definition of the new problem
2. existence and regularity of the new objective or constraint
3. exact equivalence or quantified approximation to the original problem
4. the mapping from a solution or stationary point of the new problem to the original criterion
5. the effect of penalty, smoothing, inner-solve, or sampling error

Do not call a reformulation equivalent when only an asymptotic or error-bound relation is proved.

## Theorem statements

State:

- the assumptions or exact references to them
- the algorithm and parameter regime
- the output or iterate selection rule
- the criterion being bounded
- whether the result holds deterministically, in expectation, with high probability, or almost surely
- the dependence on iteration count and accuracy
- the cost model used by any complexity conclusion

An informal theorem may suppress constants but must not suppress conditions or change the criterion. The appendix theorem must match the main-text theorem.

## Proof sketches

A proof sketch should identify the key obstacle, the lemmas that resolve it, and the inequality or invariant that yields the result. Do not replace the argument with `See Appendix`.

For stochastic proofs, state the conditioning and filtration when needed. For min, max, expectation, differentiation, or limit interchanges, name the theorem or verify its conditions.

## Complexity accounting

Separate:

- iterations
- full-gradient evaluations
- stochastic first-order oracle calls
- function-value calls
- Hessian-vector or Jacobian-vector products
- projections or proximal operations
- linear-optimization oracle calls
- lower-level solver steps
- communication rounds
- memory and wall-clock cost

If an iteration contains a loop, batch, line search, or approximate solve, include that work in the final oracle count. State parameter dependence hidden by big-O when it affects comparison with prior work.

## Algorithm and theorem consistency

Check that the analyzed update matches the pseudocode in indexing, randomness, step sizes, projections, momentum, stopping, and subproblem accuracy. If the implementation differs, label the difference and state which result applies.

## Presentation

- Use one symbol per object.
- Define constants before use and do not change their dependence later.
- Restate a symbol's role when a long proof makes it hard to recover.
- Keep formal claims separate from interpretation.
- Do not apologize for a theorem's scope. State the regime directly.
