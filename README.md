# Task_7-Get-Basic-summary-from-a-Tiny-SQLite-Database-using-python
Basic Sales Summary using Python, SQLite, pandas, and matplotlib. Task 7 for Data Analyst Internship — create a sales database, run SQL queries, and visualize revenue.


# Task 7 – Basic Sales Summary (Data Analyst Internship)

This project is part of a Data Analyst Internship. The goal is to extract and visualize basic sales data using SQL within Python. It demonstrates connecting to an SQLite database, running SQL queries, and plotting the results using matplotlib.

---

## 📌 Task Objective

- Use SQLite inside Python to pull basic sales summary info.
- Show total quantity and revenue by product.
- Display the output using print and a simple bar chart.


## 🛠 Tools Used

- Python
- SQLite (sqlite3 module)
- pandas
- matplotlib


## 📂 Files Included

-  Sales summary.pdf: The main Python script
- Sales_Data_Task7.xlsx: SQLite database with 20 rows of sales data
- README.md: Project documentation


## 🧾 Sales Data Sample

The data includes 20 rows with products like:

- Laptop
- Mouse
- Keyboard
- Monitor
- Headphones

Each row contains:
- product
- quantity
- price


## 🧠 What the Script Does

1. Connects to an SQLite database.
2. Creates a sales table.
3. Inserts 20 sample sales records.
4. Runs an SQL query to:
   - Group data by product
   - Calculate total quantity and total revenue
5. Displays the summary using print().
6. Plots a revenue bar chart using matplotlib.


## 📊 SQL Query Used

```sql
SELECT 
    product, 
    SUM(quantity) AS total_quantity, 
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
