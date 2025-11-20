# 📊 Apple iPhone Sales Analysis Dashboard

### Power BI | Data Analytics | Sales Insights | iPhone Market Trends

This project analyzes **Apple iPhone sales data** to uncover trends related to revenue, model performance, regional demand, year-wise growth, and customer purchasing patterns.
The dashboard provides meaningful KPIs and visual insights useful for **sales teams, marketing analysts, retail strategy teams, and data-driven decision-making**.

---

## 📁 Project Files in This Repository

| File                                     | Description                                                 |
| ---------------------------------------- | ----------------------------------------------------------- |
| **📂 iphone_india_full.csv**             | Dataset used for cleaning, modeling, and dashboard creation |
| **📊 Apple_iPhone_Sales_Dashboard.pbix** | Full Power BI dashboard                                     |
| **📑 Apple_iPhone_Sales_Report.pdf**     | PDF report explaining insights                              |
| **📝 README.md**                         | Project documentation                                       |

---

## 📘 Project Overview

The goal of this project is to analyze the sales performance of iPhone models across regions and years, identify revenue trends, and highlight growth opportunities.
The dashboard combines KPIs, charts, and slicers to offer dynamic insights.
The cleaned dataset (iphone_ambia_full.csv processed) and the Power BI dashboard together demonstrate a complete workflow—from data preparation → modeling → visualization—suitable for analytics portfolios, corporate reporting, and GitHub showcase projects

## 🎯 Key Objectives

* Analyze yearly and monthly iPhone sales trends
* Compare performance of different iPhone models
* Identify high-performing regions and sales channels
* Calculate revenue KPIs and growth metrics
* Provide a business-ready dashboard for decision-making

---
## 📘 **Dataset Overview**

The project uses the cleaned iPhone sales dataset containing more than **80,000 rows** of sales records across different iPhone models, regions, and years.

## 📄 **Files**

* **Raw file:** iphone_india_full.csv

## 📑 **Column Description**

| Column Name | Description                                  |
| ----------- | -------------------------------------------- |
| sales_id    | Unique ID for each sales transaction         |
| model_id    | Identifier for each iPhone model             |
| sale_date   | Date on which the sale occurred              |
| region      | Region or market where the sale happened     |
| year        | Year extracted from the sale date            |
| month       | Month extracted from the sale date (1–12)    |
| units_sold  | Total number of units sold                   |
| price_inr   | Selling price of the iPhone in Indian Rupees |
| return_rate | Percentage of returned or defective units    |
| storage_gb  | Storage capacity (GB) of the device          |
| ram_gb      | RAM configuration (GB)                       |

---

# 🧹 **Data Cleaning Steps**

The dataset was cleaned and prepared in Excel before importing into Power BI.
Below are the steps followed:

### **1. Converted Data Types**

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

### **2. Sorted and Structured Data**

* Sorted sales_id in ascending order
* Removed blank rows and duplicate records
* Fixed date format inconsistencies
* Ensured month and year fields match sale_date

### **3. Standardized Columns**

* Removed unnecessary spaces
* Corrected inconsistent text values (region, model names)
* Ensured numerical columns had no text errors

### **4. Added Derived Columns**

* Month Name (Excel):

  ```
  =TEXT(G2, "mmm")
  ```
* Year-Month (for time series):

  ```
  =TEXT(G2, "YYYY-MM")
  ```

---

# 🧮 **DAX Measures Used in Power BI**

# ✅ **1. Total Units Sold**

Counts all units sold from the *units_sold* column.

```DAX
Total Units Sold =
SUM('Sales'[units_sold])
```

---

# ✅ **2. Total Models**

Counts how many **unique iPhone models** exist.

```DAX
Total Models =
DISTINCTCOUNT('Sales'[model_id])
```

---

# ✅ **3. Total Revenue (INR)**

Revenue = units sold × price

You can use either:

### ✔ **Method A: Direct SUMX (Best Practice)**

```DAX
Total Revenue INR =
SUMX(
    'Sales',
    'Sales'[units_sold] * 'Sales'[price_inr]
)
```

### ✔ **Method B: If revenue column already exists**

