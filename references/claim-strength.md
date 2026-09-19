# Claim Strength and Evidence

Classify a statement before drafting or auditing it. Do not silently promote one category into another.

## Claim categories

### Formal mathematical claim

A definition, proposition, lemma, theorem, corollary, or proved consequence. State the conditions, mathematical object, quantifiers, and conclusion. Use `prove`, `establish`, or `guarantee` only when the cited argument supports the exact statement.

### Interpretation

An explanation of what a formal or empirical result means. An interpretation can be compelling without being proved. Tie it to the result and avoid presenting a mechanism as established unless the paper tests or derives that mechanism.

### Empirical observation

A measured pattern under a stated dataset, problem family, metric, protocol, and uncertainty estimate. Use `we observe`, `the results show`, or a direct numerical statement. Do not generalize beyond the evaluated regime.

### Motivation

The reason a problem, regime, or technical obstacle matters. Motivation does not establish novelty, prevalence, or practical impact without supporting evidence.

### Conjecture or hypothesis

An unresolved mathematical or empirical proposition. Label it explicitly. Do not turn suggestive evidence into a theorem or factual mechanism.

### Implementation choice

A decision about architecture, solver, data processing, stopping, approximation, or engineering. Describe what was chosen and why. Do not present the choice as an inherent property of the abstract method.

## Valid movement between categories

- A theorem may support an interpretation, but the interpretation needs its own scope.
- An experiment may corroborate a theoretical prediction, but it does not prove the theorem.
- A repeated empirical pattern may motivate a conjecture, but it does not establish a universal law.
- An implementation may instantiate an algorithm, but observed implementation behavior is not an algorithmic guarantee.
- A citation may support motivation or prior-work characterization, but it does not prove the current paper's claim.

## Claim-strength checks

For each major statement, identify:

- the category
- the scope
- the evidence source
- the inference from evidence to wording
- the repeated versions elsewhere in the paper

Use the narrowest wording that retains the contribution. Narrow does not mean timid. A precise claim is often stronger than a broad claim surrounded by caveats.

## High-risk terms

### First and novel

Require verified literature support and a defined comparison set. Prefer the exact technical delta when priority cannot be established.

### State of the art

Require comparable baselines, protocols, metrics, and budgets. Name the benchmark and setting.

### Scalable

Name the scaling variable and show time, memory, oracle calls, or success as that variable grows.

### Significant

State whether the term is statistical. Give the test or interval when statistical significance is claimed. Use a quantitative adjective or direct value for practical magnitude.

### Efficient

Name the cost model. Iteration complexity, oracle complexity, wall-clock time, memory, and communication are different claims.

### Robust

Name the perturbation, distribution shift, parameter range, or failure mode tested.

## Internal claim ledger

When auditing a paper, record each major claim with:

`location | exact wording | category | scope | evidence | support level | repeated locations`

Use `establishes`, `supports`, `suggests`, `motivates`, or `does not support` for the support level.
