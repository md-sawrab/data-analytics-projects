### Excel PivotTable Dashboard Project
 
#### Project Overview
 
This project takes raw order-level sales data and turns it into an interactive Excel dashboard using PivotTables, PivotCharts, Slicers, and a Timeline. I practiced this dashboard-building workflow using a sales dataset as the source.
 
#### Business Scenario
 
Working with order-level sales data, the goal was to build a dashboard to review:
- Total Revenue, Total Orders, Quantity Sold, Average Order Value
- Monthly Sales Trend
- Performance by Region, Product Category, and Sales Channel
- Top-selling Products

#### Workbook Sheets
 
| Sheet | Purpose |
|---|---|
| **Start_Here** | Project overview and instructions |
| **Dashboard_Plan** | Explains the data columns, key data-quality checks performed, and the plan mapping business questions to dashboard elements and the columns used |
| **Sales_Data** | Raw sales data (2000+ rows) |
| **Supporting_Pivots** | PivotTables built to power the KPI cards and charts |
| **Sales_Dashboard** | Final interactive dashboard |
 
#### Sales_Data Columns
 
`Order ID`, `Date`, `Region`, `Sales Channel`, `Customer Type`, `Product Category`, `Product`, `Salesperson`, `Quantity`, `Unit Price`, `Discount`, `Revenue`
 
#### Steps I Followed
 
1. Reviewed the raw data in **Sales_Data** and checked for data-quality issues (blank headers, blank rows, dates recognized correctly, numeric columns truly numeric, consistent category/region spelling).
2. Planned the dashboard requirements in **Dashboard_Plan** — mapping each business question to a dashboard element and the source columns.
3. Built **Supporting_Pivots** — PivotTables behind each KPI card and chart.
4. Assembled the final **Sales_Dashboard** with KPI cards, charts, slicers, and a timeline for interactive filtering.