(Use only if revenue is pre-calculated in Excel)

```DAX
Total Revenue INR =
SUM('Sales'[revenue_inr])
```

---

# ✅ **4. Total Sales Transactions**

Each `sales_id` = 1 transaction.

```DAX
Total Transactions =
COUNT('Sales'[sales_id])```

---
## 🔧 Tools & Technologies

* **Power BI (Core Dashboard Development)**
* **Excel / CSV (Data Source)**
* **DAX Measures**
* **Power Query (Data Cleaning)**
* **GitHub (Version Control & Documentation)**

---

## 📈 Key KPIs Displayed

* **Total Units Sold**
* **Total Revenue**
* **Average Selling Price (ASP)**
* **Year-over-Year Growth**
* **Top Selling iPhone Model**
* **Best Performing Region**

---

## 📊 Dashboard Features

### 1️⃣ **Sales Trend Analysis**

* Year-wise and month-wise sales performance
* Peak seasons and demand drops

### 2️⃣ **Model-wise Comparison**

* iPhone models ranked by units sold
* High-revenue models vs budget models

### 3️⃣ **Region-wise Insights**

* Sales performance across India zones
* Heatmaps for regional demand

### 4️⃣ **Customer & Price Insights**

* Price band analysis
* Revenue contribution by model category

### 5️⃣ **Interactive Filters**

* Year
* Region
* Model
* Sales channel

---

## 📂 Data Model Overview

**Fact Table:**
`Sales_Fact` → contains sales qty, revenue, year, model, region

**Dimension Tables:**

* `Dim_Model` (iPhone model details)
* `Dim_Region` (zone, state)
* `Dim_Date` (calendar table)

Relationships:

* Star schema optimized for performance
* One-to-many relationships

---

## 📜 DAX Measures Used

```DAX
Total Units Sold = SUM(Sales_Fact[Units])
Total Revenue = SUM(Sales_Fact[Revenue])
Avg Selling Price = [Total Revenue] / [Total Units Sold]

YoY Growth = 
VAR CurrentYear = [Total Revenue]
VAR PreviousYear = CALCULATE([Total Revenue], DATEADD(Dim_Date[Date], -1, YEAR))
RETURN DIVIDE(CurrentYear - PreviousYear, PreviousYear)
```

More measures included in the PBIX file.

---

## 📢 Insights Summary (From Dashboard)

* iPhone **Pro models contribute the highest revenue**
* Some regions show strong growth, indicating **market expansion** opportunities
* Older models still contribute significant sales due to price sensitivity
* Sales spike during festivals and new product launch windows

---

## 🖼️ Dashboard Preview (Screenshot)

*(Add your dashboard image here when uploading)*

---

## 🚀 How to Use This Project

1. Clone or download this repository
2. Open `Apple_iPhone_Sales_Dashboard.pbix` in **Power BI Desktop**
3. Load data from `iphone_india_full.csv`
4. Explore visual insights using filters and charts

---

## 🤝 Contributions

Contributions are welcome!
You may improve the dataset, create advanced DAX measures, or enhance visualization.

---
📌 Conclusion

The Apple iPhone Sales Analysis Dashboard provides a clear, data-driven view of iPhone sales performance across India. By cleaning and transforming the raw dataset (iphone_india_full.csv), the project ensures accurate and reliable insights for sales, pricing trends, product performance, storage/variant preferences, and overall revenue analytics.

The Excel cleaning process standardized data types, corrected dates, generated month names, and removed inconsistencies, resulting in a fully structured dataset ready for Power BI. With this cleaned dataset, the dashboard delivers:

📊 Accurate time-series sales trends

🔍 Model-wise and variant-wise performance insights

💰 Price and revenue distribution patterns

📈 Units sold vs. return rate correlations

🧩 Filters for dynamic and interactive exploration

This project highlights how raw transactional data can be transformed into actionable business intelligence, supporting decision-making for pricing strategy, inventory planning, and product demand forecasting.


---


🪄 Author

Pradeepa

📍 Viruthunagar, Tamil Nadu

💼 BE Graduate | Data & Analytics Enthusiast




