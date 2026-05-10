# HR Analytics Dashboard

## 📌 Project Overview
This project focuses on analyzing employee and HR operational data to generate actionable business insights through interactive dashboards and KPI tracking.

The dashboard was built using **Power BI** and designed to help HR teams monitor:
- Employee distribution
- Attrition trends
- Performance metrics
- Salary analysis
- Workforce demographics
- HR KPIs

The goal of this project is to demonstrate how HR data can support better decision-making in recruitment, employee retention, and workforce management.

---

# 🎯 Objectives
- Analyze employee workforce data
- Track HR KPIs and trends
- Identify attrition patterns
- Monitor employee performance
- Visualize salary and demographic insights
- Build an interactive HR analytics dashboard

---

# 🛠 Tools & Technologies
- Power BI
- DAX
- Excel / CSV Dataset
- Data Cleaning & Transformation
- Business Analytics
- Statistical Analysis

---

# 📊 Key Features

## Employee Overview
- Total Employees
- Active Employees
- Gender Distribution
- Department-wise Employee Count

## Attrition Analysis
- Attrition Rate
- Attrition by Department
- Attrition by Age Group
- Attrition by Salary

## Salary Analysis
- Average Salary
- Salary Distribution
- Salary Comparison Across Departments

## Performance Analysis
- Employee Performance Score
- Satisfaction Score
- Overtime & Absence Tracking

## Workforce Demographics
- Age Bucket Analysis
- Experience Distribution
- Education Background

---

# 📈 KPIs Used
- Headcount
- Attrition Rate
- Average Salary
- Employee Satisfaction
- Average Performance Score
- Absenteeism
- Retention Analysis

---

# 📂 Dataset Information
The dataset contains HR-related employee information such as:
- Employee ID
- Age
- Gender
- Department
- Salary
- Date of Hire
- Performance Score
- Satisfaction Score
- Attrition Status
- Overtime
- Absences

---

# 🧠 DAX Concepts Used

```DAX
Average Salary = AVERAGE(HRDataset_v14[Salary])

Age Bucket =
SWITCH(
    TRUE(),
    HRDataset_v14[Age] >= 18 && HRDataset_v14[Age] <= 25, "18-25",
    HRDataset_v14[Age] >= 26 && HRDataset_v14[Age] <= 35, "26-35",
    HRDataset_v14[Age] >= 36 && HRDataset_v14[Age] <= 45, "36-45",
    HRDataset_v14[Age] >= 46 && HRDataset_v14[Age] <= 55, "46-55",
    HRDataset_v14[Age] >= 56, "55+"
)

# 📌 Business Insights

- Certain departments show higher attrition trends
- Younger employees demonstrate higher turnover rates
- Salary and satisfaction scores influence retention
- Performance varies across departments and experience levels

---

# 🚀 Project Outcome

This project demonstrates practical skills in:

- HR Analytics
- Dashboard Development
- Business Intelligence
- Data Visualization
- Data-Driven Decision Making

---

# 📷 Dashboard Preview

