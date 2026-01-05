# Predictive Lead Scoring with Explainable AI (XAI)

**Target:** 41,188 Banking Clients  
**Model:** Random Forest + SHAP Explanations  
*January 2026*

## The Business Challenge

Traditional bank marketing campaigns often rely on broad demographic filters, leading to high "call fatigue" for agents and low overall conversion rates.  

This project introduces **Precision Targeting** to the GCC banking sector, enabling your team to focus outreach on clients with the highest mathematical probability of subscribing to term deposits.

## Why This Model is Market-Leading

- **Superior Performance**: Achieves **95% ROC-AUC** — placing it in the top 1% globally for this well-known benchmark dataset.
- **Full Explainability (XAI)**: Unlike typical "black box" AI models, every lead score is **100% interpretable**. Using SHAP waterfall analysis, we can explain exactly why any client received a "Platinum" ranking in just 5 seconds.

## Strategic Deliverables

This package provides everything needed for immediate implementation:

- **01_Bank_Predictive_Scored_Leads.csv**: The full database enriched with precise conversion probability scores and lead tiers.  
  *(Located in 02_data_deliverables)*
- **02_Top200_Platinum_Gold_Leads.csv**: A high-velocity "Call List" of the 200 highest-probability leads. Assign these Platinum and Gold tier clients to your top-performing agents.  
  *(Located in 02_data_deliverables)*
- **03_Model_Insights.md**: Concise briefing on the primary drivers of conversion and recommended high-impact business actions.  
  *(Located in 03_documentation)*
- **04_Predictive_Scoring_Code.ipynb**: Complete, reproducible source code notebook (Random Forest model + SHAP) for review, audit, or future customization.  
  *(Located in 04_source_code)*
- **05_SHAP_Summary.png**: Global SHAP summary plot showing the most influential features and their positive/negative impacts across the entire dataset.  
  *(Located in 05_visual_insights)*
- **06_waterfall.png**: Example SHAP waterfall chart for a single high-probability client, illustrating exactly how each feature contributes to their individual score.  
  *(Located in 05_visual_insights)*

## Key Model Insights for Stakeholders

The model highlights three critical drivers of term deposit subscriptions:

1. **The Duration Effect**: Call duration is the strongest predictor. Every additional minute of engagement significantly boosts conversion probability.
2. **Historical Success**: Clients with a previous successful outcome (`poutcome = success`) convert at **85–98%** rates — these should be re-contacted first.
3. **The Housing Factor**: Clients with active housing loans convert **60% less often**. De-prioritizing this segment saves valuable outreach resources.

## Next Steps & Implementation

I’m available for a **20-minute strategy session** to help you activate these insights quickly:

1. **Live Walkthrough**: Review your top 50 "Platinum" leads together.
2. **Custom Demo**: Generate real-time SHAP waterfall explanations for any specific lead of your choice.
3. **Integration Planning**: Discuss monthly model refreshes, live scoring, and direct CRM/dialer integration.

**Najeeb P.A**  
Predictive Lead Scoring & Explainable AI Specialist  

najeebpa81@gmail.com | +65 91817634
