 Executive Summary: Enterprise Capital Allocation & Performance Audit 
**Lead Data Analyst:** Eyong Eyong Eneke Alain   

---

### C-Suite Strategic Alignment & Executive Governance

Enterprise payroll spend represents the organization's largest controllable operating commitment (**$6.87M USD** across 100 audited positions), yet standard HR reporting frequently manages personnel as fixed overhead rather than capital investments requiring financial return[cite: 1, 2].
 **Project Talent ROI** bridges workforce analytics and financial governance by providing tailored diagnostic intelligence across the C-Suite.

* **Chief Executive Officer (CEO):** Realigns organizational culture with a true pay-for-performance model, eliminating tenure-based productivity decay and ensuring top-tier talent is incentivized to drive long-term strategic value.
* **Chief Financial Officer (CFO):** Identifies and reclaims **$2.80M USD in Low-Performance Capital Drain (LPCD)**, closes structural pay grade overlap anomalies, and restores capital allocation efficiency across business units.
* **Chief Human Resources Officer (CHRO):** Re-engineers compensation architecture, enforces strict salary band midpoints, mitigates high-performer flight risks, and corrects branch-level pay equity gaps.

By translating raw workforce metrics into C-Suite financial diagnostics, this audit transforms human capital management from administrative oversight into a strategic driver of enterprise profitability and governance[cite: 1, 2].


## 1. Problem Statement & Core Business Challenge
Enterprise leadership currently lacks visibility into direct capital productivity within human workforce expenditure. Standard HR reporting focuses heavily on descriptive operational metrics (headcount, absenteeism, training hours) rather than financial ROI and capital efficiency. 

As a result, the organization faces four major structural risks:
1. **Unmonitored Payroll Leakage:** Severe capital drain allocated to low-performing talent without performance justification.
2. **Decoupled Pay-for-Performance:** A compensation framework operating independently of performance output, leading to demotivated top performers and overcompensated underperformers.
3. **Pay Band Entropy & Overlap:** Unenforced pay grades allowing salary inflation across junior and senior administrative levels.
4. **Tenure Productivity Decay:** Compounding salary increases for long-tenured employees paired with stagnating or declining performance output.

**Goal:** This project solves these challenges by auditing $6.87M USD in direct compensation spend across 100 enterprise records, converting raw HR data into actionable financial diagnostics for C-Suite executives (CFO, CHRO, CEO).

---

## 2. Core Audit Findings & C-Suite Strategic KPIs

1. **Low-Performance Capital Drain (LPCD):** **$2.80M USD (40.74% of total payroll)** is allocated to underperforming employees (Ratings 1–2).
2. **Broken Pay-for-Performance:** Statistically near-zero correlation ($r = 0.0673$) between total compensation and employee performance output.
3. **Tenure Productivity Decay:** Staff with 10+ years of tenure exhibit the lowest average performance score (**2.53 / 5.0**) compared to new hires under 3 years (**3.06 / 5.0**), despite earning higher average compensation ($73.9k vs. $66.1k).
4. **Pay Grade Overlap Entropy:** Adjacent salary bands (Grades A through D) show a **100% overlap ratio**, spanning $30k to $98k without enforced midpoint controls.
5. **Equity Deficits & Misallocation:**
   * **15 High-Performer Flight Risks:** Staff with performance scores >= 4 who are compensated below the corporate median ($66.1k).
   * **20 Overcompensated Low Performers:** Staff with performance scores <= 2 who earn above the corporate median.
   * **Branch Gender Pay Gap:** Female employees at branch locations experience an **12% compensation deficit** relative to male peers ($62.4k vs. $70.8k).

---

## 3. Operational HR KPIs Summary

| HR Operational Metric | Value |
| :--- | :--- |
| **Total Headcount** | 100 Employees |
| **Total Direct Cash Compensation (TCC)** | $6,866,804.00 |
| **Average Compa-Ratio (vs. Median Midpoint)** | 1.05 |
| **Cost per Performance Point** | $23,678.63 / Point |
| **Overall Absenteeism Rate** | 4.77% (327.4 days equivalent) |
| **Training Participation Rate** | 61.0% |
| **Certification Upskilling Rate** | 63.0% |
| **Contingent Workforce Ratio** | 59.0% |
| **High Performer Share (Rating 4–5)** | 35.0% |
| **Benefits & Insurance Adoption Rate** | 68.0% |

---

## 4. Key Visualizations Developed

* **Operational Grid:**
  1. Departmental Payroll Breakdown ($2.09M in Sales leading total spend).
  2. Workforce Distribution across Performance Scores (1–5 scale).
  3. Work Location Split across Employment Types.
* **Strategic Diagnostic Grid:**
  1. **Total Payroll Spend by Department:** Highlights headcount vs. capital allocation per department.
  2. **Compensation Delta from Company Mean ($76,480):** Proves Rating 2 underperformers receive +$3,475 above company mean, while Rating 3 core staff receive -$1,200 below mean.
  3. **Pay Grade vs. Performance Matrix (Heatmap):** Pinpoints pay band anomalies, such as Grade B Rating 2 staff commanding $93,798 on average.
  4. **Tenure Performance Progression:** Tracks the decay curve from mid-tenure peak (3.12) down to senior tenure (2.90).

---

## 5. Methodology & Data Pipeline Architecture

1. **Data Ingestion & Cleaning:**
   * Imported raw 100-row enterprise dataset (`HR Dataset.xlsx`).
   * Cleaned numeric fields (`Salary`, `Bonus/Allowances`, `Leave Taken`) and imputed missing allowance values with `$0`.
   * Formatted dates and derived total direct compensation (`Total_Compensation = Base Salary + Bonus/Allowances`).
2. **Feature Engineering:**
   * Calculated exact `Tenure_Years` using hire date relative to audit baseline.
   * Binned continuous metrics into categorical groups (`Tenure_Group`: 0–3 yrs, 3–6 yrs, 6–10 yrs, 10+ yrs; `Age range`: 18–25, 26–35, 36–45, 46–55, 56+).
3. **Analytical Auditing:**
   * Aggregated cross-tabulations across `Pay Grade`, `Performance Rating`, and `Work Location`.
   * Evaluated correlation coefficients ($r$) between pay, tenure, age, and performance.
4. **Report Exporting:**
   * Generated action-oriented CSV exports for executive decision-making (`compensation_reallocation_action_list.csv`).
   * Rendered high-resolution 300 DPI visualizations for presentation decks.

---

## 6. Repository & File Structure

```text
├── HR Dataset.xlsx                          # Raw enterprise dataset
├── Project_Talent_ROI_Audit.ipynb           # Main Jupyter Notebook
├── run_audit.py                              # Executable CLI Python script
├── output_reports/                           # Exported CSV action lists
│   └── compensation_reallocation_action_list.csv
├── output_charts/                            # High-res PNG chart exports
│   ├── distinct_4_chart_grid.png
│   ├── dept_summary_dashboard.png
│   └── pay_for_performance_misalignment.png
└── README.md                                 # Executive project documentation