# Validation Report: pas-coagulation-markers.md

**Validated against**: `medi-105-e48810.pdf` (Gao, Yang et al. 2026), `12884_2024_Article_7065.pdf` (Jiang, Qu et al. 2024), `s12884-023-05784-2.pdf` (Zhou, Yu et al. 2023) — Accuracy/Clarity/Falsity use sources only. Relevance/Completeness additionally draw on `PAS_Previa_Union_Baseline.docx`.

**Methodology**: `VALIDATION.md` rubric — 5 categories (Accuracy, Relevance, Clarity, Completeness, Falsity) × 4 prompting styles (Contextual, Non-contextual, Argumentative, Querying) = 20 cells per response. Each cell scored 1–3; category verdict = PASS if the 4 cells sum to ≥8. Every pass is blind — derived independently, with no cross-referencing of other cells, categories, responses, or documents. Below, each cell lists its method, its key finding, and its score — condensed from the full session record, but with no finding dropped.

**Page split into five responses** (originally four; C was further divided to keep D under the ~150-word cap):
- **Response A** — Summary + D-dimer/fibrinogen study population (sources: all three PDFs)
- **Response B** — 2nd/3rd-trimester Findings table, biphasic explanation, regression paragraph (source: `medi-105-e48810.pdf`)
- **Response C** — Severity-subgroup finding + Diagnosis and design (source: `medi-105-e48810.pdf`)
- **Response D** — tPA and PAI1-tPA complex, tissue validation (source: `s12884-023-05784-2.pdf`)
- **Response E** — Antithrombin III and PAI-1 (source: `12884_2024_Article_7065.pdf`)

Validated 2026-07-28 (Response A), 2026-07-29 (Responses B–D), and 2026-07-30 (Response E).

---

## Response A

> "Coagulation/fibrinolysis proteins — D-dimer, fibrinogen, antithrombin III, and PAI-1 — are dysregulated in PAS, with D-dimer and fibrinogen showing a distinctive biphasic (2nd- vs. 3rd-trimester) pattern and, combined with 3D Doppler ultrasound, the single best diagnostic model found across this wiki's corpus.
>
> Measured at two gestational-age windows in a cohort where all subjects already have "pernicious placenta previa" (PPP) — placenta previa plus a prior cesarean scar — as the inclusion criterion; PAS is assessed as a complication superimposed on this previa population, comparing PAS-complicating-PPP (n=66) against PPP-without-PAS (n=34)."

### Accuracy — 8/12 PASS

