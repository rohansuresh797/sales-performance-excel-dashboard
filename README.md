# Sales Performance Dashboard — Excel

An interactive sales analysis dashboard built in Microsoft Excel using PivotTables, PivotCharts, and a consolidated dashboard view. The project takes raw transactional sales data and turns it into a single-screen executive summary covering monthly trends, salesperson performance, product category share, and profit by city.

## Overview

The source data is a year of order-level transactions (one row per order) containing date, region, city, product category, product, quantity, unit price, total price, and salesperson. From this raw table, five PivotTables/PivotCharts were built and then combined into one dashboard sheet.

**Workbook tabs:**
| Sheet | Purpose |
|---|---|
| `Dashboard` | Consolidated view of all charts and the product summary table |
| `Sales Data` | Raw transaction table (with a derived `Month` column) |
| `Sales by Month` | PivotTable + line chart of monthly revenue trend |
| `Sales by Salesperson` | PivotTable + bar chart ranking reps by revenue |
| `Items Sold by Category` | PivotTable + pie chart of unit sales share by category |
| `Sales Profit by City` | PivotTable + pie chart of revenue share by city |
| `Sales by Product Type` | PivotTable summary table (quantity by product), embedded in the dashboard |

## Build process

1. **Prep the data** — Converted the raw range (`A1:I23` and beyond) into a formatted Excel Table to support dynamic PivotTable refresh and chart creation.
2. **Derive a Month field** — Inserted a new column to the left of `Region`, named it `Month`, and used `=TEXT(A2,"mmm")` to extract a three-letter month label from each order date, then filled it down the table.
3. **Sales by Month** — Built a PivotTable (`TotalPrice` → Values, `Month` → Rows) on a new sheet named *Sales by Month*. Formatted the values as Currency with 0 decimal places, then inserted a line chart next to the PivotTable. Adjusted the chart's vertical axis minimum from 0 to 500 so the monthly trend line is easier to read.
4. **Sales by Salesperson** — Built a second PivotTable (`TotalPrice` → Values, `Salesperson` → Rows), formatted as currency, and sorted largest to smallest. Inserted a clustered bar chart and set the vertical axis to display categories in reverse order so the top performer appears at the top of the chart.
5. **Items Sold by Category** — Built a PivotTable (`Quantity` → Values, `Category` → Rows) and changed the value display to "% of Grand Total." Visualized it as a pie chart showing each category's share of total units sold.
6. **Sales Profit by City** — Built a PivotTable (`TotalPrice` → Values, `City` → Rows) and visualized it as a pie chart showing each city's share of total revenue.
7. **Sales by Product Type** — Built a final PivotTable (`Quantity` → Values, `Product` → Rows) on its own sheet to use as a supporting summary table on the dashboard.
8. **Assemble the dashboard** — Created a new sheet, selected the entire sheet (Ctrl+A) and applied a uniform fill color as a clean background, then placed the Sales by Month, Sales by Salesperson, Items Sold by Category, and Sales Profit by City charts onto it, along with a copy of the Sales by Product Type table.

## Key insights

- **Trend:** Monthly revenue ranged from a low of $926 (Feb) to a peak of $2,309 (Jun), with a generally choppy but upward-leaning pattern across the year. Total revenue for the period: **$17,989**.
- **Top performer:** Marc Williams led all salespeople with **$4,896** in sales, more than 50% ahead of the second-place rep, Emily Moore ($3,152).
- **Category mix:** Cookies (43.5%) and Bars (38.4%) together account for roughly 82% of all units sold; Crackers and Snacks make up the remainder.
- **Geography:** Boston generated the largest share of profit at **36.1%**, followed by New York (29.0%), Los Angeles (22.9%), and San Diego (11.9%).
- **Top product by volume:** Carrot was the best-selling product at 2,456 units, ahead of Arrowroot (1,220) and Oatmeal Raisin (1,281).

## Skills demonstrated

PivotTables · PivotCharts (line, clustered bar, pie) · calculated text fields (`TEXT` function) · custom number formatting (currency, percentage) · chart axis customization · dashboard design and layout in Excel.

## Files

- `Sales_Performance_MIS_Dashboard.xlsx` — the full workbook with all sheets, PivotTables, and the dashboard
- `screenshots/` — reference images of the dashboard and each supporting sheet

## Screenshots

Add the dashboard and sheet screenshots to a `screenshots/` folder in the repo and reference them here, for example:

```markdown
![Dashboard](screenshots/dashboard_view.png)
```
