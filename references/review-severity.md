# Review Findings and Severity

Use this reference for every audit skill.

## Evidence anchor

Every substantive finding needs an anchor that a reader can inspect:

- file and line when sources are available
- section and quoted phrase for prose
- theorem, lemma, assumption, equation, or algorithm label
- figure, table, dataset, metric, or log entry

If the evidence is unavailable, state the verification limit. Do not fill the gap with a plausible criticism.

## Severity

### Blocker

The main claim cannot currently be trusted or the submission cannot be evaluated. Examples include a false theorem step, a missing condition that invalidates the result, an algorithm that differs from the analyzed update, a central claim with no evidence, or a broken manuscript build that hides content.

### Major

The paper's contribution, scope, comparison, or reproducibility is materially unclear or overstated, but a bounded repair may resolve it.

### Minor

A local issue affects precision, consistency, or readability without changing the central result.

Do not assign severity based on how easy an issue is to fix. Rank by consequence for correctness, evidence, interpretation, and evaluation.

## Evidence status

Use one status:

- **confirmed**: directly visible in the supplied artifacts
- **probable**: strongly indicated but dependent on unavailable material
- **unverified**: cannot be assessed from the supplied artifacts

Do not present probable or unverified findings as facts.

## Finding format

For each finding, report:

1. anchor
2. category
3. severity and evidence status
4. exact problem
5. consequence
6. minimum repair or author decision

Use the specialized category set when a skill defines one. Proof audits use correctness issue, missing justification, notation issue, assumption mismatch, and presentation improvement.

## Prioritization

- Report substantive issues before style.
- Deduplicate the same defect found in several passes.
- Keep separate defects separate when they require different repairs.
- Do not target a fixed number of findings.
- State clean categories only when they were actually checked.
- Do not issue a publication verdict unless the user requests one and the evidence supports it.

## Review boundary

A review request authorizes diagnosis, not rewriting. Provide a concrete repair direction, but do not replace the author's argument or prose unless asked.
