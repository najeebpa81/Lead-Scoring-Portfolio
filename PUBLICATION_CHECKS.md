# Publication checks — 24 October 2026

- Kaggle notebook input links identify the user-provided sources, but do **not** establish redistribution permission. Raw datasets, scored row-level records, and packaged Tableau workbooks are excluded.
- Bank Marketing rule-based scoring and predictive model were tested against the supplied 41,188-record CSV. See `VALIDATION_STATUS.md` and `BANK_VALIDATION_METRICS.json`.
- Dubai notebook Python code was executed against the supplied 41,381-listing CSV, after removing notebook-only `%matplotlib inline` for the execution check. See `DUBAI_VALIDATION_METRICS.json`.
- Bank Marketing predictive model excludes `duration`, fits one-hot encoding using training data only, and achieves held-out ROC-AUC 0.8148 and average precision 0.4897 in the recorded random split. This is not prospective validation.
- Bank rule-based tiers produce no Hot cases with the current thresholds; the rules are not business-validated.
- Old public GitHub commit history is unaffected by uploading this package. Do not overwrite the existing repository until a clean-history publication plan is agreed.
- The provided notebook files were not independently executed from top to bottom in a fresh Jupyter kernel with all dependencies pinned; future environment changes may affect repeatability.