| Style          | Prompt                                                                                                                                            | Finding                                                                                                                                                                                                                                                                                       | Score |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| Contextual     | Act as an experienced evaluator. Use the comparison material to determine how accurately information was portrayed in pas-coagulation-markers.md. | "Biphasic" is applied to both D-dimer and fibrinogen, but the source shows D-dimer only rises monotonically (elevated → further elevated); only fibrinogen reverses (elevated → decreased). Antithrombin III/PAI-1 dysregulation, AUC 0.952, and the PPP n=66/34 split all check out exactly. | 2     |
| Non-contextual | Determine the accuracy of pas-coagulation-markers.md.                                                                                             | Definitional/terminology-precision check against the Abstract's exact wording confirms the same biphasic mischaracterization; every other term (coagulation/fibrinolysis proteins, AUC, cohort definition) matches precisely.                                                                 | 2     |
| Argumentative  | Assuming there are information accuracy mistakes in pas-coagulation-markers.md, find all instances of this.                                       | Strict-definitional stress test: "biphasic" requires a direction reversal, not just a magnitude change. D-dimer fails this test (progressive/monophasic); fibrinogen passes. All other claims re-verified against freshly re-quoted text.                                                     | 2     |
| Querying       | How many accuracy mistakes are present in pas-coagulation-markers.md?                                                                             | Atomic-claim table (6 claims): only "D-dimer shows a biphasic pattern" is False; "combined model reaches AUC 0.952" is True but underspecified (doesn't name the trimester); everything else True.                                                                                            | 2     |

### Relevance — 8/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as an experienced evaluator. Use the comparison material to determine how relevant pas-coagulation-markers.md is. | Cross-checked against the baseline: it groups PAI-1 under angiogenesis (§2.3), not coagulation (§2.9) as this page does; D-dimer, fibrinogen, and "PPP" don't appear anywhere in the baseline's biomarker sections at all — suggesting this page's central content is newer/paper-specific rather than established consensus. | 2 |
| Non-contextual | Determine the relevance of pas-coagulation-markers.md. | Baseline emphasizes combined-marker superiority (§3.7) — matches Response A's framing — but always pairs that point with a validation-status caveat absent from this passage; baseline's clinical-actionability framing (§6, why detection matters) isn't connected to Response A's population description. | 2 |
| Argumentative | Assuming there are scope changes in pas-coagulation-markers.md, find all instances of this. | Lexical/quantifier analysis: "dysregulated in PAS" is stated before the PPP-only population is revealed (scope-expansion via ordering); antithrombin III/PAI-1 claims carry the same confidence as the directly-measured D-dimer/fibrinogen claims despite resting on a secondary citation chain (Shainker, not in `raw/`). | 2 |
| Querying | How many relevance inconsistencies are present in pas-coagulation-markers.md? | Boundary-testing each claim standalone found 3 inconsistencies: "dysregulated in PAS" reaches broader than the PPP-only cohort tested; antithrombin III/PAI-1's secondary-citation status isn't distinguished from primary-sourced claims; "best model across this wiki's corpus" is only verified against the 3 sources cited on this page, not the whole wiki. | 2 |

### Clarity — 6/12 FAIL

| Style          | Prompt                                                                                                                       | Finding                                                                                                                                                                                                                                                                                                         | Score |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| Contextual     | Act as an experienced evaluator. Look for ambiguity or unclearness that could mislead readers of pas-coagulation-markers.md. | Opening sentence overloads three ideas (protein list, D-dimer/fibrinogen pattern, combined-model superlative) into one clause with no topic-shift signal; "the single best diagnostic model" has no established referent — no model has been named yet in this passage.                                         | 2     |
| Non-contextual | Determine the clarity of pas-coagulation-markers.md.                                                                         | Read-aloud test: four technical terms precede the sentence's main verb (long subject-to-verb delay); the entire second paragraph is one semicolon-joined sentence carrying the heaviest prosodic load found anywhere in this validation project.                                                                | 1     |
| Argumentative  | Assuming there are clarity errors in pas-coagulation-markers.md, find all instances of this.                                 | Reader-comprehension quiz: "which markers does biphasic apply to" is answerable clearly, but "does the two-gestational-window design apply to all four markers or just some" is not — the paragraph break never signals that antithrombin III/PAI-1 come from an entirely different study design.               | 2     |
| Querying       | How many ambiguous or other clarity issues are present in pas-coagulation-markers.md?                                        | Plain-language translation test: translating forces guesses at what "the single best model" refers to and what was "measured"; "PAS-complicating-PPP" carries a genuine parsing-ambiguity risk (participle vs. clause reading); the second paragraph needed splitting into four sentences to translate cleanly. | 1     |

### Completeness — 4/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as an experienced evaluator. Use a list of facts contained in the comparison material to identify how many are missing from pas-coagulation-markers.md. | Fact-checklist against sources + baseline: 4 of 12 facts present (33%). Missing: single-center design, sample-size justification, baseline-comparability data, clinical-outcome differences, the secondary-citation caveat, mechanistic rationale, inflammatory-ratio context, and the field-wide validation caveat. | 1 |
| Non-contextual | Determine the completeness of pas-coagulation-markers.md. | A fresh checklist on clinical-practice/risk-factor connections: 3 of 7 present (43%). Missing explicit clinical-utility framing, the specific clinical decisions this could inform (delivery timing, surgical approach), fit with current guidelines, and connection to established risk-factor literature. | 1 |
| Argumentative | Assuming there is missing information in pas-coagulation-markers.md, find all instances of this. | Checklist mining the Discussion's mechanism, Limitations, and the baseline's imaging section: 2 of 6 present (33%). Missing the paper's own mechanistic explanation (microthrombosis/hyperfibrinolysis vs. factor consumption), stated limitations (small percreta subgroup, 2nd/3rd-tri-only sampling), and the broader Doppler-feature framework. | 1 |
| Querying | How many completeness gaps are present in pas-coagulation-markers.md? | Holistic proportional read of the whole source: only ~17% of relevant background/design content is represented — motivational/mechanistic content is entirely absent, and most design details (single-center, date range, sample-size specifics, inclusion/exclusion criteria) are missing. | 1 |

### Falsity — 8/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as an experienced evaluator. Use the comparison material to identify false information that could be hallucinations in pas-coagulation-markers.md. | Necessary-condition test: "biphasic" requires a direction reversal; D-dimer's own reported values (elevated → further elevated) directly contradict this, crossing from imprecision into a genuine hallucination. AUC/cohort claims unaffected. | 2 |
| Non-contextual | Determine the falsity of pas-coagulation-markers.md. | Source-triangulation across every location: D-dimer's monotonic trajectory is confirmed consistent across both the Abstract and Figure 1's caption — two independent locations reinforcing the same mischaracterization; AUC 0.952 confirmed across 5 locations. | 2 |
| Argumentative | Assuming there are hallucinations in pas-coagulation-markers.md, find all instances of this. | Hypothetical-fabrication test re-quoting source text fresh: the same single fabrication is confirmed (biphasic/D-dimer); dysregulation, AUC, and cohort claims are all directly supported. | 2 |
| Querying | How many false or hallucinated statements are present in pas-coagulation-markers.md? | Plain-restatement test: restating "D-dimer changes in two opposite phases" fails against the source's monotonic values; the fibrinogen, AUC, and cohort restatements all hold. | 2 |

**Central defect**: the Summary sentence applies **"biphasic"** jointly to D-dimer and fibrinogen, but only fibrinogen's trajectory actually reverses direction. This was independently confirmed as a genuine mischaracterization — not a mere imprecision — across four different Accuracy methods and reconfirmed under Falsity (one confirmed hallucination; everything else, including the exact AUC 0.952 figure and the PPP cohort/n-count definitions, checked out).

---

## Response B

> "2nd trimester: D-dimer elevated (AUC 0.784, sens 72.73%, spec 76.47%); Fibrinogen elevated (AUC 0.739, sens 66.67%, spec 70.59%); 3D Doppler VFI (best single index) AUC 0.826; Combined model AUC 0.888, sens 81.82%, spec 87.88%. 3rd trimester: D-dimer further elevated (AUC 0.839, sens 78.79%, spec 79.41%); Fibrinogen reversed — significantly decreased vs. control (AUC 0.792, sens 72.73%, spec 76.47%); VFI AUC 0.902; Combined model AUC 0.952 (95% CI 0.91–0.99), sens 90.91%, spec 91.18%.
>
> The fibrinogen reversal is a biphasic pattern, not a contradiction — reflecting an evolving coagulation-fibrinolysis imbalance as PAS progresses. In multivariable logistic regression, D-dimer, fibrinogen (inverse direction), VI, and VFI were all independent predictors; FI was not."

### Accuracy — 12/12 PASS (perfect)

| Style          | Prompt                                                                                                                | Finding                                                                                                                                                                                                                                                                  | Score |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----- |
| Contextual     | Use the comparison material to identify accuracy mistakes in pas-coagulation-markers.md.                              | Claim-by-claim check against Table 3/4: all 10 discrete claims (AUC/sens/spec at both timepoints, the fibrinogen-scoped biphasic framing, the full regression outcome) verified exact.                                                                                   | 3     |
| Non-contextual | Ascertain the accuracy of pas-coagulation-markers.md.                                                                 | Internal-consistency check: every sens/spec pair back-calculates to a clean integer patient count (no fractional-patient impossibilities); AUC and direction-of-change move independently and sensibly; no cross-contamination with Zhou/Yu's separate regression model. | 3     |
| Argumentative  | Find all instances of information accuracy mistakes in pas-coagulation-markers.md and argue for/against its accuracy. | Maximally adversarial re-testing of every phrase, including "not a contradiction" (a defensible synthesis of the source's own "progressive imbalance" language, not an invented claim) — nothing broke after genuinely trying.                                           | 3     |
| Querying       | What is the accuracy of pas-coagulation-markers.md?                                                                   | Exhaustive enumeration of all 32 discrete atomic assertions — all 32 verified true; Response B correctly scopes "biphasic" to fibrinogen alone, avoiding Response A's error.                                                                                             | 3     |

### Relevance — 8/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Use the comparison material to determine how relevant pas-coagulation-markers.md is. | The baseline's Doppler section names only qualitative signs, never quantitative indices like VI/FI/VFI, and its coagulation section doesn't describe any trimester-specific fibrinogen reversal — Response B's quantitative layer is newer/paper-specific content beyond the general-consensus baseline. | 2 |
| Non-contextual | Ascertain the relevance of pas-coagulation-markers.md. | Baseline's biomarker literature centers on first-trimester single-timepoint screening; Response B's 2nd-vs-3rd-trimester dynamic-monitoring paradigm sits outside that dominant framing — though its individual-then-combined structure closely matches the baseline's own stated diagnostic-integration principle (§3.7). | 2 |
| Argumentative | Find all instances of scope changes in pas-coagulation-markers.md and argue for/against its relevance. | "Not a contradiction" pre-emptively rebuts an objection the source itself never raises (Gao/Yang never frames the fibrinogen reversal as needing defense) — a modest scope expansion from relaying source content into interpretive commentary, though the underlying substance remains faithfully grounded. | 2 |
| Querying | What is the relevance of pas-coagulation-markers.md? | Audience-fit test: the AUC/sensitivity/specificity and regression breakdown serve a clinician-reader's core question well, but actual cutoff concentration values (needed to act on the numbers clinically) are never reported, despite the source confirming cutoffs were determined via Youden index. | 2 |

### Clarity — 6/12 FAIL

| Style          | Prompt                                                                                                | Finding                                                                                                                                                                                                                                                                                                    | Score |
| -------------- | ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| Contextual     | Look for ambiguity or unclearness that could mislead readers of pas-coagulation-markers.md.           | Paragraph 1 is a dense semicolon-joined list acting as one sentence; "Combined model" never clarifies its own scope (the Findings list names only 3 items, but the actual model also incorporates VI and FI); VI and FI are used in the regression sentence without ever being introduced.                 | 1     |
| Non-contextual | Ascertain the clarity of pas-coagulation-markers.md.                                                  | Plain-language rewrite test: "(best single index)" breaks the list's grammatical parallelism with an unscoped superlative; "reversed" carries a live lexical ambiguity (direction-change vs. retraction) before self-correcting; "biphasic" and "independent predictors" are both used without definition. | 1     |
| Argumentative  | Find all instances of clarity errors in pas-coagulation-markers.md and argue for/against its clarity. | Divergent-reader simulation: a clinician wants an actionable cutoff value the passage never gives; a statistically-minded reader can't tell whether the 2nd- and 3rd-trimester combined models are the same fitted equation or two separately fitted ones — a materially different claim either way.       | 1     |
| Querying       | What is the clarity of pas-coagulation-markers.md?                                                    | Quantifier/precision audit: "significantly decreased" carries no p-value/CI even as an explicit CI sits a few words away for the combined model; "best single index" never states its comparison set; "independent predictors" and "combined model" read as contradictory outside statistical training.    | 2     |

### Completeness — 5/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Use the comparison material to identify how many key facts or information were included in pas-coagulation-markers.md. | Fact-list against the source: missing 95% CIs for every individual marker (only the combined model's CI is given), individual performance data for VI/FI, and the source's own "no single parameter was sufficiently robust for standalone clinical diagnosis" caveat. | 2 |
| Non-contextual | Find and explain the completeness score of pas-coagulation-markers.md. | Section-coverage mapping against the source's own structure: qualitative performance labels ("good"/"excellent"), the cross-sectional-vs-longitudinal framing, and the rationale for why combination improves performance are all present in the source's own organization but absent here. | 1 |
| Argumentative | Act as a critic and expose all instances of missing information that weaken pas-coagulation-markers.md using the comparison material. | Reader-task simulation: omitting the external-validation caveat risks a reader overstating confidence in the reported AUCs; omitting the bleeding-risk clinical rationale leaves the numbers without practical motivation. | 1 |
| Querying | How incomplete is pas-coagulation-markers.md compared to its comparison material? | Proportional-emphasis audit: the source devotes ~30% of its relevant text to mechanism and ~15% to clinical rationale/caveats; Response B reduces mechanism to one clause and omits rationale/caveats (0%) entirely, while over-representing raw numbers. | 1 |

### Falsity — 12/12 PASS (perfect)

| Style          | Prompt                                                                                                                | Finding                                                                                                                                                                                                                                                                           | Score |
| -------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| Contextual     | Use the comparison material to identify false information that could be hallucinations in pas-coagulation-markers.md. | Exhaustive numeric cross-verification against Table 3/4 and the Discussion narrative: every claim traces exactly, including the biphasic/mechanism language and the regression outcome.                                                                                           | 3     |
| Non-contextual | Ascertain the falsity of pas-coagulation-markers.md.                                                                  | Cross-location triangulation (Abstract, Table, Results text, Figure captions): every figure checked is consistent across every location it appears, including a source-internal figure-panel discrepancy that Response B avoids by following the dominant textual/tabular values. | 3     |
| Argumentative  | Find all instances of hallucinations in pas-coagulation-markers.md and argue for/against its falsity.                 | Adversarial steelman targeting "best single index" specifically: VFI's AUC is genuinely the highest of all individual markers at both timepoints, so the claim survives even the harshest test.                                                                                   | 3     |
| Querying       | What is the falsity of pas-coagulation-markers.md?                                                                    | Necessary-condition falsification test applied to every discrete claim: no falsifying condition holds for any of them.                                                                                                                                                            | 3     |

---

## Response C

> "In a 3rd-trimester severity subgroup analysis, D-dimer was highest in percreta and lowest in accreta, while fibrinogen showed the opposite pattern.
>
> **Diagnosis and design**: Previa confirmed by transvaginal 3D ultrasound; PAS reference standard is intraoperative findings and/or postoperative histopathology based on depth of villous invasion. Prospective cohort, formal a priori sample-size calculation (target AUC 0.90, 90% power, minimum 87 needed, 100 enrolled after a 10% dropout buffer). The authors explicitly flag as a limitation that "the combined diagnostic model was developed and evaluated within the same cohort," meaning no external validation has yet been performed."

### Accuracy — 9/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as a fact-checker and determine the accuracy of pas-coagulation-markers.md. | Fact-checker claim-by-claim verification: every discrete claim (severity ordering, ultrasound/histopathology reference standards, sample-size figures, the verbatim-quoted limitation) traces precisely to the source, with only minor defensible paraphrase. | 3 |
| Non-contextual | Accuracy: pas-coagulation-markers.md? | Terminology-substitution audit: "postoperative histopathology" is verbatim source language (stronger fidelity than initially assumed); but the severity-subgroup analysis is presented without the source's own "exploratory" qualifier, overstating its evidentiary weight. | 2 |
| Argumentative | Expose all errors that negatively affect the accuracy score of pas-coagulation-markers.md. | Implied-claim audit: juxtaposing the subgroup finding next to the "formal a priori" sample-size sentence implies shared statistical rigor the source doesn't extend to the subgroup analysis; "highest in percreta...lowest in accreta" linguistically collapses a three-category comparison (increta sits between) into an apparent two-group one. | 2 |
| Querying | Are there misinterpreted or misrepresented facts or data included in pas-coagulation-markers.md? | Attribution audit: every claim is tied to the correct stage/group except the AUC-0.90 sample-size target, which is stated without specifying it's for the combined model specifically. | 2 |

### Relevance — 8/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as a researcher and determine the relevance of pas-coagulation-markers.md. | Purpose-alignment test: the severity finding and external-validation caveat are squarely relevant (the baseline itself treats validation status as central to biomarker-utility assessment); the granular sample-size figures (exact N, dropout %) drift toward methodological trivia not clearly tied to clinical utility. | 2 |
| Non-contextual | Relevance: pas-coagulation-markers.md? | Counterfactual-removal test: the reference-standard sentence and severity finding are necessary for interpreting the page's AUC claims; the previa-ultrasound-confirmation sentence is removable without loss (it's about previa ascertainment, not the coagulation markers). | 2 |
| Argumentative | Expose all discrepancies that negatively affect the relevance score for pas-coagulation-markers.md. | "Wrong home" test: the previa-confirmation and generic reference-standard sentences arguably belong on a previa/PAS-overview page rather than a coagulation-markers page, though a self-contained-context justification partly offsets this. | 2 |
| Querying | Is there scope-related creep noticeable in statements included in pas-coagulation-markers.md? | Specificity-gradient audit: the severity finding and validation caveat score high on relevance to coagulation markers specifically; the previa-confirmation sentence, reference-standard sentence, and sample-size figures all score low — generic PAS/previa methodology, not marker-specific content. | 2 |

### Clarity — 4/12 FAIL (lowest score on the page)

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as an editor and determine the clarity of pas-coagulation-markers.md. | Editorial read: percreta/accreta staging is used without explanation and requires inferring fibrinogen's reversed order; the previa-vs-PAS diagnostic standards are merged with no signposted relationship; the sample-size sentence is a verb-less fragment; the closing clause blurs whose voice is interpreting the quoted limitation. | 1 |
| Non-contextual | Clarity: pas-coagulation-markers.md? | Read-aloud/prosody test: the subject is delayed several words behind its modifier; "percreta"/"accreta" are phonetically near-identical when spoken; the sample-size parenthetical strips numeric anchors, making referent-tracking by ear difficult. | 1 |
| Argumentative | Expose all unclearness that negatively affects the clarity score for pas-coagulation-markers.md. | Naive-reader belief-tracking: no severity ordering is established before percreta/accreta appear; the previa sentence arrives with no signaled topic shift from PAS severity; the sample-size sentence builds unearned confidence that the following limitation sentence then silently reverses. | 1 |
| Querying | Are there ambiguous, un-concise, or confusing statements in pas-coagulation-markers.md? | Conciseness/redundancy audit: "and/or" in the reference-standard definition is genuinely ambiguous; "based on depth of villous invasion" has an unresolved attachment; "formal a priori" and "explicitly flag" both pair a strong term with a redundant intensifier. | 1 |

### Completeness — 4/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as a cross-checker and verify that pas-coagulation-markers.md is complete. | Cross-checker fact-audit: missing the companion null finding that Doppler indices showed no significant severity difference (only coagulation markers did), the 2nd-trimester null finding for the same analysis, the "exploratory" label, study site/dates, full eligibility criteria, and detailed sample-size parameters (α, case:control ratio). | 1 |
| Non-contextual | Completeness: pas-coagulation-markers.md? | Reader-question test: missing why the percreta subgroup's small size should temper confidence (the source's own stated caveat), the source's forward-looking external-validation research plan, and the baseline's rationale for why previa triggers PAS screening at all. | 1 |
| Argumentative | Expose all instances of missing information that weaken pas-coagulation-markers.md using the comparison material. | Materiality-weighted argument: the source's own limitation about the small percreta-subgroup size directly undermines the very finding this response leads with — a self-undermining omission, the most serious of several candidates weighed. | 1 |
| Querying | How incomplete is pas-coagulation-markers.md compared to its comparison material? | Quantitative coverage count: 14 of 34 enumerated relevant facts present (~41%), including all five of the source's stated study strengths and three of its four stated limitations missing entirely. | 1 |

