# 📊 Business Analytics Project — E-Commerce User Behavior Analysis

Welcome to my **Business Analytics Project**, where I analyzed e-commerce user activity logs to uncover insights into **conversion performance**, **customer retention**, and **purchase behavior**.  
All analyses and calculations were **answered and documented in the Excel file: “Business Analytics Project.xlsx.”**

---

## 🧠 Project Overview

As a newly hired **Junior Data Analyst** at a fictional e-commerce company, my goal was to transform raw event logs into actionable business metrics.  
Using spreadsheet analytics, I built a **conversion funnel**, performed **cohort analysis**, and calculated **retention rates** to help the executive team understand customer engagement and loyalty.

The dataset, provided in the `"raw_user_activity"` sheet, contains the following columns:

| Column | Description |
|---------|--------------|
| `user_id` | Unique customer IDs |
| `event_type` | The type of activity (page view, add to cart, purchase) |
| `category_code` | Product category viewed or purchased |
| `brand` | Brand name |
| `price` | Product price (USD) |
| `event_date` | Date of the activity (YYYY-MM-DD) |

---

## 🧾 Dataset Source
- File Name: **Business Analytics Project.xlsx**  
- Sheet: **raw_user_activity**  
- Tools Used: **Microsoft Excel / Google Sheets**
---

## 🗂️ Files Included

| File | Description |
|------|--------------|
| `Business Analytics Project.xlsx` | Project report template used for final submission |
| `README.md` | This file |
---

## 🧩 Project Tasks and Deliverables
All the following tasks were **completed and documented in the Excel file** “Business Analytics Project.xlsx.”

### **Part 1: Build a Conversion Funnel**
**Goal:** Understand how effectively product page views convert into purchases.  
**Steps Completed:**
- Created a new sheet: `conversion_funnel`
- Built a **pivot table** counting **unique users** at each stage of the funnel (view → cart → purchase)
- Added **total conversion rate** and **step-to-step conversion rate** formulas  
**Answered in:** `conversion_funnel` sheet  

---

### **Part 2: Prepare Data for Cohort Analysis**
**Goal:** Group users into acquisition cohorts based on the month of their first purchase.  
**Steps Completed:**
- Created a new sheet: `purchase_activity`
- Filtered only purchase events from the raw data
- Created a `first_purchase` pivot table to find each user’s earliest purchase date
- Used `VLOOKUP()` to map first purchase dates into the main purchase dataset
- Created columns for:
  - `event_month` — extracted using `TEXT()` function  
  - `first_purchase_month` — formatted as YYYY-MM  
  - `cohort_age` — calculated using `DATEDIF()` (months between first and current purchase)  
**Answered in:** `purchase_activity` and `first_purchase` sheets  

---

### **Part 3: Calculate Retention Rates**
**Goal:** Measure how well the company retains customers over time by cohort.  
**Steps Completed:**
- Built a pivot table: `cohort_analysis`  
  - Rows: first purchase month (cohort)  
  - Columns: cohort age (months since first purchase)  
  - Values: unique users per cohort age  
- Created a `retention_rates` sheet to calculate month-over-month retention percentages using fixed references.  
**Answered in:** `cohort_analysis` and `retention_rates` sheets  

---

### **Part 4: Organize and Document the Spreadsheet**
**Goal:** Deliver a polished, executive-ready analysis file.  
**Steps Completed:**
- Wrote an **executive summary** describing key insights:
  - Conversion funnel results  
  - Retention analysis highlights  
- Added a **data description** and **methodology notes** (cohort definitions, formulas, assumptions)  
- Organized all sheets in logical order:
  1. `Table of Contents`
  2. `Executive Summary`
  3. Analytical results (conversion, retention)
  4. Supporting calculations
  5. Raw data sheets  
- Applied professional formatting: frozen headers, bold titles, consistent date formats, and cell borders.  
**Answered in:** `Executive Summary` and `Table of Contents` sheets  

---

## 📈 Key Business Insights
*(Summarized from the Excel analysis)*

- The **conversion funnel** revealed clear drop-off stages between browsing and checkout.  
- **Cohort analysis** showed consistent retention for new users over several months.  
- The **retention rates** helped identify which acquisition months produced the most loyal customers.  

---

## ⚙️ Tools & Skills Used
- **Microsoft Excel / Google Sheets**
- **Pivot Tables**
- **VLOOKUP(), TEXT(), DATEDIF()**
- **Conditional Formatting**
- **Data Cleaning & Filtering**
- **Cohort Analysis**
- **Conversion Funnel Metrics**

---

### 🏁 Summary

This project demonstrates the use of **advanced spreadsheet techniques** to analyze customer behavior, calculate retention rates, and communicate insights effectively.  
Each part of the analysis was carefully executed and **answered in the Excel file “Business Analytics Project.xlsx”**, showcasing hands-on business analytics skills in data preparation, funnel analysis, and cohort modeling.

