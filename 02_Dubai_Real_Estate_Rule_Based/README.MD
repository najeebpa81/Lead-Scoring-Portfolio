# 🏙️ Dubai Real Estate: Rule-Based Lead Scoring & Investor Tiering

> 🚀 **New Visitors:** To understand the strategic objectives of this project, please start with the **[Welcome_Dubai_Real_Estate.pdf](./Welcome_Dubai_Real_Estate.pdf)** for a high-level executive summary.

## 📂 Project Overview
This repository contains a specialized lead scoring engine designed to process **41,381 Dubai property listings**. By applying a custom-weighted heuristic model, the system identifies high-value "Hot Leads" from massive datasets, enabling real estate brokers to focus their energy on the most lucrative opportunities.

## 🛠️ Step-by-Step Technical Process

### 1. Data Ingestion & Audit
* **Dataset:** 41,381 records containing 22 features (Price, Location, Beds, Completion Status, etc.).
* **Integrity Check:** Standardized numerical columns (`price`, `beds`, `baths`) and handled missing values in geolocation data.

### 2. UAE-Specific Feature Engineering
* **Arabic Content Detection:** Implemented a Regex-based function to detect Arabic script in `building_name` and `address`. 
* **Cultural Context:** Identifying Arabic naming often correlates with localized marketing campaigns or specific investor segments in the GCC, used as a scoring weight (+15 points).

### 3. The Scoring Engine (Rule-Based Heuristics)
Instead of a "Black Box" model, we use a transparent, auditable scoring system (Max Score: 200) based on market drivers:
* **Luxury Tiering:** Up to **50 points** for properties over AED 10M.
* **Prime Location Analysis:** Automated detection of **Hot Areas** (Palm Jumeirah, Downtown, Dubai Hills, etc.) adding **30 points**.
* **Ready-to-Move Premium:** **25 points** for 'Ready' status vs. off-plan, reflecting immediate buyer intent.
* **Volume & Luxury:** Points assigned for high bedroom/bathroom counts (4+), indicating high-ticket investor leads.

### 4. Categorical Tiering
The raw scores are transformed into a prioritized sales funnel:
* **🔥 Hot (90+):** 3,040 Properties (The "Platinum" Call List).
* **🟠 Warm (50-89):** 14,003 Properties (Nurture Pipeline).
* **🔘 Cold (0-49):** 24,338 Properties (Automated Marketing).

---

## 📈 Business Impact & ROI

By implementing this rule-based scoring, a Dubai-based agency achieves:

* **High-Value Targeting:** The system instantly isolated the **top 7% (3,040 leads)** of the database. Focusing sales staff here ensures they are working on listings with higher commissions (Luxury properties in Hot Areas).
* **Reduced Time-to-Close:** By awarding points for **"Ready" completion status**, the engine prioritizes inventory that can be transacted immediately.
* **Improved Lead Management:** Transforms a chaotic list of 41k entries into a ranked strategy, reducing agent burnout from "Cold Calling" irrelevant leads.
* **Strategic Expansion:** The scoring logic is easily adjustable. If a new area (like *Dubai Creek Harbour*) becomes "Hot," the engine can be updated in seconds to reflect market shifts.

## 🖼️ Market Visuals

### Lead Distribution Overview
![Lead Tiers Bar Chart](./Lead_Tiers_Bar_Chart.png)
*Figure 1: Distribution of 41,381 properties into actionable sales tiers.*

### Top Tier Example
| Building Name | Area | Price (AED) | Score |
| :--- | :--- | :--- | :--- |
| **Palm Jumeirah** | Luxury Villa | 111,000,000 | **140** |
| **Dubai Hills Estate** | Mansion | 14,500,000 | **140** |

---

## 💼 Contact (UAE/GCC)
Specializing in Real Estate Data Architecture and Lead Prioritization.<br>
Mohamed Najeeb P.A <br>
najeebpa81@gmail.com