### Falsity — 12/12 PASS (perfect)

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as a detective and find hallucinations in pas-coagulation-markers.md. | Detective investigation: every claim — severity ordering, both diagnostic standards, all five sample-size figures, the verbatim limitation quote — traces cleanly with nothing invented. | 3 |
| Non-contextual | Falsity: pas-coagulation-markers.md? | Cross-location triangulation: the severity-subgroup finding is independently corroborated across Results text, the Discussion, and Figure 2's caption/rendered bar values; sample-size figures corroborate across Methods and Results. | 3 |
| Argumentative | Expose all hallucinated false information that weaken pas-coagulation-markers.md using the comparison material. | Adversarial steelman targeting the merged reference-standard sentence and the "100 enrolled after dropout" phrasing: both are compressions of adjacent source sentences that preserve truth value, not fabrications. | 3 |
| Querying | How false is pas-coagulation-markers.md compared to its comparison material? | Necessary-condition falsification test applied to all nine discrete claims: no falsifying condition holds for any of them. | 3 |

---

## Response D

> "Tissue-type plasminogen activator (tPA) is decreased in PAS vs. preeclampsia (ratio 0.42) in this study's Cohort One; in the independent Cohort Two replication, the same fibrinolysis axis was instead measured as the inactivated PAI1-tPA complex, which was elevated (ratio 1.59, p<0.01) — the reversed direction reflects a different molecular form being measured (free active tPA vs. complexed/inactivated tPA), not a contradiction. Tissue-level IHC/RT-qPCR confirmed tPA (PLAT) expression differs significantly between invasion area, non-implantation area, and normal placenta, concentrated in the non-implantation area. This is a distinct fibrinolysis-axis finding from the D-dimer/fibrinogen/antithrombin-III/PAI-1 markers above, from a different raw/ source."

