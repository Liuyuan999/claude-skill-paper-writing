# Writing Style

Apply this style to every skill that generates prose.

## Core style

Write direct, technical, compact prose. State the strongest claim supported by the mathematics, experiments, or cited evidence. Qualify a claim only when the qualification changes its truth or scope.

Prefer positive statements of what the paper establishes. Do not organize prose around imagined objections. Do not repeatedly explain what the method does not claim. State a necessary boundary once, where it affects interpretation.

## Defensive writing

Delete reflexive hedges when the evidence already supports the sentence:

- `we believe`, `we hope`, and `we feel`
- `may`, `might`, `could`, and `potentially`
- `appears to` and `seems to`
- `it is important to note that`
- `it is worth noting that`
- `although one might argue`
- `we acknowledge that`
- `admittedly`

Keep uncertainty for a conjecture, noisy estimate, extrapolation, unresolved mechanism, or genuine logical condition. Name the source of uncertainty. Do not spread one uncertainty marker across claims that have different support.

State scope without apology:

- Prefer `We study smooth nonconvex objectives.`
- Avoid `We only consider the admittedly restrictive smooth nonconvex setting.`

Explain what an assumption enables mathematically. Discuss where it holds only when that fact helps the reader interpret the result.

## Technical specificity

Replace evaluative adjectives with the relevant object and measure.

- Replace `better performance` with the metric, comparison, and setting.
- Replace `efficient` with iteration, oracle, memory, or wall-clock complexity.
- Replace `scalable` with the dimension varied and the observed resource curve.
- Reserve `significant` for a defined statistical meaning.
- Use `optimal` only with the stated criterion and comparison class.

Avoid promotional contribution language. Verbs such as `prove`, `establish`, `derive`, `design`, and `observe` should point to a specific result.

## Prohibited filler

Avoid generic academic and AI phrasing, including:

- `This highlights`
- `This underscores`
- `plays a crucial role`
- `offers a promising avenue`
- `in real-world scenarios`
- `a wide range of`
- `has attracted significant attention`
- `with the rapid development of`
- `in today's world`
- `the rest of this paper is organized as follows`

Do not add a roadmap unless explicitly requested or required. Do not manufacture a limitations paragraph, future-work paragraph, or broad-impact claim from a generic template.

## Sentence construction

- Avoid routine semicolons in prose. Split independent claims or state their relation directly.
- Do not use em dashes to carry sentence structure. Use a period, comma, or a subordinate clause.
- Keep parenthetical remarks short and rare. Move important content into the sentence.
- Avoid repeated colon-led rhetorical constructions. Use headings, full sentences, or compact lists when they improve structure.
- Keep one main logical job per sentence.
- Use stable technical terms. Do not rotate synonyms for defined concepts.
- Name the object instead of using vague `this`, `that`, or `it` when the referent is not immediate.

## Revision pass

For the exact candidate text:

1. Underline the main claim of each paragraph.
2. Move the claim earlier when background or apology delays it.
3. Circle each hedge and retain only those that alter truth conditions.
4. Mark every adjective of quality and replace it with evidence or remove it.
5. Check semicolons, em dashes, parentheses, and colon-heavy constructions.
6. Check every sentence against the claim categories in [claim-strength.md](claim-strength.md).
