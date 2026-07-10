# Comparing Adverse Event Profiles: Metformin vs Glipizide

## Motivation
As a pharmacist, I've seen how adverse drug reactions differ across 
medications treating the same condition. This project uses the FDA's 
public adverse event data (openFDA) to quantitatively compare the 
reported side-effect profiles of two common diabetes medications.

## Method
- Pulled adverse event report counts for metformin and glipizide from 
  the openFDA Drug Adverse Event API
- Aggregated the top 10 most frequently reported reactions per drug
- Compared them side by side in a grouped bar chart

## Findings
- Metformin shows substantially higher report counts across most 
  reaction categories, including nausea, drug ineffectiveness, and 
  elevated blood glucose.
- Certain reactions appear prominently in one drug's top 10 but not 
  the other's. For example, lactic acidosis and acute kidney injury feature
  only in metformin's top reported reactions, while dizziness and 
  decreased blood glucose feature only in glipizide's.
- Interestingly, glipizide appears in reports for both increased and 
  decreased blood glucose. This can be described as a bidirectional or
  biphasic response that this dataset alone can't explain, and would
  need further investigation to understand.
- This is a descriptive comparison of raw report counts, not an 
  adjusted risk estimate. The differences may partly reflect how 
  frequently each drug is prescribed, not just intrinsic risk.

## Tools used
Python, pandas, matplotlib, openFDA API

## Next steps
Investigate whether glipizide's bidirectional blood-glucose effect is dose-dependent or driven by patient-specific factors (e.g., age, renal function, or other prescribed medications) since the current dataset doesn't capture enough detail to distinguish between these explanations.
