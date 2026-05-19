# HR Employee Attrition Analysis
### Python · SQL · Power BI

> Identifying why employees leave using data — and what companies can do about it.



## Problem Statement

Employee attrition is costly — replacing a single employee can cost up to 200% of their annual salary. This project analyzes IBM HR data to uncover the key drivers behind employee attrition, helping HR teams make data-driven decisions to improve retention.



## Key Findings

| Finding | Detail |
|---|---|
| Overall attrition rate | 16.1% (237 out of 1,470 employees) |
| Overtime employees | 3× more likely to leave (30.5% vs 10.4%) |
| Income gap | Leavers earn $2,046 less per month than stayers |
| Highest risk role | Sales Representatives at 39.8% attrition |
| Highest risk age group | 18–25 year olds at 35.2% attrition |
| Single employees | Leave at 25.5% vs 12% for married employees |



## Tools Used

- **Python (Pandas)** — data cleaning and feature engineering
- **SQLite (SQL)** — business question analysis
- **Power BI** — interactive dashboard with DAX measures
- **Excel** — column value mapping


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
<img width="1321" height="737" alt="Screenshot 2026-05-19 210726" src="https://github.com/user-attachments/assets/d8c3b132-10ee-461f-8161-f078229594f5" />


**Page 2 — People & Job Factors**
Attrition by age group, marital status, overtime comparison, job satisfaction vs attrition, work-life balance vs attrition
<img width="1321" height="737" alt="Screenshot 2026-05-19 210744" src="https://github.com/user-attachments/assets/ad4cf68c-3c82-4477-9511-c9056659aadc" />


**Page 3 — Compensation**
Income gap KPI, avg income by education (leavers vs stayers), distance from home by job role
<img width="1318" height="735" alt="Screenshot 2026-05-19 210804" src="https://github.com/user-attachments/assets/efdc1fcc-e751-48f6-8a9c-c136b98e6708" />


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
