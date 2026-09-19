# LaTeX and Manuscript Consistency

Use source checks for defects that can be established mechanically. Use substantive audits for scientific judgment.

## Active source graph

Start from the main document. Follow active `\input`, `\include`, and `\subfile` commands recursively. Restrict checks to that graph and its active bibliography, tables, algorithms, and appendices.

Exclude comments, generated build files, archived versions, response letters, and review reports unless the user includes them.

## Compilation evidence

When the project provides a documented build command, run it if the user has authorized verification and the command is safe. Otherwise use the available LaTeX build tool without changing sources.

Inspect the log for:

- undefined control sequences
- missing files
- undefined citations and references
- multiply defined labels
- fatal package or environment errors
- overfull boxes that obscure content

Do not treat every warning as a manuscript defect. Report the warnings that affect output or verification.

## Labels and references

Check:

- each `\ref`, `\eqref`, `\autoref`, and `\cref` target exists
- duplicate label definitions
- labels that are never referenced when they appear intended for cross-reference
- theorem, equation, figure, table, algorithm, and appendix references
- hard-coded object numbers that drift from LaTeX numbering

## Citations and bibliography

Check:

- every citation key exists in an active bibliography
- bibliography entries that appear unintentionally unused
- duplicate keys
- missing citations for specific external claims
- citation commands that do not match their grammatical role

A valid key does not establish that the cited paper supports the sentence. Route that question to literature or claim auditing.

## Macros and environments

Check:

- duplicate macro definitions
- conflicting definitions across included files
- argument-count mismatches
- theorem environments with inconsistent numbering
- symbols defined by a macro in one section and typed differently elsewhere
- local redefinitions that change meaning after first use

## Cross-artifact consistency

Compare:

- pseudocode variables with method text and theorem statements
- main-text and appendix theorem conditions
- captions with displayed values and units
- abstract numbers with tables and figures
- dataset, sample, task, model, and dimension counts across sections
- notation in equations with notation in prose
- algorithm step sizes and tolerances with implementation details

Do not infer a mismatch from an unreadable figure. Record that the value could not be checked.

## Draft artifacts

Search for unresolved placeholders such as `TODO`, `TBD`, `FIXME`, `XXX`, `??`, `\todo`, and empty references. Inspect context before reporting a match.

## Reporting

For each defect, provide:

`severity | file and line | exact source | why it is inconsistent | required correction`

Separate compiler-confirmed findings from source-inspection findings.