### Accuracy — 10/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Using the comparison material, critically evaluate how appropriately information was documented in pas-coagulation-markers.md. | Documentation-appropriateness review: every claim — the 0.42 ratio, the 1.59 ratio, the molecular-form distinction, the tissue-localization finding — checks out, with only minor precision notes (the Cohort One attribution doesn't specify the testing-group subdivision; "replication" is the wiki's own reasonable characterization). | 3 |
| Non-contextual | Find and explain the accuracy score of pas-coagulation-markers.md. | Terminology-substitution audit across the full source: "independent" and "free tPA" both turn out to be verbatim source terms (stronger than initially assumed), and "PLAT" and the three placental-region terms map correctly onto the source's own Figure 4 legend. | 3 |
| Argumentative | Act as a critic and expose all accuracy mistakes that weaken pas-coagulation-markers.md using the comparison material. | Charitable-reading test: "Cohort One" generalizes a finding specific to the testing-group sub-analysis (19 PAS vs. 20 PE); "not a contradiction... different molecular form" is framed as though resolving a tension the source itself never raises. | 2 |
| Querying | How inaccurate is pas-coagulation-markers.md compared to its comparison material? | Quantitative deviation measurement: every number matches exactly (0% deviation); the "Cohort One" attribution and the "not a contradiction" framing carry real but bounded scope-generalization and unflagged-synthesis deviations. | 2 |

