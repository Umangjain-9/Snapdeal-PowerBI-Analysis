# 📊 Snapdeal Product Data Analysis Dashboard (Power BI)

## 📌 Project Overview

This project presents a comprehensive data analysis of Snapdeal product listings using Power BI.  
The objective of this project was to analyze pricing, discount patterns, and customer satisfaction trends through interactive dashboards.

The project was completed as part of a Data Analytics Internship assignment and includes multiple analytical tasks focusing on business insights.

---

## 🎯 Project Objectives

The main goals of this project were:

- Analyze product-level pricing and discount data
- Identify relationships between discount and customer rating
- Perform value analysis (Price vs Customer Satisfaction)
- Study discount trends over time
- Build interactive and business-ready dashboards
- Apply data segmentation using calculated columns (DAX)

---

## 🛠 Tools & Technologies Used

- **Power BI Desktop**
- **Power BI Service (Cloud Publishing)**
- **DAX (Data Analysis Expressions)**
- Microsoft Excel (Data source format)
- GitHub (Project Hosting)

---

## 📂 Dataset Description

The dataset contains Snapdeal product-level information including:

- Product Name
- Price
- Original Price
- Discount
- Rating (detail)
- Reviews Count
- Subcategory
- Scraped Time

The dataset was cleaned and prepared inside Power BI before analysis.

---

## 📊 Dashboard Tasks Implemented

### 🔹 Task 1 – Category-Level Discount Analysis
- Analyzed discount distribution across categories
- Used bar charts and summary visuals
- Identified high-discount categories

---

### 🔹 Task 2 – Product-Level Pricing & Discount Analysis
- Created interactive product table
- Displayed:
  - Product Name
  - Price
  - Discount
  - Rating
- Added slicers:
  - Discount Band
  - Subcategory
- Enabled dynamic filtering

---

### 🔹 Task 3 – Value Analysis (Price vs Customer Satisfaction)
- Used Combo Chart (Column + Line)
- Compared:
  - Average Price
  - Average Rating
- Applied Top 15 filtering
- Added Discount Band slicer

---

### 🔹 Task 4 – Relationship Between Discount and Rating
- Used Scatter Plot
- Analyzed correlation between:
  - Discount
  - Customer Rating
- Added interactive slicers

---

### 🔹 Task 5 – Trend of Average Discount Over Time
- Used Line Chart
- Analyzed discount variation based on scraped time
- Applied time-based analysis
- Added segmentation slicer

---

### 🔹 Task 6 – KPI Summary & Business Interpretation
This task focused on generating high-level business KPIs to summarize overall product performance.

#### 📊 KPI Cards Implemented:
- Average Price  
- Average Discount %  
- Average Rating  
- Total Products  
- Total Reviews  

These KPIs provide a quick executive-level overview of pricing strategy, discount effectiveness, and customer satisfaction.

---

## 📈 Key DAX Implementation

### Discount Band Calculated Column

```DAX
Discount Band = 
SWITCH(
    TRUE(),
    snapdeal_products[Discount] <= 10, "Low (0–10%)",
    snapdeal_products[Discount] <= 30, "Medium (11–30%)",
    snapdeal_products[Discount] <= 50, "High (31–50%)",
    "Very High (>50%)"
)

---

###Average Discount:
Average Discount = AVERAGE(snapdeal_products[Discount])

---

###Average Rating:
Average Rating = AVERAGE(snapdeal_products[Rating (detail)])

---

###Total Products:
Total Products = COUNT(snapdeal_products[Product Name])

---

###Total Reviews:
Total Reviews = SUM(snapdeal_products[Reviews Count])

---

###🔍 Key Insights Derived

-Higher discounts do not always guarantee higher customer ratings.
-Premium-priced products do not consistently have better satisfaction scores.
-Discount patterns fluctuate over time.
-Customer perception is influenced by multiple factors beyond pricing.
-Subcategory-level segmentation reveals varied discount strategies.

---

###🌐 Live Dashboard Access
Power BI Dashboard Link:
https://drive.google.com/drive/folders/1bsiYi75idMA4BJGBT9SRwB1Dawoxhzx0?usp=sharing
**PBIX file shared for download due to publishing restriction
