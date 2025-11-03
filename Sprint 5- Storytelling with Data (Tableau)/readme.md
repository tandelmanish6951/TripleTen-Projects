# Storytelling with Data — Tableau Project

Welcome to my Storytelling with Data project, where I analyzed the Superstore dataset to uncover the root causes of product returns and developed a Tableau Story for executive presentation.

---

## Project Overview

The Superstore is experiencing a high number of returned orders, and the CEO wants to understand why customers are returning items and how to reduce return rates. This project uses Tableau to explore, visualize, and communicate insights that identify patterns, correlations, and key business drivers behind returns.

---

## Dataset

**File Used:** `Superstore.xls`  
**Tables:**
- **Orders:** Contains details about sales, discounts, quantity, profits, and products.
- **Returns:** Contains information on which orders were returned.
- **People (optional):** Regional manager information.

---

### 1. What is Causing Returns?

In this section, I explored multiple visual perspectives to determine why certain orders were returned.  
The `Returns` table was LEFT JOINED to the `Orders` table, and a calculated field (`Returned`) was created where:
- `"Yes"` = 1  
- `"Null"` = 0  

The average of this field represents the return rate, and the sum represents total returns.

#### Worksheets Created:
| Question | Visualization Type | Tableau Sheet Name | Description |
|-----------|--------------------|--------------------|--------------|
| Correlation between total sales and total returns | Scatterplot (by subcategory) | `Sales vs Returns` | Analyzed relationship between sales volume and return frequency. |
| Return rate by product category | Bar Chart | `Return Rate by Category` | Compared categories to find those with the highest return rates. |
| Return rate by customer | Bar Chart + Filter | `Return Rate by Customer` | Identified customers prone to returns (excluded single-order customers). |
| Return rate by geography | Map Visualization | `Return Rate by State` | Highlighted regions with unusually high return percentages. |
| Return rate by time | Line Chart | `Return Rate Over Time` | Tracked seasonal or monthly trends in returns. |
| Composite analyses | Dual/Combined Charts | `Composite Factors Analysis` | Combined multiple factors (e.g., category + date + state) to find multi-dimensional return causes. |

---

### 2.Building a Dashboard for Monitoring Returns

The next phase was to design and build a dashboard that consolidates key visualizations and allows the CEO to monitor return performance interactively.

#### Steps Followed:
1. Low-Fidelity Mockups
   - Created 3 sketches of dashboard layouts and select most effective design for the final build.

2. Dashboard Template Creation
   - Built a template using empty containers in Tableau and take a screenshot of the empty layout. 

3. Final Dashboard Assembly
   - Added worksheets, filters, and key metrics.
   - Applied professional formatting, color consistency, and branding.

---

### 3. Presenting the Analysis and Story

To communicate findings effectively, I created a Tableau Story that walks through the analysis and key takeaways in a structured narrative for executive review.

#### Story Structure:
| Story Section | Description | Tableau Element |
|----------------|-------------|-----------------|
| **Introduction** | Overview of the problem and objective | Story Point 1 |
| **Measuring Returns** | Compared different metrics — total returns, cost of returns, and return rate — to identify the most meaningful KPI. | Story Point 2 |
| **Root Cause Analysis** | Highlighted visual evidence of high-return categories, customers, and regions. | Story Point 3 |
| **Dashboard Walkthrough** | Demonstrated how to interact with the dashboard and interpret filters. | Story Point 4 |
| **Actions & Recommendations** | Suggested operational changes to reduce returns (e.g., quality checks, regional review, high-return product audit). | Story Point 5 |
| **Conclusion** | Summarized key insights and next steps for implementation. | Story Point 6 |

---

## Files Included

| File | Description |
|------|--------------|
| `Sprint 4 Project-twbx.zip` | Project report zip file used for final submission |
| `Superstore.xls` | Excel file used for data evaluation |
| `README.md` | This file |

---

## Tools & Techniques Used
- Data Preparation (LEFT JOIN, Calculated Fields)
- Aggregations & Return Rate Calculations
- Data Storytelling Techniques
- Dashboard & Storyboard Design
- Trend and Correlation Analysis
- Visualization Types: Scatterplots, Bar Charts, Maps, Line Charts, Composite Charts

---


### Summary

This project demonstrates how data storytelling transforms analytics into actionable business decisions. 
Through Tableau visualizations, dashboards, and stories, I identified key drivers of product returns, built an interactive executive dashboard, and presented a narrative for reducing return rates.  