### Relevance — 8/12 PASS

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Using the comparison material, critically evaluate how faithfully pas-coagulation-markers.md keeps to its scope. | Boundary-testing: four of five components are squarely on-topic (matching wiki precedent for tissue-validation content, e.g. on the EGF page); the closing meta-sentence ("distinct fibrinolysis-axis finding... different raw/ source") is pure navigational commentary with no biomarker content of its own. | 2 |
| Non-contextual | Find and explain the relevance score of pas-coagulation-markers.md. | Counterfactual-removal test: the two ratio findings and the reconciling explanation are all necessary (removing the explanation would let a reader wrongly conclude the two cohorts contradict each other); the tissue-localization data and closing meta-sentence are both removable without loss. | 2 |
| Argumentative | Act as a critic and expose all scope or relevance creeping that weaken pas-coagulation-markers.md using the comparison material. | "Wrong home" test: tissue-localization data could be argued to belong on a general pathophysiology page, but the wiki's own precedent (EGF's page pairs serum data with tissue IHC identically) undercuts that argument — only the meta-sentence remains a clean example of content with no proper home. | 2 |
| Querying | How irrelevant is pas-coagulation-markers.md compared to its comparison material? | Specificity-gradient audit: three of five components score high-to-very-high on relevance to coagulation markers; the tissue-localization data is moderate; the closing meta-sentence is the one clearly low-relevance element. | 2 |

