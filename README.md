# Customer Segmentation & Loan Pricing Analytics (2025)

## Full Report

The complete project report (225MB, detailed analysis and visualizations) is hosted on Google Drive due to GitHub’s file size limits.  

📄 [Full Report (PDF)](https://drive.google.com/file/d/1PKPhWowJtSyi0gJzH-MIr8N3Juq_khTM/view?usp=sharing)

**Elevator pitch**  
Actionable customer segmentation and pricing insights derived from 70K+ borrower records to inform risk-based pricing, customer master analytics, and targeted retention programs.

---

## Table of contents
1. [Project summary](#project-summary)  
2. [Business context & goals](#business-context--goals)  
3. [My role & responsibilities](#my-role--responsibilities)  
4. [Data overview](#data-overview)  
5. [Key business questions & KPIs](#key-business-questions--kpis)  
6. [Approach & methods](#approach--methods)  
7. [Key findings & business impact](#key-findings--business-impact)  
8. [Recommendations & next steps (BI roadmap)](#recommendations--next-steps-bi-roadmap)  
9. [Limitations & ethics](#limitations--ethics)  
10. [Contact](#contact)

---

## Project summary
This project analyzes customer profiles and loan behaviors to:  
1. Identify high-value borrower segments.  
2. Quantify drivers of loan demand, term preferences, and repayment likelihood.  
3. Deliver actionable pricing recommendations and BI assets that improve profitability and retention.  

The analysis is based on ~70,000 customer records, incorporating year-over-year behavioral changes (2022–2023).

---

## Business context & goals
**Context**  
A firm operates in Vietnam’s consumer finance sector, where profitability is highly dependent on accurate pricing, effective risk management, and sustainable customer relationships.  

**Primary goals**  
- Build robust customer segments to improve targeting and personalization.  
- Generate pricing insights (loan demand vs. repayment likelihood vs. term preferences).  
- Develop BI dashboards for monitoring customer master data and portfolio performance.  

---

## My role & responsibilities
- Designed and executed the full BI pipeline: **data ingestion → cleaning → EDA → modeling → visualization → business recommendations**.  
- Built segmentation and predictive models (loan type choice, repayment probability, loan benefit score).  
- Produced dashboards and presented strategic recommendations (pricing, loyalty tiers, flexible terms) for improved decision-making.  

---

## Data overview
- **Volume:** 70,000+ customer records.  
- **Customer attributes:** demographics, income bracket, job type, education, marital status, dependents.  
- **Loan attributes:** loan type, amount, term, interest rate, purpose (accommodation, shopping, vehicle, etc.).  
- **Time dimension:** year-over-year data (2022 vs. 2023) to capture changing loan demand.  
- **Privacy:** data anonymized; no personally identifiable information included.  

---

## Key business questions & KPIs
**Business questions**  
- Which customer segments drive the highest profitability and lowest default risk?  
- What factors influence loan product choice and repayment likelihood?  
- How should pricing and loan terms be adjusted for different customer segments?  

**KPIs**  
- Loan Benefit Score (profitability – risk – viability).  
- Average Loan Amount per segment.  
- Repayment probability per segment.  
- Default rate by cohort.  
- Estimated Customer Lifetime Value (CLV).  

---

## Approach & methods
**Pipeline**  
1. **Data cleaning & preparation** (missing values, encoding, outliers).  
2. **Exploratory Data Analysis (EDA):** demographic trends, correlations, time-based changes.  
3. **Segmentation:** K-Means clustering → 3 borrower profiles (entry-level, mid-income stable, high-income family-oriented).  
4. **Predictive modeling:**  
   - Random Forest: loan product choice & repayment likelihood.  
   - Linear Regression: loan amount, loan term, and benefit score decomposition.  
5. **Loan Benefit Score:** composite scoring model to prioritize profitable customer groups.  
6. **BI dashboards:** designed in Power BI for monitoring and decision support.  

**Why these methods?**  
- Clustering = intuitive segments for marketing/CRM.  
- Random Forest = non-linear patterns & feature importance.  
- Regression = interpretability for business leaders.  

---

## Key findings & business impact
- **Three actionable segments**: entry-level borrowers, mid-income individuals, and high-income family clients.  
- **High-value group:** income bracket 15–20M VND showed the highest Loan Benefit Scores → recommended as primary focus.  
- **Behavioral shift (2022–2023):** high-income customers moved toward shorter-term loans, signaling risk-averse behavior.  
- **Drivers of loan choice:** income level and job type were the strongest predictors for loan product and repayment behavior.  

**Impact**  
- Risk-based pricing recommendations to align interest rates with repayment probability.  
- Targeted retention initiatives (loyalty programs, flexible terms) to increase CLV.  
- Operational dashboards to improve customer master monitoring and decision-making.  

## Recommendations & Next Steps (BI Roadmap)

- **Operationalize Loan Benefit Score**: integrate into CRM pipeline to support real-time customer scoring and targeted campaigns.  
- **Deploy Pricing Simulator**: run A/B tests on pricing adjustments to measure impact on profitability and default rates.  
- **Integrate Dashboards**: connect Power BI dashboards with real-time updates from the customer master database.  
- **Pre-Approval Logic**: apply automated pre-approval for stable income segments to improve loan conversion rates.  
- **Model Governance**: monitor model drift and repayment KPIs monthly to ensure stability and fairness.

---

## Limitations & Ethics

- **Data Privacy**: all datasets anonymized; no personally identifiable information (PII) shared.  
- **Bias Risks**: models built on historical patterns, subject to sampling bias and changing economic conditions.  
- **Validation**: recommendations should be tested with controlled A/B experiments before company-wide rollout.

---

## Contact

**Nguyen Thi Thanh Truc (Willow)**  
📧 willownguyen.2111@gmail.com  
🌐 GitHub: [github.com/WillowNguyen](https://github.com/WillowNguyen)
