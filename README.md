# Sales-data-Task-7

# 🧾 Task 7: Basic Sales Summary Using SQLite & Python

Analyze basic sales performance using SQL inside Python and visualize the output using a simple bar chart.

## 📦 Dataset
- **Database**: `sales_data.db`
- **Table**: `sales`
- **Fields**:
  - `product`: Product name
  - `quantity`: Quantity sold
  - `price`: Price per unit

## 🎯 Objective
- Calculate:
  - Total quantity sold per product
  - Total revenue per product (`quantity * price`)
- Visualize revenue using a bar chart.

## 🛠️ Tools Used
- Python (`sqlite3`, `pandas`, `matplotlib`)
- SQLite (no setup needed — built into Python!)

## 📜 SQL Query
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
