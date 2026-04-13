# 📊 Workforce-Intelligence-Dashboard-Uncovering-Attrition-Drivers-Promotion-Gaps

*A 4-page business-ready analytics tool covering workforce distribution, attrition drivers, compensation patterns, and promotion trends.*

> **Attrition is highest in the 26–35 age group. Sales has the longest promotion wait time. Overtime employees leave significantly more. The data tells you where to act.**

---

## 🔷 Overview

HR teams often sit on rich data but lack a clear view of *why* people leave and *who* is at risk. This dashboard bridges that gap — built with clean data modelling, DAX measures, and insight-first visual design across 4 focused pages.

**Built for:** HR leaders, people analytics teams, and workforce strategy decision-makers.

---

## 🔷 Key KPIs at a Glance

| Metric | Description |
|---|---|
| 👥 Total & Active Employees | Headcount overview |
| 🚪 Attrition Count & Rate | Who left and at what frequency |
| 💵 Avg & Median Monthly Income | Compensation benchmarks |
| 💸 Avg Salary — Attrited Employees | Compensation of those who left |
| 🎂 Average Age & Tenure | Workforce maturity indicators |
| ⏳ Avg Years Since Last Promotion | Promotion health signal |

---

## 🔷 Dashboard Preview

<img width="439" height="250" alt="image" src="https://github.com/user-attachments/assets/4cbe8b4e-3f54-40ed-8042-5367c72a545c" />
<img width="439" height="250" alt="image" src="https://github.com/user-attachments/assets/c3782ac8-534a-4d3a-86f4-7380357e8f4c" /> </br>
<img width="439" height="250" alt="image" src="https://github.com/user-attachments/assets/dada8b90-8eee-4b51-8d37-69bd6d89696b" />
<img width="439" height="250" alt="image" src="https://github.com/user-attachments/assets/20f4d7ea-789d-4de9-a818-cea65ba97b3e" />

---

## 🔷 Dashboard Pages

### 1 — Workforce Overview
Headcount by department and age group, gender distribution, and core workforce KPIs. Sets the baseline before diving into problem areas.

### 2 — Attrition Analysis
The core of the dashboard. Breaks attrition down by job role, age group, department, overtime status, distance from home, and compensation. Answers the question: *who is leaving and why?*

### 3 — Salary & Compensation
Total salary cost, average and median monthly income by role and gender, and compensation distribution. Surfaces pay inequities and cost-of-attrition implications.

### 4 — Promotion & Tenure
Promotion wait time analysis, tenure distribution, and department-wise comparison. Answers: *are we promoting the right people at the right time?*

---

## 🔷 Key Insights

- **Attrition peaks in the 26–35 age group** — the highest-value talent cohort for most organizations
- **Sales has the highest turnover AND the longest promotion wait time** — a compounding retention risk
- **Overtime is strongly correlated with attrition** — employees working overtime leave at a disproportionately higher rate
- **Compensation varies significantly across roles and departments** — creates internal equity issues that HR can act on

---

## 🔷 Sample DAX Measures

```dax
Attrition Rate :=
DIVIDE(
    CALCULATE(COUNTROWS(HR_Data), HR_Data[Attrition] = "Yes"),
    COUNTROWS(HR_Data)
)

Avg Monthly Income :=
AVERAGE(HR_Data[MonthlyIncome])

Avg Years Since Promotion :=
AVERAGE(HR_Data[YearsSinceLastPromotion])

Active Employees :=
CALCULATE(COUNTROWS(HR_Data), HR_Data[Attrition] = "No")
```

---

## 🔷 Data Cleaning (Power Query)

- Removed nulls and duplicate employee records
- Standardized categorical fields (department, job role, education level)
- Created age group and tenure buckets for segmentation
- Built calculated columns for attrition flags and compensation ratios
- Structured data model for cross-page filter consistency

---

## 🔷 Tech Stack

```
Power BI Desktop   →  Data modelling, DAX, report design
Power Query        →  Data cleaning & transformation
Excel / CSV        →  Source data preparation
DAX                →  KPI calculations & custom measures
```

---

## 🔷 Business Impact

- Gives HR a **single dashboard** to monitor workforce health across 4 dimensions
- Pinpoints **which departments and roles** carry the highest attrition risk
- Quantifies the **cost of overtime culture** through attrition correlation
- Enables **targeted interventions** — rather than broad, expensive retention programs

---

## 📌 Future Improvements

- Add **predictive attrition scoring** using Python integration in Power BI
- Build a **What-if parameter** to model impact of salary increases on attrition rate
- Include **exit survey sentiment data** to add qualitative context
- Connect to live HRIS data source for real-time monitoring

---

## 💡 Key Learning

> The hardest part wasn't the DAX or the visuals.  
> It was deciding *which* questions the dashboard should answer — and resisting the urge to answer all of them at once.
