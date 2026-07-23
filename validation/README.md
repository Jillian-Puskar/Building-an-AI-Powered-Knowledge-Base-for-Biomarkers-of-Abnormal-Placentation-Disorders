# Validation of AI-Generated Responses 
## ***Update
<b>As of 7/24/2026, a sample of the information generated within the knowledge base has been evaluated.</b>
<ul>
  <li>10% (~4) of randomly selected biomarker pages</li>
  <ul><li>egf.md</li><li>sflt-1.md</li><li>d-dimer.md</li><li>fibrinogen.md</li></ul>
  <li>5% (~2) of non-biomarker-related wiki pages</li>
  <ul><li>pas-coagulation-markers.md</li><li>tersigni-et-al-2024-syncytiotrophoblast-extracellular-vesicles-previa-pas.md
</li></ul>
  <li>25% (~270 lines) of YAML file</li>
  <ul><li> sources (lines 107-243)</li><li>biomarkers (lines 646-771)</li><li>Total: 271 lines</li></ul>
</ul>

### Results

| Page | PASS/FAIL | Cumulative Score |
|------|-----------|------------------|
|egf.md|          |                  | 
|sflt-1.md|        |                  | 
|d-dimer.md || 
|fibrinogen.md| | 
|pas-coagulation-markers.md ||
|tersigni-et-al-2024-syncytiotrophoblast-extracellular-vesicles-previa-pas.md | |
|biomarker-knowledge-base.yaml lines 107-243 | ||
|biomarker-knowledge-base.yaml lines 646-771 || |

As our research is preliminary, we believe this sample is adequately representative of the information contained within the entire knowledge base and is sufficient for this study. 
<br><br>
Validation reports regarding the results of these evaluations can be found within this folder, named correspondingly:
<ul><li>egf-validation-report.docx</li> <li>sflt-1-validation-report.docx</li> <li>d-dimer-validation-report.docx</li> <li>fibrinogen-validation-report.docx</li> <li>pas-coagulation-markers-validation-report.docx</li> <li>tersigni-et-al-2024-validation-report.docx</li> <li>yaml-part-1-validation-report.docx</li> <li>yaml-part-2-validation-report.docx</li></ul>
<br>

## Methodology
Most of our validation methodology and the rubric used to grade responses can be found within "Validation.pdf." 
<br><br>Baselines are located within the "baselines" folder.

### Expansion on prompting types
The following prompting types were used for validation:
<ul><li>Contextual</li>
    <ul><li>Example: ""</li></ul>
  <li>Non-contextual</li>
    <ul><li>Example:</li></ul>
  <li>Argumentative</li>
    <ul><li>Example:</li></ul>
  <li>Querying</li>
  <ul><li>Example: ""</li></ul>
</ul><br>
