# Data Visualization with Tableau

Welcome to my **Data Visualization with Tableau Project**, where I analyzed the **Superstore dataset** to uncover insights on profitability, advertising strategies, and product returns.  
All project tasks and visualizations were **answered and built in the Tableau workbook file: “Sprint 4 Project-twbx.zip.”**

---

## Project Overview

The fictional **Superstore** is facing major profitability challenges.  
As a consultant, my goal was to analyze the store’s sales, profit, and return data to recommend **profitable product strategies**, **advertising opportunities**, and **loss reduction tactics** through **data-driven visualizations** built in **Tableau Desktop**.

---

## Dataset

**File Used:** `Superstore.xls`  
**Source:** Provided dataset simulating Superstore’s transactional and returns data.  
**Tables Included:**
- **Orders:** Sales, quantity, discounts, profits, categories, customer info
- **Returns:** Information on product returns
- **People:** Regional managers (optional join)

---

## Project Tasks & Deliverables
All questions below were **answered in Tableau** and saved within **Sprint 4 Project-twbx.zip**.

---

### Part 1: Profits & Losses
**Goal:** Identify key profit and loss centers across the business.

#### Tasks:
1. Determine the **two biggest profit centers** and **two biggest loss-makers** using combinations of dimensions (e.g., subcategory + region, shipping mode + product ID).  
   - 🔍 Visualization: Profit comparison across dimension pairs.  
   - **Answered in Tableau (Sheet: Profit Centers)**  

2. Identify **which products the store should stop selling.**  
   - 🔍 Visualization: Product profitability distribution.  
   - **Answered in Tableau (Sheet: Product Losses)**  

3. Determine **3 product subcategories to focus on** and **3 to stop selling.**  
   - 🔍 Visualization: Profit by subcategory bar chart.  
   - **Answered in Tableau (Sheet: Subcategory Strategy)**  

---

### Part 2: Advertising Strategy
**Goal:** Evaluate the best time and place for advertising based on profitability trends.

#### Tasks:
1. Identify the **3 best state-month combinations** for advertising based on average profit trends.  
   - 🔍 Visualization: Line charts of average profit by month for selected states.  
   - **Answered in Tableau (Sheet: Advertising Opportunities)**  

2. Calculate the **advertising budget limit** assuming the store should spend **1/5 of profits** on advertising.  
   - 🔍 Visualization: Profit-to-ad-spend ratio per month and state.  
   - **Answered in Tableau (Sheet: Ad Spend Strategy)**  

---

### Part 3: Returned Items Analysis
**Goal:** Detect patterns in product and customer returns and assess their profitability impact.

#### Tasks:
1. **Join** the `Returns` table to the `Orders` table using a **LEFT JOIN** to analyze returned vs. non-returned products.  
   - Created a **calculated field** `Returned` (Yes = 1, Null = 0).  

2. Identify **products with the highest return rate.**  
   - 🔍 Visualization: Return rate by product.  
   - **Answered in Tableau (Sheet: Product Returns)**  

3. Identify **customers with the highest return rate.**  
   - 🔍 Visualization: Return rate by customer.  
   - **Answered in Tableau (Sheet: Customer Returns)**  

4. Visualize **average profit vs. average return rate** across a chosen dimension (e.g., state or shipping mode).  
   - 🔍 Visualization: Scatter plot comparing profitability and return rate.  
   - **Answered in Tableau (Sheet: Profit vs Return Analysis)**  

---

## Deliverables Summary
| Part | Task Description | Tableau Sheet Name | File |
|------|------------------|--------------------|------|
| 1 | Profit & Loss Centers | `Profit Centers`, `Product Losses`, `Subcategory Strategy` | Sprint 4 Project-twbx.zip |
| 2 | Advertising Analysis | `Advertising Opportunities`, `Ad Spend Strategy` | Sprint 4 Project-twbx.zip |
| 3 | Return Analysis | `Product Returns`, `Customer Returns`, `Profit vs Return Analysis` | Sprint 4 Project-twbx.zip |

---

## Tableau Public Dashboard

 **View Interactive Dashboard Here:**  
 [Tableau Public Link](https://public.tableau.com/)

*(Replace this link with your published dashboard URL once uploaded to Tableau Public.)*

---

## Tools & Techniques Used
- **Tableau Desktop**
- Data Cleaning & Joining (LEFT JOIN)
- Calculated Fields (`Returned`)
- Aggregations & Filtering
- Profitability and Return Analysis
- Line Charts, Bar Charts, Scatter Plots
- KPI Design & Storytelling
---

### Summary

This project demonstrates how **data visualization can uncover business insights** — from profit analysis and advertising strategy to product return behavior.  
Each task was completed in **Tableau** and saved in the **“Sprint 4 Project-twbx.zip”** file, highlighting skills in **data storytelling**, **visual analytics**, and **strategic business recommendations**.
