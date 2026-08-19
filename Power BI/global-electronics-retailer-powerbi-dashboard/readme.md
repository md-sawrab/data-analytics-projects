# Global Electronics Retailer — Power BI Dashboard

An end-to-end Power BI dashboard analyzing sales, profit, and customer performance for a global electronics retailer. The dashboard combines an executive overview with deeper drill-downs into customer behavior, product performance, and channel (online vs. offline) analysis.

## 📊 Dashboard Overview

This project transforms raw transactional data into an interactive, decision-ready dashboard, covering:

- **Executive KPIs** — Total Sales, Total Profit, Total Orders, Total Customers, Profit Margin %, all with Year-over-Year comparisons
- **Customer Analysis** — New vs. Returning Customers, Repeat Rate, Average Orders per Customer, Average Revenue per Customer, Age Group segmentation
- **Product Performance** — Revenue & Profit by Product, Product Sold Rate, Average Selling Price, custom tooltips with product-level trend charts
- **Store & Channel Analysis** — Revenue & Profit by Store Size, Online vs. Offline sales comparison
- **Time Intelligence** — YoY, MTD, and trend analysis using a custom Calendar table

## 🗂️ Data Model

The project follows a **Star Schema** design:

| Table | Description |
|---|---|
| Sales (Fact) | Order-level transactional data |
| Customers (Dimension) | Customer demographics |
| Products (Dimension) | Product catalog, pricing, and cost |
| Stores (Dimension) | Store location and size |
| Calendar (Dimension) | Custom date table for time intelligence |
| Exchange Rates (Dimension) | Currency conversion rates |

## 🛠️ Tools Used

- **Power BI Desktop** — Data modeling, DAX, and visualization
- **Power Query (M)** — Data cleaning and transformation
- **DAX** — Custom measures for KPIs, time intelligence, and customer analytics

## 📐 Key DAX Concepts Implemented

- Time Intelligence functions (`SAMEPERIODLASTYEAR`, `PREVIOUSMONTH`, `TOTALYTD`)
- Customer segmentation logic (New vs. Returning Customers using `ALLEXCEPT` and `FILTER`)
- Dynamic report page tooltips with `HASONEVALUE`
- Custom sort ordering for categorical groups (Age Group, Store Size)
- Safe division handling with `DIVIDE()`

## 📁 Files

- `Global_Electronics_Retailer.pbix` — Main Power BI file
- `screenshots/` — Dashboard preview images

## 📌 Data Source

Global Electronics Retailer Dataset

## 🙋 Feedback

This project is a work in progress as I continue learning Power BI and DAX. Feedback and suggestions are always welcome!
