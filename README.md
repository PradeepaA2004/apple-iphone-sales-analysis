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

## 💡 Dashboard Visuals Summary

| Visual Type              | X-Axis / Legend | Y-Axis / Values          |
| ------------------------ | --------------- | ------------------------ |
| **Line Chart**           | Date            | Units Sold / Revenue INR |
| **Line Chart**           | Month           | Total Units Sold         |
| **Stacked Column Chart** | Model Name      | Sum of Rating            |
| **Donut Chart**          | Channel         | Total Models             |
| **Stacked Bar Chart**    | Region          | Units Sold               |

---

## 💻 Project Files

* **Project Report:** `Apple_iPhone_Sales_Report.pdf`
* **Dashboard:** `Apple_iPhone_Sales_Dashboard.pbix`
* **Dataset:** `Cleaned dataset.csv`

---

## ✅ Conclusion

* **Trend Insights:** Monthly sales and revenue trends highlight peak periods and patterns.
* **Model Performance:** Ratings and units sold help identify top-performing iPhone models.
* **Channel & Regional Analysis:** Visualizations show which sales channels and regions drive the most revenue.
* **Informed Decision-Making:** The dashboard supports strategic decisions in marketing, inventory, and sales planning.

This dashboard **transforms raw data into actionable insights**, allowing stakeholders to monitor performance and make data-driven decisions efficiently.

---

## 🪄 Author

**Pradeepa**
📍 Virudhunagar, Tamil Nadu
BE Graduate | Data & Analytics Enthusiast.
