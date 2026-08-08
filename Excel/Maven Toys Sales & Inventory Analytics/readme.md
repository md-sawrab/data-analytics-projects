# Maven Toys Sales & Inventory Analytics (Excel / Power Pivot)

An end-to-end retail analytics project for a fictional toy retailer, **Maven Toys**, built entirely in Excel using Power Pivot, DAX measures, and PivotChart-based dashboards.

## 📁 Dataset

Raw CSV files (Data Model source, connected via Power Pivot):

| File | Rows | Description |
|---|---|---|
| `sales.csv` | 829,262 | Transaction-level sales: Sale_ID, Date, Store_ID, Product_ID, Units |
| `products.csv` | 35 | Product catalog: Name, Category, Cost, Price |
| `stores.csv` | 50 | Store master: Name, City, Location type, Open Date |
| `inventory.csv` | 1,593 | Store × Product stock snapshot: Stock_On_Hand |
| `calendar.csv` | 638 | Date dimension table |

## 🗂️ Data Model

Star schema built in Power Pivot:

```
              Stores (1)
             /          \
         Sales (*)     Inventory (*)
             \          /
              Products (1)

         Calendar (1) → Sales (*)   [Date]
```

- `Stores[Store_ID]` → `Sales[Store_ID]`
- `Stores[Store_ID]` → `Inventory[Store_ID]`
- `Products[Product_ID]` → `Sales[Product_ID]`
- `Products[Product_ID]` → `Inventory[Product_ID]`
- `Calendar[Date]` → `Sales[Date]`

> Sales and Inventory are never related directly — both are "many"-side fact tables and connect only through Stores/Products to avoid ambiguous filter paths.

## 📐 Key DAX Measures

```DAX
Total Revenue        = SUM(Sales[Revenue])
Total Units Sold      = SUM(Sales[Units])
Total Cost            = SUM(Sales[Cost])
Total Profit          = SUM(Sales[Profit])
Profit Margin %       = DIVIDE([Total Profit], [Total Revenue])
Total Transactions    = DISTINCTCOUNT(Sales[Sale_ID])

Total Stock On Hand   = SUM(Inventory[Stock_On_Hand])
Total Stock Value     = SUMX(Inventory, Inventory[Stock_On_Hand] * RELATED(Products[Product_Cost]))
Out of Stock Count    = CALCULATE(COUNTROWS(Inventory), Inventory[Stock_On_Hand] = 0)
Low Stock Count       = CALCULATE(COUNTROWS(Inventory), Inventory[Stock_On_Hand] > 0 && Inventory[Stock_On_Hand] < 10)
Stock to Sales Ratio  = DIVIDE([Total Stock On Hand], [Total Units Sold])

Total Stores          = DISTINCTCOUNT(Stores[Store_ID])
```

## 📊 Dashboard Pages

**1. Executive Overview** — Total Revenue, Profit, Margin %, Units Sold, Transactions; monthly revenue trend; revenue by weekday/quarter; revenue by city; top 10 stores.

**2. Store Performance** — Top 10 stores by revenue/profit, revenue by store location type, store age vs. revenue, full sortable store table.

**3. Product Analysis** — Revenue by category, top/bottom 10 products, profit margin by category, price vs. cost comparison, units sold vs. revenue scatter, price range distribution, full product mix table.

**4. Inventory Management** — Stock on hand, stock value, out-of-stock and low-stock counts, stock status breakdown, stock value by store/category, stock-to-sales ratio, fast-moving/low-stock restock alerts, conditional-formatted inventory table.

## 🛠️ Tools Used

- Excel (Power Pivot, Power Query, PivotTables/PivotCharts)
- DAX for calculated columns and measures
- Data Model with a star-schema relationship design

## 📌 Notes

- Composite key `Store_Product_Key` (`Store_ID & "-" & Product_ID`) used where a single-column relationship wasn't available.
- Grand Total rows are excluded from category/time-series PivotCharts (Design → Grand Totals → Off) to avoid skewing chart scale.
- Top N filters applied to any store- or product-level chart, since the dataset has 50 stores and 35 products.

## 📄 License

For portfolio/educational use.