### Clarity — 5/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Using the comparison material, critically evaluate how concisely and unambiguously pas-coagulation-markers.md is written in terms of writing quality. | Close editorial read: the opening sentence packs five propositional units into one semicolon/dash-joined clause; "instead" creates a forward-reference gap before its contrast resolves; "the reversed direction" requires reconstructing two ratios across two cohorts to parse; the closing sentence stacks two unrelated uses of "from" back to back. | 1 |
| Non-contextual | Find and explain the clarity score of pas-coagulation-markers.md. | Read-aloud/prosody test: the full term precedes its own abbreviation; two ratios in a compare/contrast frame risk being transposed when spoken; "PAI1-tPA" is phonetically near-indistinguishable from "PAI-1," a separate entity discussed elsewhere on this same page; "IHC/RT-qPCR" is a dense unspoken acronym pileup. | 1 |
| Argumentative | Act as a critic and expose all clarity concerns that weaken pas-coagulation-markers.md. | Naive-reader belief-tracking: the passage triggers an apparent contradiction (tPA down, then "PAI1-tPA" up) before resolving it several clauses later, rather than heading off the confusion; the serum-vs-tissue relationship between the two halves of the passage is never made explicit. | 2 |
| Querying | Are there ambiguous, un-concise, or confusing statements in pas-coagulation-markers.md? | Direct complexity comparison against the source's own (simpler, separated) presentation of the same two cohort findings: Response D merges what the source keeps as two plain sentences into one compound sentence with an added interpretive layer, measurably increasing complexity relative to its own source. | 1 |

### Completeness — 4/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Using the comparison material, critically evaluate and measure how many key facts or information were included in pas-coagulation-markers.md. | Fact-audit: missing tPA's decrease vs. normal-term controls and vs. placenta previa (only the vs.-preeclampsia ratio given), a second confirmation from the validation group, Cohort Two's limited-sample/different-assay-kit caveat, the serum-vs-plasma equivalence check, the mechanistic hemorrhage-risk link, and the study's stated limitations (single-center, Asian-only, small sample). | 1 |
| Non-contextual | Find and explain the completeness score of pas-coagulation-markers.md. | Reader-question test: missing why tPA is lower across multiple comparator groups (not just PE), how reliable the "replication" cohort actually is, and the clinical/mechanistic significance of the finding. | 1 |
| Argumentative | Act as a critic and expose all instances of missing information that weaken pas-coagulation-markers.md using the comparison material. | Materiality-weighted argument: the missing cross-reference to the Shainker/PAI-1 discussion elsewhere on this same page is the standout omission, compounded by the response's own closing claim of being "distinct" — an assertion of independence the source material itself complicates. | 1 |
| Querying | How incomplete is pas-coagulation-markers.md compared to its comparison material? | Quantitative coverage count: 8 of 17 enumerated facts present (~47%), the best Completeness coverage ratio on the page but still under the 51% threshold. | 1 |

### Falsity — 12/12 PASS (perfect)

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Using the comparison material, critically evaluate and measure how many hallucinations and false statements are present in pas-coagulation-markers.md. | Detective investigation: every ratio, direction, and molecular-form distinction traces exactly to the source, with nothing invented or altered. | 3 |
| Non-contextual | Find and explain the falsity score of pas-coagulation-markers.md. | Cross-location triangulation: every claim is corroborated across every location it appears (Abstract, Methods, Results, Discussion, Figure captions/panels) with no location contradicting another. | 3 |
| Argumentative | Act as a critic and expose all hallucinated false information that weaken pas-coagulation-markers.md using the comparison material. | Adversarial steelman specifically testing whether "the same fibrinolysis axis" invents a link between tPA and PAI1-tPA: it doesn't — PAI-1/tPA complex formation is established fibrinolysis biochemistry the source's own framing directly supports. | 3 |
| Querying | How false is pas-coagulation-markers.md compared to its comparison material? | Necessary-condition falsification test applied to all ten discrete claims: no falsifying condition holds for any of them. | 3 |

---

## Response E

> "This wiki's structured knowledge base (`biomarker-knowledge-base.yaml`) separately documents Antithrombin III (elevated, 240.4 vs. 150.3 mg/L, p=0.002) and PAI-1 (decreased, 4.1 vs. 7.1 ng/mL, p<0.001) from Shainker et al. 2020's plasma proteomics discovery-then-ELISA-validation study. **That paper is not itself present in `raw/`** — it is cited only as background context here, consistent with this wiki's rule of restricting sourced claims to files actually in `raw/`.
>
> A newer paper that *is* in `raw/` independently discusses and corroborates that same Shainker panel: the cervicovaginal-fluid multi-omics study (Jiang, Qu et al. 2024) explicitly names Shainker's four ELISA-validated proteins — antithrombin III, PAI-1, soluble Tie2, and soluble VEGF receptor 2 — when contrasting its own discovery-only design against Shainker's two-phase discovery→validation design (source: 12884_2024_Article_7065.pdf). See [[pas-cervicovaginal-fluid-biomarkers]] for that paper's own (different) biomarker findings."

**Structurally different from A–D**: this is the only response built around a citation chain (this wiki citing Jiang/Qu, which cites Shainker, not in `raw/`) rather than direct primary-source reporting — the source of nearly every defect below.

### Accuracy — 4/12 FAIL

