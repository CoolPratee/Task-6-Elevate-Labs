Sales Trend Analysis – Monthly Revenue & Orders
Overview
This project analyzes monthly revenue and order volumes from an e-commerce dataset. The goal is to identify sales patterns and trends using SQL aggregation functions.

Dataset
online_sales_original_dataset.csv contains:

order_id – Unique order reference

order_date – Purchase date

amount – Order revenue

product_id – Product identifier

Sample data covers the year 2023 with realistic variations.

Key Query (SQLite Example)
sql
Copy
Edit
SELECT
    STRFTIME('%Y', order_date) AS order_year,
    STRFTIME('%m', order_date) AS order_month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS total_orders
FROM online_sales
GROUP BY order_year, order_month
ORDER BY order_year, order_month;
Deliverables
Dataset: online_sales_original_dataset.csv

Aggregated Results: monthly_sales_results.csv

SQL Script: sales_trend_analysis.sql

Database: online_sales.sqlite

Insights
Reveals monthly revenue and order trends

Identifies peak and low-performing months

Useful for business decision-making and forecasting
