# Abstract & Introduction Templates

The abstract and intro are where referees decide accept/reject. Get them right first. Pair
this with `house-style.md` if writing in the group style.

---

## Abstract — fill-in-the-blank (≈4–6 sentences, one paragraph)

```
[1 — Context/importance] <Paradigm> is a <one-line characterization> that arises in
<application domain>.
[2 — Gap] However, existing <methods/analyses> <concrete limitation: e.g. require nested
loops / Hessian-vector products / restrictive assumption X>.
[3 — Proposal] In this paper, we propose <ACRONYM>, a <key property> method that
<core mechanism>.
[4 — Theory guarantee] We prove that <ACRONYM> <achieves rate / attains property>
under <named assumption>.
[5 — Evidence] Experiments on <benchmarks> show <single most remarkable number / outcome>.
```

Rules:
- Theory claim **before** the experimental claim (group convention; also fine generally for
  theory papers).
- Include your single best number if empirical.
- Open with a statement everyone accepts, end with the surprising payoff.
- One coined acronym, expanded once.
- Journal: add a `Keywords:` line.

### Worked skeleton (bilevel, paraphrased pattern — write fresh prose)
> *Bilevel optimization, a hierarchical paradigm, underlies meta-learning, hyperparameter
> optimization, and LLM fine-tuning. However, most methods rely on Hessian-vector products
> or nested loops that scale poorly. In this paper, we propose XYZ, a single-loop,
> Hessian-free algorithm based on a penalty reformulation. We prove XYZ converges to an
> ε-stationary point in O(ε^{-1.5}) iterations under a relaxed flatness condition.
> Experiments on data hypercleaning and hyper-representation match or beat second-order
> baselines at a fraction of the cost.*

---

## Introduction — structure (~1 page)

Two jobs: **describe the problem** and **state contributions**. Follow this paragraph plan,
which fuses Widom's five questions with the house-style flow:

1. **¶1 — Problem & paradigm, by example.** Define the paradigm in one sentence, then the
   **application litany with citation clusters**. Make the problem concrete; avoid the
   molehill opening.
2. **¶2 — Formulation.** Introduce the main problem as **Eq. (1)** with objective
   signatures inline. Establish the few symbols the intro needs.
3. **¶3 — Why it's hard / why prior work falls short.** Present the **two-camp taxonomy**
   of existing approaches and the limitation each camp has (Widom Q3 & Q4).
4. **¶4 — The research question & our answer.** Pose the *italicized question*; answer
   "affirmative"; give the **best-of-both-worlds** positioning and the one-line idea.
5. **¶5 — Contributions** (often a `§1.1 Our main results` subsection): a refutable
   bulleted list, each bullet forward-referencing its section. Optionally a separate
   **T1/T2 technical-challenges** list.

### Contribution-bullet template

```
Our contributions are summarized as follows.
- **C1 (Reformulation).** We show <problem> admits a penalty reformulation with
  <property> (Section 3).
- **C2 (Algorithm).** We propose <ACRONYM>, a <key property> method requiring only
  <cost> per step (Algorithm 1, Section 4).
- **C3 (Theory).** We prove <ACRONYM> attains <rate> under <named assumption>
  (Theorem 1, Section 5).
- **C4 (Experiments).** On <benchmarks>, <ACRONYM> <quantified outcome> (Section 6).
```

Each bullet:
- Starts with a **refutable verb** (prove/establish/show/propose), not "study/explore".
- **Forward-references** a section, theorem, or algorithm.
- Is one line (single column) or ≤two lines (double column).

### Technical-challenges template (optional, group style)
```
Technically, we overcome the following challenges.
- **T1.** <why the natural approach fails / what makes the analysis non-trivial>.
- **T2.** <second obstacle and the idea that resolves it>.
```

---

## Figure 1

Plan **Figure 1 as the most-read object in the paper**: a method cartoon, the Pareto
front, or the loss landscape that conveys the idea at a glance. Place it top of page 1–2.
Vector/PDF, fully labeled, legible in grayscale. Reference it in ¶1 or ¶4.

---

## Filler to cut

Delete on sight; they signal weak writing and waste page budget:
- "increasingly important", "has attracted much attention/recent interest"
- "with the rapid development/rise of …"
- "in today's world", "plays a vital/crucial role"
- "the rest of this paper is organized as follows" (use forward references)
- nonreferential "this/that/it" (name the noun)
- "etc.", "and so on", "for various reasons" (give the reasons)
- nominalizations: "perform an analysis of" → "analyze", "make a comparison" → "compare"

---

## Self-check

- Can a reader state your one idea after reading only the intro?
- Is every contribution refutable and forward-referenced?
- Does the intro answer all five Widom questions?
- Is there a concrete example, not just generalities?
- Did you defer related-work detail to its own (later) section?