| Style                  | Prompt                                                                                           | Finding                                                                                                                                                                                                                                                                                                                                                      | Score |
| ---------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----- |
| Contextual             | Act as a fact-checker and determine the accuracy of pas-coagulation-markers.md.                  | The four named proteins match the source exactly, but the citation marker is attached to a sentence claiming "ELISA-validation" and a "two-phase discovery→validation design" for Shainker — neither term appears anywhere in Jiang/Qu's paper, whose actual point of comparison in that passage is sample type (CVF vs. blood), not validation methodology. | 1     |
| Non-contextual         | Accuracy: pas-coagulation-markers.md?                                                            | Terminology-substitution audit across the *entire* source (not one passage): confirms "ELISA" appears nowhere in the paper at all, in either its own methods or its citation of Shainker — reinforcing the sourcing problem independently.                                                                                                                   | 1     |
| Argumentative (redone) | Expose all errors that negatively affect the accuracy score of pas-coagulation-markers.md.       | Adversarial charitable-reading test: even the most generous reading of "corroborates" fails, since Jiang/Qu's own results never re-measure any of Shainker's four proteins; the citation-scope convention for the design-contrast claim doesn't rescue it either.                                                                                            | 1     |
| Querying               | Are there misinterpreted or misrepresented facts or data included in pas-coagulation-markers.md? | Attribution audit: the four-protein claim is correctly attributed; the design-contrast claim is misattributed — its content may be true as outside knowledge about Shainker, but it's not supported by *this* citation.                                                                                                                                      | 1     |

### Relevance — 5/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as a researcher and determine the relevance of pas-coagulation-markers.md. | Purpose-alignment test: only the antithrombin III/PAI-1 level data is substantive biomarker-utility content; the wiki's own `raw/`-sourcing-rule sentence, the citation/design-comparison discussion, and the navigational cross-reference are all meta-level content about sourcing policy and paper provenance. | 1 |
| Non-contextual | Relevance: pas-coagulation-markers.md? | Counterfactual-removal test: only one of four components is necessary; the other three (sourcing-rule explanation, citation/design tracking, cross-reference) are all removable without loss to a reader's understanding of these biomarkers' clinical utility. | 1 |
| Argumentative | Expose all discrepancies that negatively affect the relevance score for pas-coagulation-markers.md. | "Wrong home" test: the wiki's own hybrid topic-plus-cross-reference convention (as used everywhere else on this page) justifies keeping antithrombin III/PAI-1 content here; only the narrower design-comparison sub-claim lacks a clearly appropriate home anywhere in the wiki's structure. | 2 |
| Querying (redone) | Is there scope-related creep noticeable in statements included in pas-coagulation-markers.md? | Specificity-gradient audit, evaluated purely on this response's own terms: three of four components carry no substantive coagulation-marker content — the sourcing-policy sentence in particular is a categorically different kind of content, unrelated to PAS or previa biology at all. | 1 |

### Clarity — 4/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as an editor and determine the clarity of pas-coagulation-markers.md. | "Separately documents" has no established point of comparison yet; the numeric parentheticals don't label which figure belongs to which group; "discovery-then-ELISA-validation" is a dense compound requiring active unpacking; the final sentence stacks a colon, an em-dash list, an arrow symbol, and a parenthetical citation in one clause. | 1 |
| Non-contextual | Clarity: pas-coagulation-markers.md? | Read-aloud/prosody test: the filename-with-extension is awkward spoken aloud; two differently-united numeric parentheticals risk blending together by ear; "raw/" jargon repeats twice in one sentence; the arrow symbol ("discovery→validation") has no standard spoken equivalent at all — a hard read-aloud failure, not just a difficulty. | 1 |
| Argumentative | Expose all unclearness that negatively affects the clarity score for pas-coagulation-markers.md. | Naive-reader belief-tracking: the passage's own sequencing produces a **false-reassurance arc** — a reader learns the data isn't traceable to `raw/`, then reads that a newer paper "corroborates" it and reasonably (but wrongly) concludes the uncertainty is resolved, since the newer paper never actually re-confirms anything. | 1 |
| Querying | Are there ambiguous, un-concise, or confusing statements in pas-coagulation-markers.md? | Conciseness/redundancy audit: redundant intensifiers ("itself," "actually," "structured"); a genuine scope-ambiguity in whether "independently" modifies just "discusses" or the whole compound verb including "corroborates"; a confusing near-tautological echo between "discovery-only" and "discovery→validation." | 1 |

### Completeness — 4/12 FAIL

| Style | Prompt | Finding | Score |
|---|---|---|---|
| Contextual | Act as a cross-checker and verify that pas-coagulation-markers.md is complete. | Missing the actual framing rationale for citing Shainker (blood-based vs. CVF-based studies), a second prior study (Afshar et al.) cited in the same source paragraph, Jiang/Qu's own sample size/limitations, and a mechanistic rationale for antithrombin III's elevation from the baseline — plus an unreconciled directional tension (the baseline calls PAI-1 "upregulated," this response calls it "decreased"). | 1 |
| Non-contextual | Completeness: pas-coagulation-markers.md? | Reader-question test: missing why the citation exists at all, how prominent it actually is in the source (one passing sentence, not a major thread), Jiang/Qu's small sample size (n=6 vs. n=6), and whether Jiang/Qu's own results table actually contains any of the four named proteins. | 1 |
| Argumentative | Act as a critic and expose all instances of missing information that weaken pas-coagulation-markers.md using the comparison material. | Materiality-weighted argument: the missing fact that Jiang/Qu's own differential-protein table never includes Shainker's four proteins is the standout omission — it directly undermines the response's own "corroborates" framing, though partly reachable via the page's own cross-reference. | 1 |
| Querying | How incomplete is pas-coagulation-markers.md compared to its comparison material? | Quantitative coverage count: 5 of 13 enumerated facts present (~38%), the lowest coverage ratio on the page. | 1 |

