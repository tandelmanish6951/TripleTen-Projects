#  Advanced Spreadsheets: Manhattan Vacation Rental Analysis

## Project Overview

This project provides data-driven recommendations to a client interested in investing in the Manhattan vacation rental market. The analysis uses Airbnb data to identify the most attractive neighborhoods and property types for investment, and estimates the potential revenue generation of these top-performing listings.

The core analysis was performed using advanced spreadsheet techniques (Google Sheets/Excel), focusing on data cleaning, pivot tables, and conditional calculations (SUMIF, IF functions).

---

##  Key Questions Answered

The final recommendations were derived by answering the following key questions:

1.  **Which neighborhoods and property sizes are most attractive for vacation rentals?**
    * *Attractiveness was measured using the `number_of_reviews_ltm` (reviews in the last 12 months).*
2.  **How much money did these attractive listings generate?**
    * *Revenue was estimated using 30 days of calendar data and extrapolated to an annual figure.*

*(Note: The answers to these questions were provided in a multiple-choice format as part of the project submission.)*

---

##  Methodology & Analysis Steps

### 1. Data Preparation & Cleaning

* A copy of the raw data was created, and all cleaning steps were documented in a separate "Change Log" sheet.
* The `neighborhood` column was cleaned to remove inconsistent capitalization and trailing spaces, storing clean values in `neighborhood_clean`.
* The `bedrooms` column was cleaned: empty cells (representing studio apartments) were replaced with `0`, stored in `bedrooms_clean` using the `IF()` function.

### 2. Identifying Most Attractive Listings (Pivot Tables)

* **Top 10 Neighborhoods:** A pivot table was built to identify the 10 most attractive neighborhoods based on the sum of `number_of_reviews_ltm`.
    * *A bar chart was added to visualize the review count for the top 10.*
* **Most Popular Property Sizes:** A pivot table determined the most popular property sizes (`bedrooms_clean`).
    * *The analysis identified 1-bedrooms and Studios as the most popular sizes overall.*
* **Neighborhood-Specific Preferences:** The pivot table was updated to recommend the most popular property size for each of the top 10 neighborhoods.
    * *Finding: All top neighborhoods favored 1-bedrooms, except for Midtown, which favored Studios.*

### 3. Revenue Generation Calculation

* A new column, `top_listing`, was created to flag listings that matched the final recommendation criteria (Top 10 Neighborhoods + Optimal Property Size for that neighborhood).
* **Calendar Data:** The `revenue_earned` was calculated by setting the value to `adjusted_price` if `available` was "f" (rented), otherwise $0.
* **Listings Data:** The `revenue_earned` column was added using the **`SUMIF()`** function to total the 30-day revenue from the calendar data for each property.
* **Ranking:** A final pivot table was created, filtered by `top_listing = 1`, and ordered by the 30-day `revenue_earned` to find the **top-earning listing** (which earned a whopping **\$29,940**).
* **Annual Projection:** The 30-day revenue was multiplied by 12 to project the estimated annual revenue for the recommended listings.

---

## Final Deliverable Checklist

The final spreadsheet analysis included the following elements for professional submission:

*  Executive Summary and Table of Contents
*  Documented Data Cleaning Steps (Change Log)
*  Clearly Documented Assumptions
*  Consistent Formatting (Borders, colors, font styles)
*  Unnecessary columns hidden for clarity

---

##  Tools Used

* **Google Sheets / Microsoft Excel** (Advanced Functions, Pivot Tables, Charts)
* **Data Analysis**
* **Data Cleaning**
