# Validation status — 24 October 2026

## Verified with the user-supplied Bank Marketing CSV
- Bank Marketing dataset: 41,188 records, 21 columns.
- Rule-based scoring notebook executed and the tier chart was regenerated.
- Predictive notebook executed using a 75/25 stratified split, one-hot encoding fitted on training data only, and `duration` excluded.
- Holdout ROC-AUC: 0.8148; average precision: 0.4897.
- SHAP summary and waterfall images regenerated from the revised fitted model (80 test rows used for explanation).
- Row-level exports disabled in public notebooks.

## Verified with the user-supplied Dubai Bayut CSV
- Dataset: 41,381 property listings, 22 columns.
- All required scoring columns are present.
- Executed the Dubai notebook code against the supplied CSV in a Python process (Jupyter magic removed for execution); no missing segments.
- Segment counts: Low (<=50): 24,338, Medium (51-90): 14,003, High (>90): 3,040.
- Recreated the listing-segment bar chart from these results. This is not a predictive buyer model.

## Outstanding
- The Dubai notebook code executed successfully outside a Jupyter kernel; full Jupyter-kernel reproducibility remains unchecked.
- Dataset licenses remain unverified; source CSVs and row-level exports are excluded.
- The bank model is a historical random-split experiment, not prospective deployment validation.
- Old public GitHub history may still expose previously committed data.
- Images reflect this execution, but repeatability on a different software environment has not been independently tested.