### Falsity — 10/12 PASS

| Style          | Prompt                                                                                                                                                 | Finding                                                                                                                                                                                                                                                                                                                                                                       | Score |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| Contextual     | Using the comparison material, critically evaluate and measure how many hallucinations and false statements are present in pas-coagulation-markers.md. | Detective investigation applying a strict silence-vs-contradiction standard: the four named proteins are confirmed true; "ELISA-validated" and the design-contrast framing are unsupported by silence, not direct contradiction — no hallucination found under this narrower test.                                                                                            | 3     |
| Non-contextual | Find and explain the falsity score of pas-coagulation-markers.md.                                                                                      | Cross-location triangulation: the four-protein claim is corroborated in *two* separate locations in the source (Introduction and Discussion, despite an internal reference-numbering inconsistency in the source itself) — the core fact is even more strongly supported than a single-location check would suggest.                                                          | 3     |
| Argumentative  | Act as a critic and expose all hallucinated false information that weaken pas-coagulation-markers.md using the comparison material.                    | Adversarial steelman using converging evidence not previously combined: both the Abstract's own curated highlights (arginine, GAL7, uPA, MMP9, ITGAM) and the Results' top-20 differential-protein table consistently exclude all four of Shainker's proteins — strong enough to treat "corroborates" as a confirmed hallucination, not just an unsupported characterization. | 2     |
| Querying       | How false is pas-coagulation-markers.md compared to its comparison material?                                                                           | Necessary-condition falsification test: the "corroborates" claim fails (source's own reported significant findings exclude all four proteins, confirmed twice); the ELISA and design-contrast claims remain unproven-but-not-disproven under the same evidentiary standard.                                                                                                   | 2     |

**Falsity is otherwise near-perfect across the page** — this is the only other confirmed hallucination besides Response A's biphasic mislabeling, and it's the more consequential of the two in one respect: the Clarity findings show it actively produces false reader confidence rather than simply omitting information.

---

## Cross-response comparison

| Category     | A          | B           | C           | D           | E          |
| ------------ | ---------- | ----------- | ----------- | ----------- | ---------- |
| Accuracy     | 8 PASS     | **12 PASS** | 9 PASS      | 10 PASS     | **4 FAIL** |
| Relevance    | 8 PASS     | 8 PASS      | 8 PASS      | 8 PASS      | **5 FAIL** |
| Clarity      | 6 FAIL     | 6 FAIL      | **4 FAIL**  | 5 FAIL      | **4 FAIL** |
| Completeness | **4 FAIL** | 5 FAIL      | **4 FAIL**  | **4 FAIL**  | **4 FAIL** |
| Falsity      | 8 PASS     | **12 PASS** | **12 PASS** | **12 PASS** | 10 PASS    |
|              |            |             |             |             |            |
**Verdicts**: A: PASS; B: PASS; C: PASS; D: PASS; E: FAIL

**Patterns across the page:**
- **Clarity fails every single time** (5/5 responses), always for a version of the same underlying problem: one sentence per response carries disproportionate structural load (semicolon/dash-joined compound clauses, undefined abbreviations, verb-less fragments, or — in Response E's case — a symbol with no spoken equivalent), consistently confirmed via at least three independently-derived methods per response.
- **Completeness fails every single time** (5/5 responses), with coverage ratios ranging from ~38% (Response E) to ~53% (Response B, the best performer). The recurring pattern: mechanistic/biological rationale, statistical granularity, and the source papers' own stated limitations are consistently the first things cut.
- **Falsity is otherwise essentially perfect.** Response A has one isolable error (D-dimer/biphasic mislabeling); B, C, D scored a flawless 12/12; Response E is the only other response with a confirmed hallucination ("corroborates"). Across the whole page, exactly two confirmed hallucinations exist, both arising from imprecise characterization rather than invented numbers — this page does not fabricate data values.
- **Relevance and Accuracy are solid for A–D but collapse for E.** Responses A–D all pass both categories comfortably; Response E fails both, and for a related reason — it's the only response built around a citation chain (to a source not in `raw/`) rather than direct primary-source reporting, and that extra layer of indirection is where its accuracy and relevance problems concentrate.
- **The single most consequential defect on the page** remains Response A's "biphasic" mislabeling of D-dimer, since it sits in the page's own Summary line — the most visible sentence on the page.
- **The second most consequential defect** is Response E's "corroborates" claim — the only other confirmed hallucination on the page, and one that actively produces false reader confidence rather than simply omitting information.

## Recommended fixes

1. **Response A summary line**: scope "biphasic" to fibrinogen only; D-dimer's pattern is a monotonic increase, not a reversal.
2. **Response A / all responses' second paragraphs**: break up the long semicolon/dash-joined compound sentences identified in each Clarity section — this is the single highest-yield fix across the page.
3. **Response D closing sentence**: reconsider "distinct fibrinolysis-axis finding" — either soften the claim of independence or add a cross-reference to the Antithrombin III/PAI-1 section, consistent with the source's own Discussion.
4. **Response E**: replace "independently discusses and corroborates" with language reflecting that Jiang/Qu only *cites* Shainker's panel rather than independently confirming it (their own reported significant findings never include these four proteins); remove or re-source "ELISA-validated" and the "two-phase discovery→validation design" characterization, neither of which this citation supports.
5. **Across B, C, D, E**: consider a brief "Limitations" line drawing on each source's own stated caveats (external validation status is already present on this page; sample-size/subgroup-size caveats and single-center/population-generalizability caveats are not).

Final overall PASS/FAIL judgment across all category verdicts is a human call, not made here.
