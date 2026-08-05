# Well-Life General Hospital — Strategic Health Insights Report
### Patient Admissions & Diagnosis Analysis (2021–2024) | Isaac Okolie | Power BI

---

## The Business Context

Well-Life General Hospital compiled four years of patient admission records covering
10,000 patients across seven diagnoses. Hospital management needed a structured,
data-driven view of what had happened — who was being admitted, for what conditions,
in what patterns, and how the picture had changed over time.

Without this visibility, decisions about staffing, capacity, pharmaceutical
procurement, and community outreach were being made without evidence. This
engagement built that evidence — and revealed that the hospital's patient
population has undergone a fundamental shift that demands a strategic response.

---

## The Business Problem

Three specific operational gaps were identified:

**1. Resource allocation was disconnected from actual patient demand.**
Chronic disease admissions were rising while capacity and staffing remained
aligned to infectious disease management — the historical profile, not the
current one.

**2. Seasonal planning was reactive.**
Q1 consistently produced the highest admission volumes every year — but without
a visible pattern, the hospital could not prepare in advance.

**3. Demographic shifts were not being captured.**
The average patient age rose from 39 to 48 over four years. Services designed
for the 2021 patient were increasingly misaligned with the 2024 patient.

A second challenge was structural: patient data was stored across separate files.
Without a connected data model, analysis would produce inaccurate counts and
incomplete insights. Stage 2 of the brief addressed this by building a proper
Power BI star schema.

---

## Project Objectives

- **Describe** total patient admissions across the four-year period
- **Map** the disease landscape by diagnosis, category, and trend
- **Profile** patients by age range and gender across all conditions
- **Detect** seasonal admission patterns by quarter and year
- **Track** year-on-year growth in admissions and its connection to changing demographics
- **Build** a connected star schema data model in Power BI for accurate reporting

---

## Dataset Overview

| Property | Detail |
|----------|--------|
| Total Records | 10,000 patient admissions |
| Time Period | 2021 – 2024 (1,460 days) |
| Diagnoses | 7 — Asthma, Diabetes, Hypertension, Malaria, Stroke, Typhoid, Ulcer |
| Categories | Chronic (5 conditions) | Infectious (2 conditions) |
| Source | SkillAhead WellLife Hospital Patient Records (.xlsx) |
| Tool | Microsoft Power BI |
| Data Model | Star schema — Patient Records (fact), Diagnosis table, Calendar table |

**Key Fields:** Patient_ID, Age, Diagnosis, Gender, Admission_Date

---

## Key KPIs

| Metric | Value |
|--------|-------|
| Total Patients | 10,000 |
| Average Age | 44 years |
| Diagnosis Count | 7 |
| Days Analyzed | 1,460 |
| Male Patients | 5,681 (56.81%) |
| Female Patients | 4,319 (43.19%) |
| Growth 2021–2024 | +132% (1,409 → 3,266) |

---

## Diagnosis Distribution

| Rank | Diagnosis | Patients | Category |
|------|-----------|---------|---------|
| #1 | Typhoid | 1,487 | Infectious |
| #2 | Asthma | 1,440 | Chronic |
| #3 | Ulcer | 1,439 | Chronic |
| #4 | Malaria | 1,436 | Infectious |
| #5 | Diabetes | 1,407 | Chronic |
| #6 | Hypertension | 1,401 | Chronic |
| #7 | Stroke | 1,390 | Chronic |

> Note: Typhoid leads the overall count, but by 2024 stroke had become the
> top annual diagnosis — reflecting the shift from infectious to chronic disease.

---

## Age Distribution

| Age Range | Patients | % of Total |
|-----------|---------|-----------|
| 11–20 years | 287 | 2.9% |
| 21–30 years | 2,023 | 20.2% |
| **31–40 years** | **2,353** | **23.5% — Largest group** |
| 41–50 years | 1,789 | 17.9% |
| 51–60 years | 1,796 | 18.0% |
| 61–70 years | 1,302 | 13.0% |
| 71–80 years | 450 | 4.5% |

---

## Year-on-Year Trends

| Year | Patients | Growth | Top Diagnosis | Avg Age |
|------|---------|--------|--------------|---------|
| 2021 | 1,409 | Baseline | Typhoid (445) | 39 yrs |
| 2022 | 2,292 | +62.7% | Typhoid (470) | 41 yrs |
| 2023 | 3,033 | +32.3% | Typhoid (451) | 44 yrs |
| 2024 | 3,266 | +7.7% | **Stroke (586)** | 48 yrs |

---

## Key Insights

**1. The hospital's patient profile has fundamentally changed**
Stroke overtook typhoid as the leading diagnosis in 2024. Average patient age
rose from 39 to 48 in four years. The hospital designed for infectious disease
management is now primarily serving a chronic disease population.

