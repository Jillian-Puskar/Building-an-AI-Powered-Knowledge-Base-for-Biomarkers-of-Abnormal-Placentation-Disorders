# Validation of AI-Generated Responses 
## ***Update
<b>As of 8/03/2026, a sample of the information generated within the knowledge base has been chosen for evaluation.</b>
<ul>
  <li>5% (~2) of randomly selected biomarker pages</li>
  <ul><li>egf.md</li><li>d-dimer.md</li></ul>
  <li>10% (~5) of non-biomarker-related wiki pages (coming soon)</li>
  <ul><li>pas-coagulation-markers.md</li><li>tersigni-et-al-2024-syncytiotrophoblast-extracellular-vesicles-previa-pas.md
</li><li>abnormal-placentation.md</li><li>pas-maternal-and-neonatal-outcomes.md</li><li>trophoblast-invasion.md</li></ul>
  <li>25% (~270 lines) of YAML file (coming soon)</li>
  <ul><li> sources (lines 107-243)</li><li>biomarkers (lines 636-771)</li><li>Total: 271 lines</li></ul>
</ul>

### Results

| Page | PASS/FAIL | Cumulative Score |
|------|-----------|------------------|
|egf.md| A: FAIL; B: PASS     |A: 24; B: 42 | 
|d-dimer.md |A: PASS; B: FAIL| A: 48; B: 35; |
|pas-coagulation-markers.md |A: PASS; B: PASS; C: PASS; D: PASS; E: FAIL |A: 34; B: 43; C: 37; D: 39; E: 27 |
|tersigni-et-al-2024-syncytiotrophoblast-extracellular-vesicles-previa-pas.md |A: PASS; B: FAIL; C: PASS; D: PASS | A: 36; B: 38; C: 37; D: 37|
|pas-maternal-and-neonatal-outcomes.md |A: PASS; B: PASS; C: PASS; D: PASS|A: 42; B: 44; C: 44; D: 39 | 
|abnormal-placentation.md |A: PASS; B: PASS; C: PASS; D: PASS |A: 32; B: 44; C: 40; D: 46|
|trophoblast-invasion.md | Part 1: A: PASS; B: FAIL; Part 2: A: PASS; B: FAIL |Part 1: A: 41; B: 36; Part 2: A: 40; B: 33 |
|biomarker-knowledge-base.yaml lines 107-243 |A: PASS |A: 49|
|biomarker-knowledge-base.yaml lines 636-771 |A: FAIL |A: 34|

As our research is preliminary, and due to time constraints, we believe this sample is adequately representative of the information contained within the entire knowledge base and is sufficient for the scope of this study. 
<br><br>
Validation reports regarding the results of these evaluations can be found within this folder, named correspondingly:
<ul><li>egf-2026-07-23.md</li>  <li>d-dimer-2026-07-23.md</li><li>pas-coagulation-markers-2026-07-29.md</li><li>tersigni-et-al-2024-syncytiotrophoblast-evs-2026-07-31.md</li><li>abnormal-placentation-2026-07-31.md</li><li>pas-maternal-and-neonatal-outcomes-2026-08-03.md</li><li>trophoblast-invasion-2026-08-03.md</li><li>biomarker-knowledge-base-yaml-2026-08-04.md</li></ul>
<br>

## Methodology
Most of our validation methodology and the rubric used to grade responses can be found within "Validation.pdf." 
<br><br>Baselines are located within the "baselines" folder.

### Expansion on prompting types
The following prompting types were used for validation:
<ul><li>Contextual</li>
    <ul><li>Example: "Act as an experienced evaluator. Determine how accurate (using the definition given) the information about the tissue-derived EGF biomarker is, considering the source file."</li></ul>
  <li>Non-contextual</li>
    <ul><li>Example: "Determine how relevant egf.md is to the source." </li></ul>
  <li>Argumentative</li>
    <ul><li>Example: "Assume that there are relevance gaps or discrepancies in d-dimer.md and find examples of them." </li></ul>
  <li>Querying</li>
  <ul><li>Example: "If a reader new to this information read d-dimer.md, would they find ambiguity or poor clarity?"</li></ul>
</ul><br>
