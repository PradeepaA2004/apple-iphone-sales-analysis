# <img width="45" height="45" alt="image" src="https://github.com/user-attachments/assets/833ad067-5063-42fc-87a4-88215daaceb7" /> Apple iPhone Sales Analysis Dashboard

**Power BI | Data Analytics | Sales Insights | iPhone Market Trends**

This project analyzes Apple iPhone sales data to uncover trends related to revenue, model performance, regional demand, year-wise growth, and customer purchasing patterns. The dashboard provides meaningful KPIs and visual insights useful for sales teams, marketing analysts, retail strategy teams, and data-driven decision-making.

---

📱**Project Overview**

The Apple iPhone Sales Analysis Dashboard provides a detailed view of sales performance across models, regions, years, and revenue segments.
Using a structured dataset of 80000+ iPhone sales records, this project uncovers:

Best-performing iPhone models

High-demand regions

Revenue and sales trends

Customer purchasing patterns

Seasonal or yearly growth behavior

This dashboard helps sales teams, retailers, and marketing analysts make data-driven decisions and optimize product strategies.

---

🎯 👍 **Project Objectives**

Build a professional Power BI dashboard for Apple iPhone sales

Analyze units sold, revenue, model trends, and region-wise performance

Create interactive visuals, KPIs, slicers, and trend charts

Compare multiple iPhone models and their contribution to revenue

Identify growth opportunities using historical trends

Present a clean, business-focused BI report

---


 📘 Dataset Overview
 -

The cleaned dataset contains **80,000+ rows** of iPhone sales records across multiple years.

📄 Files

**Raw file:** Data

**cleaned file:** iphone_india_full.csv
**Dashboard Sceenshot;**![]("C:\Users\PRADEEPA\Downloads\dashboard.png")

---

 ##⭐ Column Description
 -

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


✅ **📌 DAX Measures Used in Power BI**
--

1️⃣ Total Units Sold
Total Units Sold =
SUM ( 'Sales'[units_sold] )

2️⃣ Total Models
Total Models =
DISTINCTCOUNT ( 'Sales'[model_id] )

3️⃣ Total Revenue (INR)
Total Revenue INR =
SUMX (
    'Sales',
    'Sales'[units_sold] * 'Sales'[price_inr]
)

4️⃣ Transaction Count
Transaction Count =
COUNTROWS ( 'Sales' )

5️⃣ Average Selling Price
Average Price =
AVERAGE ( 'Sales'[price_inr] )

---

💡 💻 Dashboard Visuals Summary:
 -

| Visual Type              | X-Axis / Legend   | Y-Axis / Values          |
| ------------------------ | ----------------- | ------------------------ | 
| **Line Chart**           | Date              | Units Sold / Revenue INR | 
| **Line Chart**           | Month             | Total Units Sold         | 
| **Stacked Column Chart** | Model Name        | Sum of Rating            |
| **Donut Chart**          | Channel           | Total Models             |  
| **Stacked Bar Chart**    | Region            | Units Sold               | 

---

📁 **Project Files**
--

**Project Report:** Apple_iPhone_Sales_Report.pdf

**Dashboard:** Apple_iPhone_Sales_Dashboard.pbix

**Dataset:** data.csv 

---

✅**Conclusion**

The Apple iPhone Sales Analysis Dashboard provides a complete view of global iPhone sales, allowing for in-depth analysis across models, regions, channels, and time periods. Key takeaways include:

Trend Insights: Monthly sales and revenue trends highlight peak periods and patterns.

Model Performance: Ratings and units sold help identify top-performing iPhone models.

Channel & Regional Analysis: Visualizations show which sales channels and regions drive the most revenue.

Informed Decision-Making: The dashboard supports strategic decisions in marketing, inventory, and sales planning.

Overall, this dashboard turns raw data into actionable insights, enabling stakeholders to monitor performance and make data-driven business decisions efficiently.

---


## 🪄 Author

**Pradeepa**
📍 Virudhunagar, Tamil Nadu

 BE Graduate | Data & Analytics Enthusiast.

---
