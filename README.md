# Customer Segmentation & Loan Pricing Analytics — SHB Finance (2024)

**Elevator pitch**  
Actionable customer segmentation and pricing insights derived from 70K+ borrower records to inform risk-based pricing, customer master analytics, and targeted retention programs. :contentReference[oaicite:0]{index=0}

---

## Table of contents
1. [Project summary](#project-summary)  
2. [Business context & goals](#business-context--goals)  
3. [My role & responsibilities](#my-role--responsibilities)  
4. [Data overview](#data-overview)  
5. [Key business questions & KPIs](#key-business-questions--kpis)  
6. [Approach & methods](#approach--methods)  
7. [Key findings & business impact](#key-findings--business-impact)  
8. [Dashboards & deliverables](#dashboards--deliverables)  
9. [How to reproduce](#how-to-reproduce)  
10. [Repository structure](#repository-structure)  
11. [Recommendations & next steps (BI roadmap)](#recommendations--next-steps-bi-roadmap)  
12. [Limitations & ethics](#limitations--ethics)  
13. [Contact](#contact)

---

## Project summary
This project analyzes customer profiles and loan behaviors to (1) identify high-value borrower segments, (2) quantify drivers of loan demand and repayment, and (3) produce pricing recommendations and BI assets to improve portfolio profitability and customer retention. The analysis covers ~70,000+ customer records and year-over-year loan behaviour changes. :contentReference[oaicite:1]{index=1}

---

## Business context & goals
**Context:** Consumer finance business seeking to optimize pricing, reduce defaults, and target marketing/retention effectively.  
**Primary goals**
- Build robust customer segments to improve targeting and personalization. :contentReference[oaicite:2]{index=2}  
- Generate pricing insights (loan demand vs. term preferences vs. repayment likelihood) to support risk-based pricing and product bundling. :contentReference[oaicite:3]{index=3}  
- Deliver BI dashboards for customer master monitoring and portfolio profitability.

---

## My role & responsibilities
- End-to-end BI work: data ingestion → cleaning → EDA → modeling → dashboarding → business recommendations. :contentReference[oaicite:4]{index=4}  
- Implemented segmentation, predictive models (loan type choice & repayment probability), and a Loan Benefit Score to prioritize profitable segments. :contentReference[oaicite:5]{index=5}  
- Presented recommendations (pricing, loyalty tiers, digital onboarding) to shape product and marketing strategy. :contentReference[oaicite:6]{index=6}

---

## Data overview
- **Size:** ~70,000+ customer records (demographics, income bracket, job type, education, marital status, dependents). :contentReference[oaicite:7]{index=7}  
- **Loan attributes:** product type, loan amount, loan term, interest rate, loan purpose (accommodation, vehicle, shopping...), year. :contentReference[oaicite:8]{index=8}  
- **Time span & granularity:** Year-over-year comparison (2022 → 2023) included to capture behavioral shifts. :contentReference[oaicite:9]{index=9}  
- **Note on privacy:** Data used in analysis must be treated as sensitive — do not publish PII. See [Limitations & ethics](#limitations--ethics).

---

## Key business questions & KPIs
**Questions**
- Which customer segments deliver the highest lifetime profitability? :contentReference[oaicite:10]{index=10}  
- What customer features drive loan product choice, term length, and repayment probability? :contentReference[oaicite:11]{index=11}  
- How should pricing differ across segments to maximize profit while controlling default risk?

**KPIs (recommended)**
- Loan Benefit Score (composite profitability – risk – viability). :contentReference[oaicite:12]{index=12}  
- Avg Loan Amount / Segment  
- Avg Loan Term / Segment  
- Repayment Probability / Segment  
- Default rate (by cohort/month)  
- Customer Lifetime Value (CLV) estimate by segment

---

## Approach & methods
**Pipeline**
1. Data ingestion & cleansing (missing values, encoding, outlier handling).  
2. Exploratory Data Analysis (distributional checks, correlation matrices, temporal trends) including statistical tests for 2022 vs 2023 changes. :contentReference[oaicite:13]{index=13}  
3. Unsupervised segmentation: K-Means clustering to define 3 core borrower profiles (entry-level, mid-income stable, high-income family-oriented). :contentReference[oaicite:14]{index=14}  
4. Predictive modeling:
   - **Random Forest** for loan type choice and repayment likelihood (captures non-linear effects & feature importance). :contentReference[oaicite:15]{index=15}  
   - **Multiple Linear Regression** for loan amount/term interpretation and Loan Benefit Score decomposition. :contentReference[oaicite:16]{index=16}  
5. Score & rank segments by Loan Benefit Score = α×Profitability − β×Risk + γ×Viability. :contentReference[oaicite:17]{index=17}  
6. Dashboarding & recommendations (Power BI).

**Why these methods (BI lens)**  
- K-Means gives intuitive segment definitions usable for operational targeting.  
- Random Forests deliver feature importance that product and pricing teams can action on.  
- Regression ensures interpretability for C-level / risk committees when explaining pricing changes.

---

## Key findings & business impact
- **Three core segments** identified: entry-level (small loans), moderately-stable mid-income (mid-term loans), high-income family-oriented (larger loans). These segments align with distinct product preferences and profitability profiles. :contentReference[oaicite:18]{index=18}  
- **High-benefit segments:** Customers with monthly income in the **15–20M VND** bracket and “Segment 3” show the highest Loan Benefit Scores — prioritize these for pricing and cross-sell. :contentReference[oaicite:19]{index=19}  
- **Behavioral shift (2022→2023):** movement away from some loan types to others and an observable short-term loan preference among high-income customers—this suggests revisiting term-based pricing and promotional offers. :contentReference[oaicite:20]{index=20}  
- **Drivers of loan choice & repayment:** income level and job type are among the most influential features for product choice and repayment likelihood. Model outputs directly informed tailored pricing and pre-approval criteria. :contentReference[oaicite:21]{index=21}

**Business impact (example)**
- Recommendations (risk-based pricing, loyalty tiers, flexible loan terms) can increase portfolio profitability by focusing acquisition and retention spend on high-benefit segments while managing default exposure. :contentReference[oaicite:22]{index=22}

---

## Dashboards & deliverables
**Included artifacts**
- `report/SHBFinance_report.pdf` — Executive summary + visuals (used for stakeholder presentation).  
- `notebooks/` — Jupyter notebooks for data prep, segmentation, modeling, and scoring.  
- `models/` — Serialized model artifacts (pickle files) and score metadata.  
- `dashboard/SHB_Customer_Master.pbix` — Power BI file with interactive dashboards (Segment Overview, Pricing Simulator, Repayment Risk Monitor).  
- `README.md` — this file.

**Recommended dashboard pages (BI-ready)**
- Segment Overview (count, avg loan amount, avg term, CLV)  
- Portfolio Profitability by Segment (Loan Benefit Score heatmap)  
- Pricing Simulator (what-if pricing sensitivity & expected default impact)  
- Customer Master Health (data completeness, key changes, top 10 customers by exposure)

---

## How to reproduce
1. Clone repo  
```bash
git clone https://github.com/<your-username>/shb-customer-pricing.git
cd shb-customer-pricing
