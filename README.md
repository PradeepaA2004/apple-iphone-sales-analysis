# 📊 Apple iPhone Sales Analysis Dashboard

**Power BI | Data Analytics | Sales Insights | iPhone Market Trends**

This project analyzes Apple iPhone sales data to uncover trends related to revenue, model performance, regional demand, year-wise growth, and customer purchasing patterns. The dashboard provides meaningful KPIs and visual insights useful for sales teams, marketing analysts, retail strategy teams, and data-driven decision-making.

---

## 📁 Project Files in This Repository

| File                                     | Description                                                 |
| ---------------------------------------- | ----------------------------------------------------------- |
| 📂 **iphone_india_full.csv**             | Dataset used for cleaning, modeling, and dashboard creation |
| 📊 **Apple_iPhone_Sales_Dashboard.pbix** | Full Power BI dashboard                                     |
| 📑 **Apple_iPhone_Sales_Report.pdf**     | PDF report explaining insights                              |
| 📝 **README.md**                         | Project documentation                                       |

---

## 📘 Project Overview

The goal of this project is to analyze the sales performance of iPhone models across regions and years, identify revenue trends, and highlight growth opportunities.

---

## 🎯 Key Objectives

* Analyze yearly and monthly iPhone sales trends
* Compare performance of different iPhone models
* Identify high-performing regions and sales channels
* Calculate revenue KPIs and growth metrics
* Provide a business-ready dashboard for decision-making

---

## 📘 Dataset Overview

The cleaned dataset contains **80,000+ rows** of iPhone sales records across multiple years.

### 📄 Files

**Raw file:** iphone_india_full.csv

---

## 📑 Column Description

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

## ✅ 📌 DAX Measures Used in Power BI

1. Total Units Sold
Total Units Sold = SUM('Sales'[units_sold])

2. Total models
Total Models = DISTINCTCOUNT('Sales'[model_id])

3.Total revenue (INR)
Total Revenue INR =
SUMX(
    iphone_india_full,iphone_india_full[units_sold] * iphone_india_full[price_inr])

4.Transaction Count
Transaction Count =COUNTROWS( iphone_india_full )

5. Average Selling Price
Average Price = AVERAGE('Sales'[price_inr])

## 📊 Dashboard Features

### 1️⃣ Sales Trend Analysis

### 2️⃣ Model-wise Comparison

### 3️⃣ Region-wise Insights

### 4️⃣ Customer & Pricing Insights

### 5️⃣ Interactive Filters

---

## 📢 Insights Summary

* Pro models contribute the highest revenue
* Strong regional growth detected
* Older models still have strong demand
* Sales spike during festivals and product launches

---

## 🚀 How to Use This Project

1. Clone repo
2. Open PBIX
3. Load CSV
4. Explore dashboard

---

## 🪄 Author

**Pradeepa**
📍 Virudhunagar, Tamil Nadu
BE Graduate | Data & Analytics Enthusiast

---
