---
name: paper-writing
description: Use when writing, drafting, structuring, or revising an academic paper in machine learning, optimization, or theory — including the abstract, introduction, related work, problem formulation, theorems/proofs, experiments, or a rebuttal/response-to-reviewers. Covers NeurIPS/ICML/ICLR/AISTATS, JMLR/IEEE TSP/Math. Programming journals, and short venues (ICASSP/EUSIPCO/workshops). Encodes both general best practices and the "house style" of the Tianyi Chen / Lisha Chen / Quan Xiao / Liuyuan Jiang group (bilevel & multi-objective optimization).
version: 0.1.0
---

# Paper Writing (ML / Optimization / Theory)

## Overview

This skill helps you draft and revise academic papers in machine learning, optimization,
and theory. It carries two layers of knowledge:

1. **General best practices** distilled from the canonical sources (Simon Peyton Jones,
   Jennifer Widom, Farquhar/Foerster, Steinhardt, Zobel, Lipton & Steinhardt, the NeurIPS
   checklist, Parikh's rebuttal guide).
2. **A specific "house style"** — the conventions used consistently by Tianyi Chen and
   collaborators (Lisha Chen, Quan Xiao, Liuyuan Jiang) across bilevel-optimization and
   multi-objective-learning papers. Match this when the user is in that group or wants that
   style.

The detailed material lives in `references/` and is loaded on demand. **Read the relevant
reference file(s) before drafting** — do not write from memory of this overview alone.

## First, establish the brief

Before drafting anything, confirm (ask only what you can't infer):

- **Venue & format** — journal vs. conference; page limit (~5, ~10, journal-length); single
  vs. double column; theory-heavy vs. experiment-heavy.
- **The one idea ("ping")** — the single reusable insight the paper delivers. If there are
  several, the paper likely should be split.
- **Contributions** — draft these as a refutable bulleted list *first*; they drive the
  whole paper.
- **Style target** — generic best-practice, or the group "house style"?

## Router — which reference to read

| If the user wants to…                                  | Read |
|--------------------------------------------------------|------|
| Understand overall principles / start from scratch     | `references/general-principles.md` |
| Match the Chen-group conventions & notation            | `references/house-style.md` |
| Write/fix the **abstract** or **introduction**         | `references/abstract-and-intro.md` (+ house-style) |
| Write **theorems, assumptions, proofs**, complexity    | `references/theory-writing.md` |
| Write the **experiments / results** section            | `references/experiments.md` |
| Final pass before submission                           | `references/checklists.md` |
| Write a **rebuttal / response to reviewers**           | `references/rebuttals.md` |

Then layer the **paper-type playbook** for the target format:

| Target format                                          | Playbook |
|--------------------------------------------------------|----------|
| Theoretical **journal** (JMLR, Math. Prog., IEEE TSP)  | `references/paper-types/journal-theoretical.md` |
| ~10-page **theoretical** conference (NeurIPS/ICML/ICLR)| `references/paper-types/conference-theoretical-10page.md` |
| ~10-page **experimental** conference                   | `references/paper-types/conference-experimental-10page.md` |
| ~5-page **short** conference (ICASSP/EUSIPCO/workshop)  | `references/paper-types/conference-short-5page.md` |

A typical request reads **one paper-type playbook + one or two topic references**. Example:
"help me write the intro for my NeurIPS bilevel paper" →
`paper-types/conference-theoretical-10page.md` + `abstract-and-intro.md` + `house-style.md`.

## Default writing workflow

1. **Brief** — pin down venue/format, the one idea, and the contributions list.
2. **Read** the routed reference(s) before drafting.
3. **Outline contributions first**, then build the section skeleton from the paper-type
   playbook; assign each contribution to a section it forward-references.
4. **Draft top-down**: abstract → intro (problem-by-example + contribution bullets) →
   formulation → method/algorithm → theory → experiments → related work (later) →
   conclusion.
5. **Self-review** against `references/checklists.md`; cut filler ("first cut words, later
   cut sentences and subsections"); read aloud.

## Cross-cutting principles (always apply)

- **One ping.** Exactly one clear, reusable idea, stated 100% explicitly.
- **Contributions are refutable** and forward-reference their section ("We *prove* X
  (Section 4)", not "We *study* X").
- **Intuition before formalism.** Examples then the general case; the most direct route to
  the idea, not your discovery journey.
- **Related work comes later**, organized by theme/"the diff", and is generous to others.
- **Theory before experiments** in both the abstract and the body (group convention).
- **Few theorems** (ideally 1, rarely >3); state full assumptions inside each theorem.
- **No "mathiness."** Every theorem must convey real insight, not impress.
- **No "the rest of the paper is organized as follows."** Use forward references instead.

## Honesty about provenance

The references paraphrase and templatize the source papers and guides — they do **not**
reproduce verbatim text. When ghost-writing in the house style, generate fresh prose that
follows the *patterns*; never paste sentences from the group's published papers.
