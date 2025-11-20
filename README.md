# apple-iphone-sales-analysis
Interactive Power BI dashboard analyzing global Apple iPhone sales by model, region, and year. Includes insights on revenue, units sold, market share, and top-performing iPhone models using DAX, data modeling, and dynamic visualizations.
Here is a **highly professional, industry-standard README.md** ready for GitHub.
Clean formatting • Business style • Analyst-friendly • Looks like a real corporate project.

---

# 📊 Apple iPhone Sales Analysis Dashboard

### **Enterprise Data Analytics Project | Power BI | Revenue Insights | Market Intelligence**

This repository contains a complete **Apple iPhone Sales Analysis** project built for data-driven decision-making.
The project includes a structured dataset, a fully interactive Power BI dashboard, and a detailed insights report suitable for **business analysis, portfolio presentation, and enterprise reporting**.

---

## 📁 **Repository Contents**

| File                                  | Description                                        |
| ------------------------------------- | -------------------------------------------------- |
| **iphone_india_full.csv**             | Clean dataset used for modelling and visualization |
| **Apple_iPhone_Sales_Dashboard.pbix** | Complete Power BI dashboard file                   |
| **Apple_iPhone_Sales_Report.pdf**     | Executive summary of insights and recommendations  |
| **README.md**                         | Project documentation (you are here)               |

---

## 📘 **Project Overview**

The objective of this project is to analyze the **sales performance of Apple iPhones across regions, models, and years**.
The dashboard provides **actionable insights** into revenue trends, product performance, market behavior, and growth opportunities.

This project demonstrates real-world data analytics skills including **data cleaning, modeling, DAX calculations, KPI building, and business interpretation**.

---

## 🎯 **Project Objectives**

* Evaluate **yearly and monthly sales performance**
* Identify **top-selling iPhone models**
* Compare **regional demand and revenue**
* Calculate **key KPIs for business decision-makers**
* Create a **professional Power BI dashboard** for strategic insights

---

## 🔧 **Tools & Technologies**

* **Power BI Desktop** – Data modeling & visualization
* **Power Query** – Data cleaning & transformation
* **DAX** – KPI measurements & calculations
* **Excel / CSV** – Data source preparation
* **GitHub** – Version control & documentation

---

## 📊 **Key Performance Indicators (KPIs)**

* Total Revenue
* Total Units Sold
* Average Selling Price (ASP)
* YoY Revenue Growth %
* Best Performing Region
* Top Selling iPhone Model

---

## 📉 **Dashboard Modules**

### **1️⃣ Sales Performance Analysis**

* Year-on-year and month-on-month trends
* Seasonal patterns and launch-period spikes

### **2️⃣ Model-Level Performance**

* Revenue by iPhone model
* Unit sales comparison
* Premium vs non-premium model contribution

### **3️⃣ Geographic Insights**

* Region-wise revenue comparison
* Zone performance ranking

### **4️⃣ Customer & Price Insights**

* ASP distribution
* Product mix analysis

### **5️⃣ Interactive Filters**

* Region
* Model
* Year
* Sales channel

---

## 🗂️ **Data Model Design**

A clean **star schema** is used:

### **Fact Table**

* `Sales_Fact` → units sold, revenue, year, region, model

### **Dimension Tables**

* `Dim_Model`
* `Dim_Region`
* `Dim_Date`

**Why star schema?**

* Faster performance
* Cleaner relationships
* Easy to scale and maintain

---

## 🧮 **Sample DAX Measures**

```DAX
Total Units Sold = SUM(Sales_Fact[Units])

Total Revenue = SUM(Sales_Fact[Revenue])

Average Selling Price = 
DIVIDE([Total Revenue], [Total Units Sold])

Year over Year Growth % =
VAR CurrentYear = [Total Revenue]
VAR PreviousYear =
    CALCULATE([Total Revenue], DATEADD(Dim_Date[Date], -1, YEAR))
RETURN
    DIVIDE(CurrentYear - PreviousYear, PreviousYear)
```

---

## 📝 **Insights Summary**

* iPhone **Pro** and **Pro Max** models generate the highest revenue
* Strong sales growth in certain regions indicates **market expansion potential**
* Older generation iPhones still contribute significantly due to price-sensitive buyers
* Seasonal peaks during **festivals**, **sales events**, and **new product launches**

These insights can support **marketing strategy**, **inventory planning**, and **regional allocation** decisions.

---

## 🖥️ **How to Use This Project**

1. Download or clone the repository
2. Open the `.pbix` file in **Power BI Desktop**
3. Ensure the dataset path points to `iphone_india_full.csv`
4. Refresh data
5. Explore interactive visuals and KPIs

---

## 🤝 **Contributions**

Contributions, improvements, and enhancements are welcome.
You may add:

* Additional KPI metrics
* Advanced DAX calculations
* New visualization pages
* Extended datasets

---

## 📬 **Contact**

For any questions or collaboration opportunities:
**Pradeepa | Data Analytics Portfolio Project**

---

If you want a **more advanced enterprise-style README**, or want me to **add badges, project structure, installation instructions, or screenshots**, tell me **“Make it enterprise level”**.

