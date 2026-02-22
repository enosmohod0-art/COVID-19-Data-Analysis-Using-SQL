# 🌍 Global COVID-19 Data Analysis (SQL Server)

## 📌 Project Overview

This project presents a structured SQL Server analysis of global COVID-19 data (2020–2021), focusing on infection rates, case fatality rates, global trends, and vaccination rollout progress.

The objective was to analyze large-scale time-series data to understand pandemic severity across countries and evaluate vaccination progress using advanced SQL techniques.

---

## 🗂 Dataset Description

**Source:** Public global COVID-19 dataset (educational analysis dataset)

**Database Used:** SQL Server (SSMS)

**Tables Used:**
- `CovidDeaths`
- `CovidVaccinations`

**Record Count:**
- ~85,000+ daily country-level records
- Covers global data across 2020–2021
- Location-wise, date-wise tracked metrics

The dataset includes:
- Total & new cases
- Total & new deaths
- Population data
- Vaccination counts
- Daily updates per country

---

## 🎯 Analysis Objectives

- Calculate country-level case fatality rates
- Compare infection rates relative to population
- Analyze global death percentage trends over time
- Identify highest impacted countries
- Track rolling vaccination progress using window functions
- Compare vaccination coverage across nations

---

## 🛠 Tools & Techniques

- SQL Server (SSMS)
- Data cleaning & type casting
- Aggregations (SUM, MAX)
- Percentage calculations
- Date-based trend analysis
- Window Functions (`SUM() OVER()`)
- CTEs (Common Table Expressions)

---

## 🔎 Key Analysis Performed

### 1️⃣ Case Fatality Rate (Death %)

Calculated death percentage using:

```
(total_deaths / total_cases) * 100
```

**Key Findings:**
- Yemen recorded one of the highest death percentages (~25.94%)
- Singapore recorded one of the lowest (~0.05%)
- India’s overall death percentage was ~1.45%

---

### 2️⃣ Global Death Percentage Trend

- During mid-2020, global death percentage peaked at ~6–7%
- After mid-2020, fatality rates declined steadily
- By late 2020 / early 2021, global death % stabilized around 2–2.5%
- Indicates improved treatment response and healthcare adaptation

---

### 3️⃣ Infection Rate vs Population

Calculated infection penetration:

```
(total_cases / population) * 100
```

**Key Findings:**
- Andorra showed the highest infection rate (~17.12%)
- Montenegro, San Marino, Luxembourg also reported high infection ratios (12–15%)
- Demonstrates varying pandemic spread intensity across nations

---

### 4️⃣ Vaccination Progress Analysis

Used window functions to calculate rolling vaccination totals:

```
SUM(new_vaccinations) OVER (PARTITION BY location ORDER BY date)
```

Insights:
- Measured cumulative vaccination rollout
- Calculated vaccination percentage relative to population
- Enabled country-wise vaccination progress comparison

---

## 📈 Project Highlights

- Worked with ~85K+ time-series records
- Performed multi-table joins across death & vaccination datasets
- Applied rolling aggregations for vaccination modeling
- Conducted global, continent, and country-level comparisons
- Extracted meaningful epidemiological insights from raw data

---

## 📂 Repository Structure

```
Global-COVID-19-Data-Analysis-SQL
│
├── sql/
│   └── global_covid_analysis.sql
├── presentation/
│   └── Global_COVID_Analysis.pdf
└── README.md
```

---

## 🚀 Outcome

This project demonstrates:

- Strong SQL-based time-series analysis capability  
- Ability to analyze global-scale datasets  
- Proficiency in percentage modeling and trend analysis  
- Competency in window functions and advanced aggregations  
- Data storytelling using structured insights  

---

## 👤 Author

**Enos Mohod**  
Aspiring Data Analyst | SQL | Power BI | Python  
Turning global data into structured analytical insights
