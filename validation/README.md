# Validation of AI-Generated Responses 
## ***Update
<b>As of 7/28/2026, a sample of the information generated within the knowledge base has been chosen for evaluation.</b>
<ul>
  <li>5% (~2) of randomly selected biomarker pages</li>
  <ul><li>egf.md</li><li>d-dimer.md</li></ul>
  <li>10% (~5) of non-biomarker-related wiki pages (coming soon)</li>
  <ul><li>pas-coagulation-markers.md</li><li>tersigni-et-al-2024-syncytiotrophoblast-extracellular-vesicles-previa-pas.md
</li><li>index.md</li><li>pas-maternal-and-neonatal-outcomes.md</li><li>trophoblast-invasion.md</li></ul>
  <li>25% (~270 lines) of YAML file (coming soon)</li>
  <ul><li> sources (lines 107-243)</li><li>biomarkers (lines 646-771)</li><li>Total: 271 lines</li></ul>
</ul>

### Results

| Page | PASS/FAIL | Cumulative Score |
|------|-----------|------------------|
|egf.md| A: FAIL; B: PASS     |A: 24; B: 42 | 
|d-dimer.md |A: PASS; B: FAIL| A: 48; B: 35; |
|pas-coagulation-markers.md ||
|tersigni-et-al-2024-syncytiotrophoblast-extracellular-vesicles-previa-pas.md | |
|pas-maternal-and-neonatal-outcomes.md | | | 
|index.md | | |
|trophoblast-invasion.md | | |
|biomarker-knowledge-base.yaml lines 107-243 | ||
|biomarker-knowledge-base.yaml lines 646-771 || |

As our research is preliminary, and due to time constraints, we believe this sample is adequately representative of the information contained within the entire knowledge base and is sufficient for the scope of this study. 
<br><br>
Validation reports regarding the results of these evaluations can be found within this folder, named correspondingly:
<ul><li>egf-2026-07-23.md</li>  <li>d-dimer-2026-07-23.docx</li> </ul>
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
