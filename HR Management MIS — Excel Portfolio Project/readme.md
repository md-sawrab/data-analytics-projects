# HR Management MIS — Excel Portfolio Project

A complete, formula-driven HR Management Information System built entirely in Microsoft Excel (2019-compatible). This project simulates a real company's HR operations — employee records, attendance, leave, payroll, performance, and recruitment — tied together with 60+ formulas and a live dashboard.

## 📌 Project Overview

- **30 employees** across 6 departments (Sales, Marketing, Finance, IT, HR, Operations)
- **2 years of historical data** (Jan 2024 – Dec 2025)
- **1,300+ transactional records** across attendance and payroll
- **9 interconnected sheets**, each feeding into a central Calculations layer and a live Dashboard

## 🗂️ Sheet Structure

| Sheet | Purpose |
|---|---|
| `Lists` | Backend source lists for all dropdown data validation |
| `Employee_Master` | Core employee records — ID, department, designation, salary, joining/exit dates |
| `Attendance_Log` | Monthly attendance (days present vs working days) per employee |
| `Leave_Records` | Leave applications with type, duration, and approval status |
| `Payroll` | Monthly salary, bonus, deductions, and net pay |
| `Performance_Reviews` | Annual performance ratings (2024 & 2025) |
| `Recruitment_Pipeline` | Candidate tracking through hiring stages |
| `Calculations` | Backend formula layer — all analysis happens here |
| `Dashboard` | Final visual summary — KPIs, charts, rankings |

## ⚙️ Functions Used

**Lookup & Reference**
`VLOOKUP`, `INDEX`, `MATCH`

**Conditional Aggregation**
`SUMIFS`, `COUNTIFS`, `AVERAGEIFS`

**Logical**
`IF`, `IFS`, `AND`, `IFERROR`

**Date & Time**
`DATEDIF`, `TODAY`, `WEEKDAY`, `NETWORKDAYS`

**Statistical**
`MEDIAN`, `STDEV.S`, `LARGE`, `SMALL`, `PERCENTILE`, `QUARTILE`

**Information / Data Quality**
`ISBLANK`, `ISNUMBER`, `ISTEXT`, `ISERROR`, `ISNA`

## 📊 Dashboard Features

- **KPI Cards** — Active employees, attrition count & rate, average attendance, average performance rating
- **Department-Wise Summary** — Headcount, average salary, attendance, and rating per department (with heatmap conditional formatting)
- **Top 5 Performers** — Auto-ranked by performance rating using `LARGE` + `INDEX`/`MATCH`
- **Recruitment Pipeline Breakdown** — Candidate count by hiring stage
- **Charts** — Department headcount (bar) and recruitment pipeline (pie)

## ✅ Data Validation

Dropdown lists applied to prevent bad data entry:
- `Employee_Master`: Department, Status, Gender
- `Leave_Records`: Leave Type, Leave Status
- `Recruitment_Pipeline`: Hiring Stage

## 🧠 What This Project Demonstrates

- Structuring raw, multi-sheet business data into a clean analytical model
- Cross-sheet lookups and conditional aggregation at scale (1,000+ rows)
- Building KPIs and visual reporting entirely from formulas — no manual calculation
- Data quality validation using information functions
- Excel 2019 compatibility awareness (avoiding 365-only functions like `XLOOKUP`, `FILTER`, `UNIQUE`)

## 🔜 Next Steps

- Add Pivot Tables for deeper ad-hoc analysis
- Expand to Power Query for automated data refresh
- Explore basic VBA/macros for one-click report generation

---
*Built as a hands-on practice project after completing a 9-chapter Excel formula review (Math, Logical, Text, Lookup, Conditional, Date/Time, Statistical, Information, Dynamic Array functions).*
