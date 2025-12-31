# 🏦 Bank Predictive Lead Scoring & Classification (GCC Edition)

> **New Visitors:** Please start with the [Welcome_Bank_Predictive_SHAP.pdf](./Welcome_Bank_Predictive_SHAP.pdf) for a high-level executive summary of this project's objectives and results.

---

## 📂 Project Navigation & Roadmap

To get the most out of this showcase, I recommend exploring the files in the following order:

1.  **🚀 [START HERE] `Welcome_Bank_Predictive_SHAP.pdf`**: A professional introduction to the project, intended for business stakeholders.
2.  **📋 `03_Model_Insights.pdf`**: A deep dive into the SHAP results, explaining the "Why" behind the model's decisions.
3.  **🧪 `04_Predictive_Scoring_Code.ipynb`**: The full Python implementation, from data cleaning to model training.
4.  **🎯 `01_Bank_Predictive_Scored_Leads.xlsx`**: The final deliverable—a prioritized list of leads ready for a sales team.
5.  **⚡ `5_Live_Waterfall_Generator.ipynb`**: An interactive script to generate real-time explanations for any individual customer.

# 🏦 Bank Predictive Lead Scoring & Classification

This project implements a machine learning solution to transform banking outreach from "Mass Marketing" to **"Precision Targeting."** By utilizing an ensemble-based Random Forest model and Explainable AI (SHAP), we identify high-intent leads and prioritize them into actionable tiers for the sales team.


## 🛠️ Technical Process Flow

### 1. Data Ingestion & Feature Engineering
Converting raw business data into a machine-readable format:
* **Data Parsing:** Handling non-standard delimiters (semicolons) and encoding binary outcomes (Yes/No to 1/0).
* **One-Hot Encoding:** Converting categorical variables (Job, Education, Marital Status) into 53 distinct numeric features. 

### 2. Strategic Data Partitioning
Ensuring the model generalizes well to new market data:
* **The Holdout Method:** Splitting data into a **Training Set** (logic building) and a **Test Set** (simulating unseen future customers).
* **Feature-Target Isolation:** Separating independent variables (customer traits) from the dependent variable (subscription outcome).

### 3. Ensemble Model Architecture
Utilizing a **Random Forest Classifier** to reduce error and variance:
* **n_estimators (300):** Building 300 unique trees to create a "wisdom of the crowd" effect for higher accuracy.
* **max_depth (12):** A regularization technique used to prevent **overfitting** by stopping trees from memorizing individual historical noise.
* **Parallel Processing:** Optimized using `n_jobs=-1` to utilize all available CPU cores for high-speed training.

### 4. Model Training & Heuristics
The process where the model learns the "rules" of banking conversions:
* **Bootstrapping:** Training each tree on a different random sample of data to ensure forest diversity.
* **Feature Randomness:** Forcing trees to consider a random subset of features at each split, preventing over-dependence on a single metric like "Account Balance."

### 5. Performance Validation (ROC-AUC)
In lead scoring, ranking quality is the primary success metric:
* **Probabilistic Scoring:** Generating confidence scores between 0.0 and 1.0 using `predict_proba`.
* **ROC-AUC Metric:** Measuring the model’s ability to distinguish between subscribers and non-subscribers. An **AUC of 0.85** indicates excellent discriminatory power.

### 6. Lead Tiering & Business Logic
Translating mathematical probabilities into a prioritized sales strategy:
* **Binning Logic:** Categorizing leads into priority tiers using `pd.cut`:
    * **Platinum (70%+):** Immediate high-touch contact.
    * **Gold (50-70%):** Standard sales follow-up.
    * **Silver (0-50%):** Nurture through automated marketing.
* **Output Generation:** Exporting a **Scored Leads CSV** for non-technical sales teams.

### 7. Explainable AI (XAI) with SHAP
Opening the "Black Box" to build stakeholder trust:
* **Shapley Values:** Using Game Theory to calculate the exact contribution of each feature to an individual prediction.
* **Global Interpretation:** Using **Summary Plots** to rank the most important drivers across the entire dataset.
* **Local Interpretation:** Using **Waterfall Plots** to explain the specific "why" behind a single lead's high score.

### 8. Model Serialization & Handover
Making the project "Production-Ready":
* **Persistence (joblib):** Saving the trained model object (`.pkl`) to allow for instant scoring of new leads without retraining.
* **Reproducibility:** Saving the column structure (`model_columns.pkl`) to ensure future data inputs match model expectations.

---

## 📈 Business Impact & ROI

By implementing this predictive system, the following business outcomes are achieved:

* **Increased Conversion Rates:** By prioritizing **Platinum** leads, the sales team focuses on customers **6x more likely to subscribe** than the average lead.
* **Operational Efficiency:** Reduces "Cold Calling" fatigue. Sales teams can ignore the bottom 50% of the list (Silver tier) where success probability is negligible.
* **Data-Driven Strategy:** SHAP insights revealed that **call duration** and **previous campaign success** are the primary drivers, allowing for refined sales scripts.
* **Scalability:** The serialized model processes thousands of new leads in seconds, ensuring a consistent sales pipeline.
* **Regional Insight:** Specifically optimized for GCC-style banking data, identifying that **call duration** is the primary driver for successful fixed-term deposit subscriptions.

---

## 🖼️ Featured Insight: Conversion Drivers
![SHAP Summary Plot](./SHAP%20Summary.png)
*Figure 1: Global feature impact. Note how high 'duration' (red dots to the right) is the strongest predictor of a successful subscription.*
