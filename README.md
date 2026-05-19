# HR Employee Attrition Analysis
### Python · SQL · Power BI

> Identifying why employees leave using data — and what companies can do about it.

---

## Problem Statement

Employee attrition is costly — replacing a single employee can cost up to 200% of their annual salary. This project analyzes IBM HR data to uncover the key drivers behind employee attrition, helping HR teams make data-driven decisions to improve retention.

---

## Key Findings

| Finding | Detail |
|---|---|
| Overall attrition rate | 16.1% (237 out of 1,470 employees) |
| Overtime employees | 3× more likely to leave (30.5% vs 10.4%) |
| Income gap | Leavers earn $2,046 less per month than stayers |
| Highest risk role | Sales Representatives at 39.8% attrition |
| Highest risk age group | 18–25 year olds at 35.2% attrition |
| Single employees | Leave at 25.5% vs 12% for married employees |

---

## Tools Used

- **Python (Pandas)** — data cleaning and feature engineering
- **SQLite (SQL)** — business question analysis
- **Power BI** — interactive dashboard with DAX measures
- **Excel** — column value mapping

---

## Project Structure

```
hr-attrition-analysis/
│
├── HR_Attrition_Cleaning.ipynb   # Data cleaning and feature engineering
├── HR_Attrition_SQL.ipynb        # SQL business questions and answers
├── HR_analytics_cleaned.csv      # Cleaned dataset exported from Python
├── HR_Dashboard.pdf              # Power BI dashboard export (3 pages)
└── README.md
```

---

## Workflow

```
Raw CSV  →  Jupyter + Pandas  →  SQL Analysis  →  Power BI Dashboard
```

**Step 1 — Python cleaning:**
- Dropped 4 useless columns (EmployeeCount, Over18, StandardHours, EmployeeNumber)
- Mapped numeric codes to readable labels (Education, JobSatisfaction, WorkLifeBalance)
- Engineered 4 new features: AgeGroup, IncomeGroup, TenureGroup, AttritionFlag

**Step 2 — SQL analysis:**
- Answered 8 structured business questions using SQLite
- Questions covered attrition by department, overtime, job satisfaction, income, distance, age, marital status, and job role

**Step 3 — Power BI dashboard:**
- Built 3 interactive pages with cross-page slicers
- Wrote 5 custom DAX measures
- Applied consistent color coding: red = left, blue = stayed

---

## Dashboard Pages

**Page 1 — Overview**
KPI cards, attrition by department, attrition by job role, donut chart, tenure comparison

**Page 2 — People & Job Factors**
Attrition by age group, marital status, overtime comparison, job satisfaction vs attrition, work-life balance vs attrition

**Page 3 — Compensation**
Income gap KPI, avg income by education (leavers vs stayers), distance from home by job role

---

## SQL Questions Answered

1. Which department has the highest attrition?
2. Does overtime cause attrition?
3. Avg distance from home by job role and attrition
4. Avg monthly income by education and attrition
5. Which age group leaves the most?
6. Does job satisfaction predict attrition?
7. Does marital status affect attrition?
8. Which job roles are highest risk?

---

## Dataset

IBM HR Analytics Employee Attrition dataset — fictional data created by IBM data scientists. 1,470 rows, 35 columns. No nulls.

---

## How to Run

1. Clone this repository
2. Open `HR_Attrition_Cleaning.ipynb` in Jupyter and run all cells
3. Open `HR_Attrition_SQL.ipynb` to run SQL queries
4. Open Power BI Desktop and load `HR_analytics_cleaned.csv`
5. Recreate the dashboard or view `HR_Dashboard.pdf`

---

*This project was built for portfolio and learning purposes.*
