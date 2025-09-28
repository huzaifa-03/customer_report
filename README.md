📝 Customer Segmentation Report (SQL)
📌 Project Overview

This project builds a Customer Segmentation Report in SQL Server using data from Sales and Customers tables.
The report provides key customer insights such as demographics, transactions, and behavioral segmentation to support exploratory data analysis (EDA) and business decision-making.

🎯 Objectives

Retrieve and consolidate customer-level data.

Perform aggregations on transactions (orders, sales, products, etc.).

Segment customers into meaningful groups (e.g., VIP, Regular, New).

Calculate customer KPIs including recency, average order value, and monthly spend.

🗂️ Key Features

Base Query

Extracts customer demographics (name, age).

Joins customer data with sales transactions.

Customer Aggregation

Computes total orders, sales, products purchased, and customer lifespan.

Identifies the last purchase date per customer.

Customer Segmentation & KPIs

Age Groups: Under 20, 20-29, 30-39, 40-49, 50 and above.

Segments:

VIP: Lifespan ≥ 12 months & total sales > 5000

Regular: Lifespan ≥ 12 months & total sales ≤ 5000

New: Less than 12 months

KPIs Calculated:

Recency (months since last order)

Average Order Value (AOV)

Average Monthly Spend

📊 Output Columns
Column Name	Description
customer_key	    Unique customer identifier
customer_number	  Customer reference number
customer_name	    Full name of customer
age	              Customer age (in years)
age_group	        Categorized age range
customer_segment	Customer type (VIP, Regular, New)
last_order_date	  Most recent purchase date
recency	          Months since last purchase
total_orders	    Total distinct orders
total_sales	      Total sales value
total_quantity	  Total items purchased
total_products	  Distinct products purchased
lifespan	        Customer active months
avg_order_value	  Sales ÷ Orders
avg_monthly_spend	Sales ÷ Lifespan


🛠️ SQL Script

The view is created as:

CREATE VIEW customer_segmentation AS
-- (code provided in repository)


You can query the segmentation results with:

SELECT * FROM customer_segmentation;

🚀 Use Cases

Marketing Teams → Identify and target VIP or New customers.

Business Analysts → Monitor sales patterns and customer recency.

Management → Track customer value and improve retention strategies.

📂 Repository Structure
📁 Exploratory_Data_Analysis
 ┣ 📄 customer_segmentation.sql   # SQL script for the report
 ┣ 📄 README.md                   # Documentation

✅ Requirements

SQL Server (tested on MS SQL Server)

Database: Exploratory_Data_Analysis

Tables: sales, customers

📢 Author
Developed as part of Exploratory Data Analysis (EDA) with SQL to demonstrate customer segmentation reporting.
