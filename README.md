# Lead Scoring & Segmentation Portfolio

Three learning projects comparing transparent rule-based scoring, property-listing segmentation, and predictive classification with SHAP. These are retrospective portfolio exercises, not deployed client systems.

## Projects

1. **[Bank Marketing — Rule-Based Scoring](01_Bank_Marketing_Rule_Based/)** — heuristic scoring of historical bank campaign records.
2. **[Dubai Property Listings — Rule-Based Segmentation](02_Dubai_Real_Estate_Rule_Based/)** — illustrative property-attribute segmentation; **not** buyer-lead conversion scoring.
3. **[Bank Marketing — Predictive Modeling & SHAP](03_Bank_Marketing_Predictive_SHAP/)** — Random Forest modeling of historical term-deposit outcomes and feature attribution.

The two Bank Marketing projects use the **same underlying dataset** and show different analytical approaches; they are not independent validation datasets.

## Dataset references

- **Bank Marketing:** [Kaggle notebook input page](https://www.kaggle.com/code/gatewj/bank-marketing-dataset/input). The original dataset listing and its license have **not been verified**.
- **Dubai property listings:** [Kaggle notebook input page](https://www.kaggle.com/code/azharsaleem/unlocking-real-estate-gold-in-depth-analysis/input?select=bayut_selling_properties.csv), referencing `bayut_selling_properties.csv`. The original dataset listing and its license have **not been verified**.

These links identify notebook inputs, **not verified redistribution licenses**. The repository excludes original and scored row-level datasets, spreadsheets, and packaged Tableau workbooks pending source/license verification.

## Run locally

1. Obtain the datasets from an authorized source and check the applicable terms.
2. Put `Bank_Marketing.csv` or `bayut_selling_properties.csv` in the working directory from which you launch the corresponding notebook (or edit its input path).
3. Install dependencies with `pip install -r requirements.txt`.
4. Execute notebooks in order, top to bottom. Outputs and local scored CSVs are generated locally and excluded from Git.

The Bank Marketing analyses were tested on the supplied 41,188-row CSV. The Dubai scoring calculations were tested on the supplied 41,381-row CSV; see `VALIDATION_STATUS.md` for exact checks and limitations. Input paths and installed library versions may require adjustment.

## Important limitations

- Rule-based scores are analyst-selected heuristics, not calibrated conversion probabilities.
- The Dubai data describe **listings**, not identified prospective buyers; the scoring rules do not establish sales likelihood.
- Bank marketing **call duration** is only known after a call; a model using it cannot be described as a pre-call targeting model. The revised predictive notebook excludes it; the rule-based notebook remains a retrospective illustration.
- SHAP shows feature contributions to model output, not causal relationships.
- No claims of realized ROI, deployment readiness, or verified commercial results are made.
