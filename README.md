# <img width="45" height="45" alt="image" src="https://github.com/user-attachments/assets/833ad067-5063-42fc-87a4-88215daaceb7" /> Apple iPhone Sales Analysis Dashboard

**Power BI | Data Analytics | Sales Insights | iPhone Market Trends**

This project analyzes Apple iPhone sales data to uncover trends in revenue, model performance, regional demand, year-wise growth, and customer purchasing patterns. The dashboard provides actionable KPIs and visual insights for sales teams, marketing analysts, and decision-makers.

---

## 📱 Project Overview

* Provides a detailed view of sales performance across **iPhone models, regions, years, and revenue segments**.
* Analyzes **80,000+ sales records** to uncover:

  * Best-performing iPhone models
  * High-demand regions
  * Revenue and sales trends
  * Customer purchasing patterns
  * Seasonal or yearly growth behavior
* Helps sales teams, retailers, and analysts **optimize strategies and make data-driven decisions**.

---

## 🎯 Project Objectives

* Build a **professional Power BI dashboard** for iPhone sales.
* Analyze **units sold, revenue, model trends, and regional performance**.
* Create **interactive visuals, KPIs, slicers, and trend charts**.
* Compare multiple iPhone models and their **revenue contribution**.
* Identify **growth opportunities** using historical trends.
* Present a **clean, business-focused BI report**.

---

## 📘 Dataset Overview

* **Rows:** 80,000+
* **Years Covered:** Multiple years
* **Columns:** Sales transaction details, product specs, and revenue metrics

### ⭐ Column Description

| Column Name | Description                               |
| ----------- | ----------------------------------------- |
| sales_id    | Unique ID for each sales transaction      |
| model_id    | Identifier for each iPhone model          |
| sale_date   | Date on which the sale occurred           |
| region      | Region or market where the sale happened  |
| year        | Year extracted from the sale date         |
| month       | Month extracted from the sale date (1–12) |
| units_sold  | Total number of units sold                |
| price_inr   | Selling price in INR                      |
| return_rate | Percentage of returned units              |
| storage_gb  | Storage capacity (GB)                     |
| ram_gb      | RAM configuration (GB)                    |

---

## 🧹 Data Cleaning Steps

### 1️⃣ Converted Data Types

* sales_id → Whole Number

* model_id → Whole Number

* sale_date → Date

* year → Whole Number

* month → Whole Number

* units_sold → Whole Number

* price_inr → Decimal Number

* return_rate → Decimal Number

* storage_gb → Whole Number

* ram_gb → Whole Number

### 2️⃣ Sorting & Structure

* Sorted by sales_id
  
* Removed blanks
  
* Fixed date inconsistencies
  
* Ensured year/month match sale_date

### 3️⃣ Standardization

* Removed spaces

* Fixed inconsistent regions

* Ensured numeric columns have no errors

### 4️⃣ Derived Columns

* Month Name

* Year-Month key

---

## 📌 DAX Measures Used

| Measure                   | Formula                                                   |
| ------------------------- | --------------------------------------------------------- |
| **Total Units Sold**      | `SUM('Sales'[units_sold])`                                |
| **Total Models**          | `DISTINCTCOUNT('Sales'[model_id])`                        |
| **Total Revenue (INR)**   | `SUMX('Sales', 'Sales'[units_sold] * 'Sales'[price_inr])` |
| **Transaction Count**     | `COUNTROWS('Sales')`                                      |
| **Average Selling Price** | `AVERAGE('Sales'[price_inr])`                             |


---

💡 Key Insights

Trend Analysis: Monthly sales and revenue trends reveal peak periods and seasonal patterns.

Model Performance: Certain iPhone models consistently outperform others in units sold and revenue.

Regional Insights: Some regions contribute the majority of sales, guiding targeted marketing and distribution.

Channel Analysis: High-performing sales channels help optimize retail strategies.

Customer Behavior: Insights into storage and RAM preferences, repeat purchases, and buying patterns support marketing and product planning.

Revenue Optimization: Prioritizing top models and regions improves overall revenue and resource allocation.

---

## ✅ Conclusion

The Apple iPhone Sales Analysis Dashboard transforms raw sales data into actionable insights. 
It enables stakeholders to: 
* Monitor sales trends and seasonal performance.
* Evaluate model popularity and revenue contribution.
* Optimize marketing, inventory, and sales strategies by region and channel.
* Make informed, data-driven business decisions efficiently.

Overall, the dashboard provides a **complete, interactive view of iPhone sales**, supporting strategic planning and revenue growth.

---

## 🪄 Author

**Pradeepa**

📍 Virudhunagar, Tamil Nadu

BE Graduate | Data Analytics Enthusiast

---
