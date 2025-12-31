# 🏦 Bank Marketing: Predictive Lead Scoring with Explainable AI (XAI)

> 🚀 **New Visitors:** To understand the high-level business value and model performance, please start with the **[Welcome_Bank_Predictive_SHAP.pdf](./01_Executive_Summary/Welcome_Bank_Predictive_SHAP.pdf)** in the Executive Summary folder.

---

## 📂 Project Roadmap
To review this project in a logical flow, please explore the folders in numerical order:

1. **[01_Executive_Summary](./01_Executive_Summary)**: Business-focused introduction and high-level ROI summary.
2. **[02_Documentation](./02_Documentation)**: Deep-dive into model insights, feature importance, and strategic actions.
3. **[03_Source_Code](./03_Source_Code)**: Full Python implementation (Random Forest) and the Live Waterfall Generator.
4. **[04_Data_Deliverables](./04_Data_Deliverables)**: The final prioritized lead lists for sales execution.
5. **[05_Visual_Insights](./05_Visual_Insights)**: SHAP Summary and Waterfall plots illustrating the "Why" behind the AI.

---

## 🛠️ Step-by-Step Technical Process

### 1. Data Ingestion & Engineering
* **Dataset:** 41,188 client records featuring demographic and historical interaction data.
* **Encoding:** Converted categorical traits into 53 numeric features using One-Hot Encoding to ensure model compatibility.

### 2. Model Architecture (Random Forest)
* **Strategy:** Utilized an ensemble of 300 Decision Trees to minimize variance and maximize accuracy.
* **Performance:** Achieved a **95% ROC-AUC**, ensuring high-confidence separation between subscribers and non-subscribers.

### 3. Explainable AI (SHAP Integration)
* **Transparency:** Integrated SHAP (Shapley Additive Explanations) to transform a "Black Box" model into a fully auditable system.
* **Waterfall Analysis:** Every individual score can be broken down to show exactly which features (e.g., call duration, previous success) pushed the score up or down.

### 4. Categorical Lead Tiering
Probability scores are mapped to a high-velocity sales funnel:
* **💎 Platinum (70%+):** High-priority leads with confirmed conversion drivers.
* **🥇 Gold (50-69%):** Strong prospects for standard follow-up.
* **🥈 Silver (0-49%):** Long-term nurture leads for automated marketing.

---

## 📈 Business Impact & ROI

By moving from mass marketing to AI-driven precision, the bank achieves:

* **Maximized Conversion:** Platinum leads are **6x more likely to subscribe** than the average lead, significantly increasing the conversion rate of outbound calls.
* **Operational Efficiency:** Sales teams can ignore the bottom 50% of the list, reducing call fatigue and focusing on high-revenue potential.
* **Data-Driven Sales Scripts:** Insights identified that **call duration** is the #1 driver of success, allowing managers to train teams on keeping prospects engaged longer.
* **Instant Scalability:** The serialized model (`.pkl`) can score 10,000+ new leads in seconds every morning.

---

## 🖼️ Model Insights & Visuals

### Global Drivers (SHAP Summary)
![SHAP Summary](./05_Visual_Insights/SHAP_Summary.png)
*Figure 1: Visual ranking of features driving deposits, highlighting Call Duration and Previous Success as the dominant factors.*

### Individual Explanation (Waterfall)
![Waterfall](./05_Visual_Insights/Waterfall.png)
*Figure 2: A "Live Waterfall" explaining why a specific lead was marked as Platinum.*

---

## 💼 Availability for Hire (UAE / Singapore / GCC)
Specializing in Predictive Lead Scoring and Explainable AI (XAI).

**Najeeb P.A** [LinkedIn Profile] | najeebpa81@gmail.com | +65 91817634
