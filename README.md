here# 📱 Mobile Sales Dashboard (Power BI)

A complete end-to-end **Mobile Sales Dashboard** built using Power BI.
This project provides actionable insights into sales performance, revenue trends, profit margins, and product-wise performance—helping businesses make faster, data-driven decisions.

---

## 🔴 Problem Statement

Mobile retail businesses often struggle with:
* Fragmented sales data
* Manual reporting efforts
* Difficulty identifying high-performing products
* Limited visibility into monthly sales performance

The objective of this project is to build an automated Power BI dashboard that enables stakeholders to monitor **sales volume**, **revenue**, **profitability**, **top/bottom products**, and **month-over-month performance** efficiently.

---

## 📝 Step-by-Step Procedure

### 1. Business Requirement Gathering
* Identified important KPIs required by sales and management teams.
* Understood reporting needs to track product-level and monthly performance.

### 2. Understanding the Dataset
* Reviewed mobile sales data including:
  * Product name
  * Brand
  * Selling price
  * Cost price
  * Profit
  * Quantity sold
  * Invoice date
  * Region/store

### 3. Data Import & Cleaning (Power Query) 🧼
* Imported source data into Power BI using Power Query.
* Performed:
  * Null value handling
  * Wrong data correction
  * Standardization of product and category fields
  * Ensuring numeric fields were correctly typed

### 4. Creating a Single Date Column
* Date components were merged where required:
    > `Add Column → Merge Columns (Separator: "-") → Convert to Date`
* Ensured compatibility with the Calendar table.

### 5. Creating Calendar Table (Power Query) 📅
* A dynamic date table was created using `List.Dates`:
    > `List.Dates(#date(2021,1,1), 1461, #duration(1,0,0,0))`
* Added required fields: Year, Month, Month Name, Quarter, Month-Year.

### 6. Data Modeling (Power BI) ⭐
* Designed a **star schema**:
  * Fact Table → Sales
  * Dimension Table → Calendar
* Created one-to-many relationship using Date.
* Ensured optimized and efficient model for DAX calculations.

### 7. DAX Calculations (Custom Measures) ➕
* **Total Revenue** = `SUM('Sales'[Selling Price])`
* **Total Cost** = `SUM('Sales'[Cost Price])`
* **Total Profit** = `SUM('Sales'[Profit])`
* **Total Quantity** = `SUM('Sales'[Quantity])`
* **Revenue MTD** = `CALCULATE([Total Revenue], DATESMTD('Calendar'[Date]))`
* **Revenue Last Month** = `CALCULATE([Total Revenue], PREVIOUSMONTH('Calendar'[Date]))`
* **MoM Revenue Change** = `[Revenue MTD] - [Revenue Last Month]`
* **Average Profit per Unit** = `DIVIDE([Total Profit], [Total Quantity])`

### 8. Dashboard Structure & Visual Layout 🖼️
* Built visual sections for:
  * KPIs (Revenue, Profit, Quantity)
  * MoM comparison
  * Top & bottom-selling mobiles
  * Brand-wise performance
  * Category segmentation
  * Regional sales breakdown

### 9. Chart Development & Formatting
* Developed visuals including:
  * Revenue trend line & Profit trend
  * Top 5 products bar chart
  * Brand-wise performance
  * Monthly revenue comparison
  * Donut chart for category contribution
* Applied consistent theme and standardized formatting for readability.

### 10. Final Dashboard Development
* Combined all visuals into a clean, business-ready layout.
* Added slicers for Month, Brand, and Category.
* Ensured dynamic updates with Calendar-based time intelligence.

---

## 🛠 Tools & Techniques Used

* Power BI Desktop
* Power Query (Data Transformation)
* DAX (Custom Calculations)
* Star Schema Data Modeling
* Time-Intelligence Functions
* Data Visualization & Formatting

---

## 📦 Deliverables

* 📊 **Power BI Dashboard (PBIX)** — *Available on request*
* 🖼 **Dashboard Screenshot** — *Attach link*
* 📄 **Project Summary PDF** — *Attach link*
* 📝 **README.md** — This documentation

---

## 🔒 Project File Information

To ensure data confidentiality and protect the analytical work of this project, the full editable Power BI (.pbix) file is **not uploaded publicly**.
It can be shared privately upon request for academic or professional evaluation.

---

## 👤 Contact

**Krishna Jaiswal**
* 📧 Email: **krishna250763@gmail.com**
* 🔗 LinkedIn: [www.linkedin.com/in/krishnaa07](https://www.linkedin.com/in/krishnaa07)
