# Power BI Project 

Welcome to my Power BI project analyzing data from the Shopify App Store. This project explores what factors contribute to the success of Shopify apps by examining app details, categories, and user reviews through interactive Power BI visualizations.

---

##  Project Overview

As data analyst, my goal was to uncover insights about the Shopify App ecosystem — including app performance, developer engagement, and user feedback patterns. Using Power BI, I developed visuals and KPIs to evaluate app popularity, review trends, developer responsiveness, and overall customer sentiment. Each part of the project corresponds to a dedicated report page in Power BI.

---

##  Dataset

**File Used:** `shopify.xlsx`  
This dataset contains public data scraped from the Shopify App Store and includes 4 tables:

| Table | Description |
|--------|--------------|
| **apps** | Contains details of all apps in the Shopify marketplace. |
| **apps_categories** | Join table linking apps to their associated categories. |
| **categories** | Lists all available app categories. Each app can have multiple categories. |
| **reviews** | Contains user reviews, ratings, and developer replies for each app. |

---

##  Project Structure

Each section below corresponds to a Power BI report page, where individual questions are visualized through charts, KPIs, and calculated measures.  
 Screenshots were captured for each question answered.

---

### 1. App Landscape

**Power BI Page:** `App Landscape`  
**Dataset Used:** `apps` table  
This section provides a broad overview of the Shopify app ecosystem.

#### Visuals Created:
| Task | Visualization Type | Description |
|------|--------------------|--------------|
| 1. Count of unique apps | KPI Card | Displays the total number of unique apps in the Shopify App Store. |
| 2. Review trends over time | Line Chart | Shows the sum of review counts (`reviews_count`) over time using `lastmod` date on the X-axis. |
| 3. Reviews vs. Ratings | Scatterplot + Text Box | Displays the correlation between review volume and average rating. Added annotations to interpret the pattern. |

---

### 2. Reviews

**Power BI Page:** `Reviews`  
**Dataset Used:** `reviews` table  
This section evaluates review sentiment and developer responsiveness.

#### Visuals and Calculations:
| Task | Visualization Type | Description |
|------|--------------------|--------------|
| 1. Weighted helpful reviews | KPI Card | Created a calculated column using DAX: `helpful_reviews = rating * (1 + helpful_count)` and displayed its average. |
| 2. Developer responsiveness | Scatterplot | Created a new column `developer_answered` = 1 if a developer replied, else 0. Plotted average rating vs developer_answered. |

---

### 3. App Reviews

**Power BI Page:** `App Reviews`  
**Dataset Used:** `apps` and `reviews` tables  
This section focuses on developer-level performance and engagement metrics.

#### Relationships:
- Created a many-to-one relationship between:
  - `reviews[app_id]` → `apps[id]`

#### Visuals Created:
| Task | Visualization Type | Description |
|------|--------------------|--------------|
| 1. Developer vs. Total Rating | Bar Chart | Shows total sum of rating by developer (preliminary overview). |
| 2. Developer vs. Helpful Review Average | Bar Chart | Replaces misleading total ratings with average of the `helpful_reviews` column for a more accurate view. |
| 3. Developer Responsiveness | Bar Chart with Filter | Shows which developers are most responsive using the `developer_answered` column. Applied filter: `reviews_count > 500`. |

---

### 4. Project Organization & Submission

- Each part of the project corresponds to a separate page in Power BI:
  - `App Landscape`
  - `Reviews`
  - `App Reviews`
- Each question and sub-question has a corresponding visualization.
- Screenshots were captured for each sub-question for documentation and presentation.

 **Deliverable:** `Shopify App Analysis.pbix`  
 **Screenshots:** 3 images 
---
 
##  Files Included

| File | Description |
|------|--------------|
| `Shopify App Analysis.pbix` | Power BI file used for final submission |
| `shopify.xlsx` | Excel file imported in Power BI. |
| `3 image files` | Image files used for this project. |
| `README.md` | This file |

---

##  Tools & Techniques Used

- **Power BI Desktop**
- **Data Modeling:** Table relationships and schema building
- **DAX Calculations:** Custom columns and measures
  - `helpful_reviews = rating * (1 + helpful_count)`
  - `developer_answered = IF(NOT(ISBLANK(developer_reply)), 1, 0)`
- **Visualizations:** KPI Cards, Bar Charts, Line Charts, Scatterplots
- **Filtering & Interactivity:** Page-level and visual-level filters
- **Annotations & Text Boxes** for interpretative storytelling

---

##  Key Insights

- Apps with more reviews tend to have a higher visibility but not necessarily higher ratings.  
- Developers who respond to user reviews tend to maintain higher average ratings.  
- Some categories and developers consistently outperform others, suggesting strong user trust and engagement.  
- Filtering high-review-count developers helps identify top-performing and responsive teams.

---

##  Summary

This Power BI project demonstrates how data modeling and visualization can reveal key insights from complex app marketplace data. By integrating DAX expressions, relational modeling, and visual storytelling, I identified the drivers of app success and developer responsiveness on the Shopify platform.
