# Experiment Design and Reporting

Use this reference for experiment audits and factual Results-section writing.

## Claim to experiment map

For each empirical claim, record:

`claim | problem or dataset | metric | baselines | budget | protocol | result | uncertainty`

An experiment should test an identifiable claim. A major claim should have evidence under a protocol that makes the comparison interpretable.

## Problems and datasets

- State the task, data source, split, preprocessing, and exclusion rules.
- For synthetic problems, state the generative parameters and what theoretical mechanism the problem isolates.
- For real data, state the regime over which the claim is intended to hold.
- Do not describe one dataset as broad empirical validation without a reason.

## Baselines and comparability

- Include methods that test the claimed improvement, not only methods that are easy to beat.
- State whether code is official, reimplemented, or adapted.
- Tune baselines under a comparable search protocol and validation budget.
- Keep initialization, preprocessing, data access, hardware, precision, and stopping criteria comparable when the claim depends on them.
- State any deviation that changes the interpretation of a comparison.

## Budget and oracle accounting

Report the budget that matches the claim. Possible budgets include wall-clock time, iterations, epochs, samples, gradient calls, stochastic first-order calls, Hessian-vector products, projections, linear-optimization calls, lower-level steps, memory, and communication.

Do not compare iteration counts when per-iteration costs differ materially. Do not hide preprocessing, compilation, warm starts, line searches, inner solves, or evaluation calls when they contribute to the reported cost.

## Hyperparameters and stopping

- Report search spaces, selection criteria, and the data used for tuning.
- Give each method a defensible tuning budget.
- State initialization and random seed handling.
- Use stopping rules tied to the same target when possible.
- Flag a tolerance or early-stopping rule that systematically favors one method.

## Variance and statistical language

State the number of independent runs and what error bars represent. Distinguish standard deviation, standard error, confidence interval, and quantiles. Do not call a difference significant without a defined statistical analysis.

## Ablations and scaling

- Use ablations to isolate the component named in the contribution.
- Use sensitivity studies for parameters that control the claimed trade-off.
- Vary the exact dimension named by a scalability claim.
- Report time and memory as well as accuracy when resource scaling matters.
- Interpret a flat curve only over the evaluated range.

## Baseline failure reports

Distinguish timeout, out-of-memory, numerical divergence, failed convergence criterion, and software error. Record the threshold, budget, hardware, and evidence.

Explain the computational mechanism only when code or algorithm structure supports it. For a bilevel method, the cause might be a growing lower-level solve, a Hessian system, a stored Jacobian, or repeated oracle calls. A failed run alone does not identify the cause.

## Results-to-writing procedure

When converting logs, tables, or plots into prose:

1. Extract the exact values, units, aggregation, and uncertainty.
2. Compute differences using the correct quantity.
3. Select the observations that answer the experiment's stated question.
4. State observations before interpretation when the distinction matters.
5. Connect each selected observation to a paper-level claim.
6. Verify the final prose against the source artifact.

Distinguish:

- **absolute difference**: `a - b` in the metric's units
- **percentage-point difference**: subtraction between percentages
- **relative difference**: `(a - b) / b`
- **percent improvement**: a relative difference expressed as a percentage, with direction defined

Do not narrate every cell. For a typical Results section, select two to four observations that carry the main argument. Use fewer or more when the evidence structure requires it. Report trade-offs and mixed results when they affect the claim.

## Factual prose patterns

Prefer:

`Method A reaches the target tolerance in 18 minutes, compared with 47 minutes for Method B under the same oracle budget.`

`Accuracy increases by 2.1 percentage points, from 81.4% to 83.5%.`

Avoid:

`Method A significantly outperforms Method B.`

unless significance is defined and supported.
