# 📊 Superstore Sales & Profit Analysis (Power BI)

## 📌 Overview

This project presents a comprehensive **Sales and Profit Analysis Dashboard** built using Power BI.
The goal is to analyze business performance across **time, sub-categories, countries, and customer segments**, and derive actionable insights using data visualization and DAX.

---

## 🎯 Objectives

* Analyze **sales and profit trends over time**
* Identify **high-performing and loss-making sub-categories**
* Evaluate **country-wise profitability**
* Understand **profit margins and growth patterns**
* Use **DAX for advanced calculations (YoY Growth, Profit Margin, Time Intelligence)**

---

## 📂 Dataset

* Source: Superstore dataset (CSV)
* Contains:

  * Orders data
  * Sales, Profit, Quantity
  * Category & Sub-category
  * Country/Region
  * Order Date, Segment

---

## 🧠 Key DAX Measures Used

### 📈 YoY Profit Growth

Measures year-over-year change in profit:

```
YoY Profit Growth = 
DIVIDE(
    [Total Profit] - CALCULATE([Total Profit], SAMEPERIODLASTYEAR('Date'[Date])),
    CALCULATE([Total Profit], SAMEPERIODLASTYEAR('Date'[Date]))
)
```

### 📊 Profit Margin %

Shows efficiency of profit generation:

```
Profit Margin % = 
DIVIDE([Total Profit], [Total Sales], 0)
```

### 📅 YTD Calculations

Used for cumulative trend analysis:

```
YTD Profit = TOTALYTD([Total Profit], 'Date'[Date])
```

---

## 📊 Dashboard Pages & Insights

---

### 📌 1. Sub-Category Analysis

* Displays **profit distribution across sub-categories**
* Highlights top contributors like *Copiers and Phones*
* Identifies low-performing categories

🔍 **Insight:**

* Some sub-categories generate strong sales but relatively lower profit → indicates margin inefficiencies

---

### 🌍 2. Country Analysis

* Compares **sales and profit across countries**
* Shows variation in performance geographically

🔍 **Insight:**

* A few countries dominate total sales contribution
* Some regions show **negative or low average profit**, indicating operational inefficiencies

---

### 📊 3. Profit Analysis (Core Page)

#### 🔹 KPI Metrics:

* Total Sales
* Total Profit
* YoY Profit Growth
* Profit Margin %

#### 🔹 Key Visuals:

* **Bar + Line Combo Chart**

  * Median Profit vs Sales by Sub-category
* **Profit Margin by Country**
* **Segment-wise Profit Distribution (Donut Chart)**

🔍 **Insights:**

* High sales do not always translate to high profit
* Certain sub-categories show **declining profitability**
* Profit margins vary significantly across countries

---

### 📈 4. Sales Trend Analysis

* Monthly trend of sales across years and segments
* Helps identify seasonality and growth patterns

🔍 **Insight:**

* Sales show **consistent growth with seasonal spikes**
* Consumer segment contributes the most to revenue

---

## 📸 Screenshots

(Add your dashboard screenshots here)

---

## 🛠 Tools & Technologies

* Power BI
* DAX (Data Analysis Expressions)
* Excel / CSV Dataset

---

## 🚀 Key Business Insights

* 📌 High sales ≠ high profit → discounting impacts margins
* 📌 Certain sub-categories consistently underperform
* 📌 Profit growth shows variability across time
* 📌 Geographic disparities exist in profitability
* 📌 Consumer segment drives majority of sales

---

## 📎 How to Use

1. Open `.pbix` file in Power BI Desktop
2. Interact using slicers (Date, Category, Country)
3. Explore insights across different pages

---

## 💡 Future Improvements

* Add **Top N filtering for better focus**
* Include **forecasting models**
* Enhance interactivity with drill-through pages
* Add **customer segmentation analysis**

---

## 👤 Author

Mihir Aryaman

---
