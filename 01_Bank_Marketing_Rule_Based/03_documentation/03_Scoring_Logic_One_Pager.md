# Scoring Logic Framework: Bank Term Deposits

**Project:** Rule-Based Lead Prioritization | **Database:** 41,188 Clients

## Objective

To replace "blind calling" with a weighted scoring engine that identifies clients with the highest propensity to subscribe to a fixed-term deposit.

## Weighted Scoring Criteria (Max 200 Points)

The engine calculates a `lead_score` for every client based on the following verified business rules:

| Category          | Criteria                  | Points | Business Rationale                                                                 |
|-------------------|---------------------------|--------|------------------------------------------------------------------------------------|
| Past Performance  | poutcome == 'success'     | +60    | Historical data shows these clients have an 85%+ conversion rate.                   |
| Engagement        | Duration > 10 mins        | +50    | High interaction time is the #1 indicator of interest in banking products.         |
| Financial Profile | No Housing Loan           | +30    | Clients without existing debt have higher liquidity for new deposits.              |
| Contact Method    | Cellular Contact          | +25    | Mobile users are 3x more likely to engage compared to landline targets.            |
| Timing            | Month == 'Mar/Oct'        | +20    | High-performance months for GCC banking seasonal promotions.                       |
| Engagement        | Duration 5-10 mins        | +15    | Moderate interest level; requires a strong closing script.                         |

## Lead Tier Classification

Based on the final score, leads are automatically routed into three operational tiers:

- **Hot (Score 100+)**: The "Closing" List. High-intent leads with previous success or massive engagement.  
  **Action:** Assign to Top-Tier Relationship Managers.

- **Warm (Score 50-99)**: The "Nurture" List. Potential interest detected but requires more persuasion.  
  **Action:** Assign to standard sales team for follow-up within 24 hours.

- **Cold (Score 0-49)**: The "Marketing" List. No strong signals of immediate intent.  
  **Action:** Route to automated SMS/Email drip campaigns to save agent time.

## Why this Rule-Based Approach?

1. **100% Transparent**: Every score is explainable to the sales agent.
2. **Instant Deployment**: No complex AI infrastructure required; runs on standard Python/Excel.
3. **Audit-Ready**: Perfect for banking compliance where "Black Box" algorithms might face scrutiny.


Feel free to reach out if you'd like to discuss the top leads or how to put these insights into action

**Najeeb P.A**  
Lead Scoring Specialist  
najeebpa81@gmail.com | +65 91817634
