---
name: latex-paper-audit
description: Mechanically audit a LaTeX academic paper for references, labels, citations, numbering, macros, notation, and cross-section numerical consistency. Use for source-level submission checks. Do not use as a generic LaTeX tutorial or substantive peer review.
metadata:
  version: 0.2.0
---

# LaTeX Paper Audit

Inspect the active manuscript sources and report concrete defects. Do not edit by default.

## Establish the active source graph

Identify the main file, then follow active `\input`, `\include`, and `\subfile` references recursively. Include active bibliography files, algorithm sources, tables, and appendices. Exclude build outputs, archived drafts, response letters, and files outside the include graph.

Read [latex-consistency.md](../../references/latex-consistency.md) and [review-severity.md](../../references/review-severity.md).

## Run mechanical checks

Check:

- undefined, unused, and duplicate labels
- unresolved references and equation references
- missing or unused citation keys
- figure, table, theorem, algorithm, and appendix references
- theorem numbering and environment consistency
- notation drift and conflicting definitions
- duplicated or conflicting macros
- obvious syntax and compilation errors
- placeholders and stale drafting artifacts

When compilation is available and safe, inspect the actual log. Distinguish compiler findings from source inspection.

## Run manuscript consistency checks

Compare:

- algorithm variable names with the surrounding text
- theorem notation with algorithm and proof notation
- captions with table or figure contents
- abstract and introduction numbers with experiment tables
- dimensions, dataset counts, iteration counts, and sample counts across sections
- main-text theorem statements with appendix versions

Do not claim a numerical mismatch when the referenced value is unavailable. State the inspection limit.

## Output

Group findings into compilation blockers, broken references or citations, notation and macro issues, and manuscript inconsistencies. Give the file, line or anchor, observed text, and required correction. Keep stylistic preferences out of the report.
