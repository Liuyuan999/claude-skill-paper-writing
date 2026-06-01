# Checklists — Pre-Submission & NeurIPS-Style

Run these before submission. The NeurIPS checklist is mandatory at NeurIPS (papers without
it are desk-rejected) and is a good discipline everywhere.

---

## NeurIPS-style paper checklist (16 categories)

Answer each **yes / no / n/a** with a 1–2 sentence justification that **points to the
supporting section**. A justified "no/n/a" is generally fine.

1. **Claims** — abstract/intro claims match the actual contributions, scope, and
   assumptions; aspirations are distinguished from attained results.
2. **Limitations** — strong assumptions disclosed; robustness to their violation discussed;
   factors affecting performance noted.
3. **Theory (assumptions & proofs)** — the *full* set of assumptions appears in each theorem;
   complete proofs (paper or supplement) with proof sketches and cross-references.
4. **Experimental reproducibility** — a reasonable path to reproduce the main results.
5. **Open access to data & code** — code/data plus exact commands and environment;
   anonymized for submission (encouraged).
6. **Experimental settings/details** — data splits, hyperparameters, and how chosen.
7. **Statistical significance** — error bars / CIs / tests; state what variability they
   capture (std vs. SEM) and how computed.
8. **Compute resources** — hardware type, memory, per-run and total compute (incl. failed
   runs).
9. **Code of ethics** — conforms to the venue's code of ethics.
10. **Broader impacts** — potential negative societal impacts and mitigations.
11. **Safeguards** — for releasing high-risk/dual-use models or scraped data.
12. **Asset licenses** — existing assets credited and licensed correctly.
13. **New assets** — documented (and released where possible).
14. **Crowdsourcing / human subjects** — instructions, consent, fair pay.
15. **IRB / risks** — approval where applicable; risks disclosed.
16. **LLM usage** — declare only if an LLM is a core, original, non-standard component (not
    for writing/editing).

## Generic pre-submission checklist

**Content & framing**
- [ ] One clear "ping" — a reader can state it after the intro.
- [ ] Contributions are a refutable, forward-referenced bulleted list.
- [ ] Intro answers Widom's five questions; opens with a concrete example.
- [ ] Related work is later, thematic, generous, and accurate.
- [ ] Claims in abstract/intro are each backed by evidence in the body.

**Theory**
- [ ] ≤1–3 theorems; one headline result.
- [ ] Full assumptions in each theorem; robustness discussed.
- [ ] Rate/complexity in big-O visible in abstract and theorem.
- [ ] Proof sketch in body, complete proof in appendix; cross-references resolve.
- [ ] Passes the "would I rely on this?" anti-mathiness test.

**Experiments**
- [ ] Each experiment maps to a claim/contribution.
- [ ] Naive + prior + alternative baselines, fairly tuned.
- [ ] Ablations isolate the source of gains.
- [ ] Error bars, compute, and full hyperparameters reported.
- [ ] Every figure described correctly in the text.

**Writing & format**
- [ ] Filler cut; consistent terminology; each term defined once.
- [ ] `\citet` vs. `\citep` used correctly; `\label` after `\caption`.
- [ ] Figures vector/PDF, labeled, grayscale-legible, near first reference.
- [ ] Within the page limit *after* references move to where the format requires.
- [ ] No "the rest of the paper is organized as follows."
- [ ] Spell-checked; read aloud; printed and marked once.

**Logistics**
- [ ] Anonymized (double-blind venues): no author names, no identifying links/acks.
- [ ] Code-availability line present (or justified absence).
- [ ] Checklist / reproducibility statement completed.
- [ ] References complete, with venue and year (not just arXiv) where published.

---

Source: NeurIPS Paper Checklist — https://neurips.cc/public/guides/PaperChecklist
