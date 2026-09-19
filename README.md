# Academic Research Skills

A compact skill suite for writing and auditing papers in optimization, machine learning, theoretical ML, algorithms, and applied ML.

The suite targets NeurIPS, ICML, ICLR, AISTATS, ICASSP, IEEE-style venues, and optimization or theoretical ML journals. It favors direct technical prose, explicit claim discipline, and optimization-aware review.

## Skills

- **paper-writing** drafts and revises paper sections. It is the central skill.
- **paper-review** runs eight reviewer-style passes without rewriting by default.
- **proof-audit** builds a theorem dependency graph and locates exact logical gaps.
- **claim-evidence-audit** checks claims against theorems, experiments, figures, tables, and conclusions in both directions.
- **literature-positioning** verifies and synthesizes related work along precise technical axes.
- **experiment-audit** checks design, comparison budgets, oracle accounting, failures, and reporting.
- **latex-paper-audit** checks mechanical LaTeX and manuscript consistency.

Results-to-writing is a mode inside `paper-writing` and `experiment-audit`, not a separate skill. This keeps quantitative interpretation rules in one shared reference.

## Design

The skill entrypoints live in `skills/`. Shared technical guidance lives in `references/`.

```text
skills/
  paper-writing/SKILL.md
  paper-review/SKILL.md
  proof-audit/SKILL.md
  claim-evidence-audit/SKILL.md
  literature-positioning/SKILL.md
  experiment-audit/SKILL.md
  latex-paper-audit/SKILL.md

references/
  writing-style.md
  claim-strength.md
  paper-sections.md
  optimization-theory.md
  experiment-reporting.md
  literature-positioning.md
  latex-consistency.md
  review-severity.md
  venue-notes.md
  rebuttals.md
```

Each skill loads only the references needed for its task. Review breadth belongs to `paper-review`. Deep formal, claim, experiment, literature, and source checks belong to their specialized skills.

## Writing invariant

Every prose-generating workflow follows the same standard:

- direct, technical, and compact
- confident when supported and qualified when required
- no defensive writing or invented reviewer dialogue
- no routine semicolons or em-dash-driven sentence structure
- no generic AI academic filler
- no unsupported promotion from observation or interpretation to formal claim
- no manufactured limitations paragraph or paper roadmap

## Installation

This repository includes a Claude Code plugin manifest at `.claude-plugin/plugin.json`. Clone the repository and load the repository root through your client's local plugin workflow. The individual skill entrypoints are under `skills/` for manual inspection or selective installation.

```bash
git clone https://github.com/Liuyuan999/claude-skill-paper-writing.git
```

Keep the repository structure intact because the skills share the files in `references/`.

## Example requests

- `Revise this theorem statement and assumption discussion using paper-writing.`
- `Review this NeurIPS optimization paper without rewriting it.`
- `Audit the proof dependency from Assumption 2 to Theorem 4.`
- `Check whether every introduction claim is supported by a theorem or experiment.`
- `Position this bilevel method against value-function and implicit-differentiation methods.`
- `Audit whether these baselines use comparable oracle and wall-clock budgets.`
- `Check this LaTeX project for broken references and inconsistent theorem notation.`

## Reference projects

The design was informed by mechanisms from these public projects without copying their domain-specific rules or large workflows:

- [academic-writing-skills](https://github.com/WenyuChiou/academic-writing-skills)
- [literature-review-skill](https://github.com/pinshuai/literature-review-skill)
- [literature-review](https://github.com/chenlu-hung/literature-review)
- [research-skills](https://github.com/jluo41/research-skills)
- [AI-research-feedback](https://github.com/claesbackman/AI-research-feedback)
- [claude-skills](https://github.com/lcrawfurd/claude-skills)
- [awesome-academic-skills](https://github.com/O0000-code/awesome-academic-skills)

The adapted mechanisms include evidence mapping, thematic synthesis, citation verification, source-of-truth consistency, anchored review findings, deterministic mechanical checks, and explicit activation boundaries.

## License

MIT
