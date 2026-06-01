# paper-writing — Claude Code Skill

A [Claude Code](https://claude.ai/code) skill for writing academic papers in machine
learning, optimization, and theory. Encodes both general best practices and the "house
style" of the [Tianyi Chen](https://chen.tech.cornell.edu/) group
([Lisha Chen](https://lisha-chen.github.io/),
[Quan Xiao](https://jenniferquanxiao.github.io/),
[Liuyuan Jiang](https://liuyuan999.github.io/)).

## What it does

When invoked, the skill:
1. Clarifies your venue, page limit, and the paper's one core idea.
2. Routes to the relevant reference files (abstract/intro templates, theory conventions,
   experiments standards, or a paper-type playbook).
3. Drafts or reviews sections with the appropriate structure, notation, and style.

## Paper types covered

| Format | Target venues |
|--------|---------------|
| Theoretical journal | JMLR, Math. Programming, IEEE TSP, SIAM J. Opt. |
| ~10-page theoretical conference | NeurIPS, ICML, ICLR, AISTATS |
| ~10-page experimental conference | NeurIPS, ICML, ICLR |
| ~5-page short conference | ICASSP, EUSIPCO, workshops |

## Installation

```bash
# Clone into your Claude skills directory
git clone https://github.com/<your-username>/paper-writing \
    ~/.claude/skills/paper-writing
```

Or manually copy:
```bash
cp -R paper-writing ~/.claude/skills/paper-writing
```

## Usage

In any Claude Code session, invoke via the `/paper-writing` skill or just ask:

> *"Help me write the intro for my NeurIPS bilevel optimization paper."*
> *"Draft an abstract for a JMLR submission on multi-objective learning."*
> *"Write my rebuttal response to the reviewers."*
> *"Review my experiments section for an ICASSP paper."*

The skill reads the relevant reference files automatically before drafting.

## File structure

```
paper-writing/
├── SKILL.md                     # Skill definition (router + workflow)
└── references/
    ├── general-principles.md    # SPJ, Widom, Farquhar/Foerster, Steinhardt, Zobel
    ├── house-style.md           # Chen-group conventions & notation
    ├── abstract-and-intro.md    # Fill-in-the-blank templates
    ├── theory-writing.md        # Assumptions, theorems, proofs, penalty reformulation
    ├── experiments.md           # Baselines, ablations, error bars, figures
    ├── checklists.md            # NeurIPS-style checklist + pre-submission checklist
    ├── rebuttals.md             # Response-to-reviewers playbook
    └── paper-types/
        ├── journal-theoretical.md
        ├── conference-theoretical-10page.md
        ├── conference-experimental-10page.md
        └── conference-short-5page.md
```

## Knowledge sources

**General best practices** distilled from:
- Simon Peyton Jones, [*How to Write a Great Research Paper*](https://simon.peytonjones.org/great-research-paper/)
- Jennifer Widom, [*Tips for Writing Technical Papers*](https://cs.stanford.edu/people/widom/paper-writing.html)
- Sebastian Farquhar, [*How to Write ML Papers*](https://sebastianfarquhar.com/on-research/2024/11/04/how_to_write_ml_papers/) (building on [Foerster](https://www.jakobfoerster.com/how-to-ml-paper))
- Jacob Steinhardt, [*Advice for Authors*](https://jsteinhardt.stat.berkeley.edu/blog/advice-for-authors)
- Lipton & Steinhardt, [*Troubling Trends in ML Scholarship*](https://arxiv.org/abs/1807.03341)
- [NeurIPS Paper Checklist](https://neurips.cc/public/guides/PaperChecklist)
- Justin Zobel, *Writing for Computer Science*
- Devi Parikh et al., [*How we write rebuttals*](https://deviparikh.medium.com/how-we-write-rebuttals-dc84742fece1)

**House style** extracted from papers Lisha Chen and Tianyi Chen's lab in bilevel optimization and multi-objective learning (NeurIPS 2024/2025, ICML 2025,
ICLR 2025, JMLR 2024, Math. Programming 2025).

## Notes

- The reference files contain **paraphrased patterns and templates** — no verbatim text from
  source papers or guides.
- The skill instructs Claude to generate **fresh prose** in the target style, never copy
  from published papers.

## License

MIT