**2. Q1 is predictably the most demanding quarter**
Every year without exception, Q1 produced the highest admission volumes.
Post-holiday diet, deferred checkups, and cold-season stress drive this pattern.
Four years of data confirms this is not noise — it is a standing operational reality.

**3. The 31–40 age group is the highest-demand segment**
Working-age adults aged 31–40 represent the hospital's largest patient cohort
(23.5%). They are at the early onset of chronic conditions — the optimal
intervention point before disease complexity escalates.

**4. Male patients arrive later with more advanced conditions**
Men outnumber women by 1,362 admissions but present at an average age three
years older than female patients. This age gap signals delayed care-seeking
in the male population — resulting in more advanced conditions at admission.

**5. The decline in typhoid and malaria needs investigation before action**
Typhoid's seasonal Q4 peak disappeared entirely in 2024. This could reflect
genuine public health improvement — or patients choosing other facilities.
The hospital cannot know without community-level data.

---

## Business Recommendations

| Recommendation | Expected Impact |
|---------------|----------------|
| Expand chronic care for stroke, diabetes, hypertension | 30% increase in chronic capacity; fewer emergency cases from unmanaged conditions |
| Build a Q1 operational protocol | 25% fewer medicine shortages; faster treatment during peak season |
| Launch 31–40 age group preventive programs | 25% more visits from largest patient segment; earlier chronic disease detection |
| Design gender-specific health campaigns | 20% more male chronic screenings; 30% rise in female preventive attendance |
| Investigate typhoid/malaria decline | Evidence-based resource reallocation — not assumptions |

---

## Data Model (Stage 2)

Power BI star schema with three connected tables:

| Table | Role | Key |
|-------|------|-----|
| Patient Records | Fact table | Patient_ID (primary), Diagnosis (foreign), Admission_Date (foreign) |
| Diagnosis Table | Dimension | Diagnosis name, Category (Chronic/Infectious) |
| Calendar Table | Dimension | Date, Year, Quarter, Month |

**Relationships:** One-to-many from Calendar → Patient Records and
Diagnosis → Patient Records, with filters flowing from dimensions to fact.

---

## Dashboard Features

**4-page Power BI dashboard:**

| Page | Purpose | Key Visuals |
|------|---------|------------|
| Model | Data relationship view | Star schema diagram with relationship indicators |
| Analysis | Tabular drill-down | Year/quarter patient counts by condition |
| Visual | Pattern exploration | Age, gender, time-series, Chronic vs Infectious toggle |
| Dashboard | Executive summary | KPI cards, diagnosis sidebar filter, gender donut, age range bars, year buttons |

**Interactive features:** Year filter (2021–2024), Diagnosis sidebar filter,
Chronic/Infectious toggle, Patient Name search field.

---

## Skills Demonstrated

| Skill | Application |
|-------|------------|
| Power Query | Imported Excel data, extracted Year/Quarter, validated 10,000 records |
| Data Modeling | Built star schema with correct one-to-many relationships and filter direction |
| DAX Measures | Total Patients, Average Age, Diagnosis Count, Chronic/Infectious aggregations |
| Dashboard Design | 4-page interactive dashboard serving both management and clinical audiences |
| FIRE Framework | Facts → Insights → Recommendations → Expected Outcomes for all 5 tasks |
| Business Translation | Demographic shift narrative connecting data patterns to operational strategy |

---

## Limitations

- Five fields only — no treatment outcome, length of stay, or cost data
- Descriptive analysis only — explains what happened, not why
- Does not distinguish new from returning patients
- No financial data to quantify the business impact of the chronic disease shift
- Community-level context not available to explain infectious disease trends

---

## Future Improvements

- Integrate treatment outcome and discharge data for quality-of-care analysis
- Add financial data to measure cost and revenue impact by diagnosis
- Build predictive admission forecasts using 4-year quarterly trend data
- Incorporate community health data to assess the hospital's market share
- Patient journey tracking to follow how conditions evolve across multiple visits

---

## 📁 Project Structure

```
WellLife-Hospital-Analytics/
│
├── README.md
├── WellLife_Hospital_Analytics_Report.pdf
├── SkillAhead_WellLife_Hospital_Patient_Records.xlsx
├── 1_Business_Brief.pdf
├── 2_Business_Brief.pdf
└── screenshots/
    └── dashboard.png
```

---

## 👤 About Me

**Isaac Okolie**
Data Analyst & Data Analytics Tutor | Nigeria

This project demonstrates end-to-end healthcare analytics — from multi-table
data modeling and Power BI dashboard design to demographic trend analysis and
strategic recommendations framed through the FIRE methodology. Every insight
connects directly to a business action. Every recommendation is supported by
the data.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/isaac-okolie)

---

*Well-Life General Hospital | SkillAhead Analytics | Power BI | 2021–2024*
