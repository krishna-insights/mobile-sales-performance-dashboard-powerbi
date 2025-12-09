# 📱 Mobile Sales Performance Dashboard (Power BI)

A complete end-to-end **Mobile Sales Performance Dashboard** built using Power BI, Power Query, Data Modeling, and DAX.
This project delivers actionable insights into revenue trends, product performance, and regional sales contributions, enabling data-driven business decisions.

---

## 🎯 Problem Statement

Mobile sales data is often scattered across multiple files, manually processed, and lacks automated reporting. This leads to:

* ❗ **Inconsistent KPIs**
* ❗ **Delayed monthly reporting**
* ❗ **No real-time visibility** into product or brand performance

This project solves these challenges by creating a **fully automated and interactive Power BI dashboard** that tracks:
* Total Revenue, Profit, and Quantity Sold
* Top/Bottom Performing Models
* Month-to-Date & Previous Month Trends
* Regional Sales Insights

---

## 🛠️ Step-by-Step Procedure

### 1. Business Requirement Understanding
* Identified key KPIs relevant to business users: revenue, profit, quantity, top models, and monthly comparison.
* Understood reporting needs such as category-wise and region-wise breakdowns.

### 2. Data Review & Understanding
* Explored raw sales dataset including: Model, Brand, Quantity, Unit Price, Profit, Region, Category, Date.

### 3. Data Import Using Power Query 📥
* Loaded source data into Power BI.
* Ensured smooth refresh and correct data types.

### 4. Data Cleaning & Quality Check 
* Removed duplicate rows.
* Standardized date formats, corrected data inconsistencies.
* Ensured the dataset was analytics-ready.

### 5. Creating a Custom Calendar Table (Power Query) 📅
A continuous date table was essential for time-intelligence calculations.

* **Custom Calendar Code (Power Query M):**
    > ```m
    > = List.Dates(#date(2021,1,1), 1461, #duration(1,0,0,0))
    > ```
* Converted the list to a table and added Month, Year, Quarter, etc.

### 6. Data Modeling (Power BI) ⭐
* Established a **One-to-Many** relationship between Calendar Table and Sales Table.
* Ensured proper filter context flow for time-based KPIs.

### 7. DAX Measures (Core Calculations) ➕
* **Total Revenue** = `SUM('Sales Data'[Revenue])`
* **Total Profit** = `SUM('Sales Data'[Profit])`
* **Total Quantity** = `SUM('Sales Data'[Quantity])`
* **MTD Revenue** = `TOTALMTD([Total Revenue], 'Calendar'[Date])`
* **Previous Month Revenue** = `CALCULATE([Total Revenue], PREVIOUSMONTH('Calendar'[Date]))`
* **Top N Models (Dynamic)** = `RANKX(ALL('Sales Data'[Model]), [Total Revenue], , DESC)`

### 8. Dashboard Layout & Structure 🖼️
* Designed structured sections for KPIs, charts, and slicers.
* Used consistent formatting for a clean, professional look.

### 9. Chart Development & Formatting 🎨
* **Created interactive visuals including:**
  * Revenue & Profit Trend (Line Chart)
  * Top N Models (Bar Chart)
  * Brand Performance (Clustered Bar)
  * Category Contribution (Donut Chart)
  * Region-wise Sales (Map/Bubble Chart)
  * Monthly Comparison using MTD & Previous Month
* **Applied formatting for better readability:** Rounded corners, Custom color palette, Proper labeling & tooltips.

### 10. Final Dashboard Build ✅
* Added all slicers (Brand, Model, Month, Category, Region).
* Configured Edit Interactions for accurate filtering.
* Ensured full automation with refresh-ready data.

---

## 🔍 Key Insights

* **Brand Performance:** Mid-range brands dominated revenue, while flagship models contributed higher profits despite lower volume.
* **Top Models:** Few models contributed a major share of total revenue, indicating strong product concentration.
* **Monthly Trend:** Sales showed noticeable peaks during promotional periods, with clear fluctuations across months.
* **Profitability:** High-selling models were not always the most profitable, revealing margin-driven insights.
* **Regional Demand:** Certain regions consistently outperformed in revenue and quantity sold.
* **Category Behavior:** Budget phones led in volume, whereas mid-range and flagship phones led in profit.

---

## 📊 Results & Conclusion

The Mobile Sales Dashboard successfully transformed raw sales data into a comprehensive analytical report. With automated KPIs, dynamic filtering, and time-intelligence measures, the dashboard enabled:

* Real-time monitoring of revenue, profit, and quantity trends
* Identification of best- and worst-performing models
* Clear visibility into brand and region-level performance
* Accurate month-over-month insights with MTD and previous month comparison
* Faster business decisions based on reliable, refreshed data

This solution provides a strong analytical foundation for strategic planning, inventory optimization, and improved sales performance.

---

## 🔒 Project File Information

To maintain confidentiality and protect the work involved, the complete editable Power BI (.pbix) file is **not publicly uploaded**.
It can be shared upon request for professional or academic review.

---

## 👤 Contact

**Krishna Jaiswal**
* 📧 Email: **krishna250763@gmail.com**
* 🔗 LinkedIn: [www.linkedin.com/in/krishnaa07](https://www.linkedin.com/in/krishnaa07)
* Data Visualization & Formatting

---

## 🔒 Project File Information

To ensure data confidentiality and protect the analytical work of this project, the full editable Power BI (.pbix) file is **not uploaded publicly**.
It can be shared privately upon request for academic or professional evaluation.

---

## 👤 Contact

**Krishna Jaiswal**
* 📧 Email: **krishna250763@gmail.com**
* 🔗 LinkedIn: [www.linkedin.com/in/krishnaa07](https://www.linkedin.com/in/krishnaa07)
