Advanced Spreadsheets: Manhattan Airbnb Market Analysis
 Project Overview
This project analyzes Manhattan Airbnb listings to help a client identify which neighborhoods and property sizes are most profitable for vacation rentals. Using Excel’s advanced features — including pivot tables, formulas, and data cleaning — the project provides actionable insights into rental demand and estimated revenue generation across neighborhoods.
 Business Objective
A client interested in investing in Manhattan vacation rentals wants to know:
Which neighborhoods and property sizes (number of bedrooms) are most attractive for vacation rentals?
How much revenue do these listings generate?
The analysis helps guide investment decisions by highlighting high-performing neighborhoods and top-earning property types.
 Dataset
Source: NYC Airbnb Open Data
File	Description
listings	Contains Airbnb property details such as neighborhood, room type, price, and number of reviews.
calendar	Contains day-by-day availability and pricing data for each listing.
 Data Cleaning Steps
Data cleaning and preparation were completed in Excel, ensuring the dataset was consistent and analysis-ready.
Neighborhood Standardization
Fixed inconsistent capitalization and trailing spaces.
Created new column: neighborhood_clean.
Bedrooms Cleaning
Replaced empty bedroom cells (studio listings) with 0.
Created new column: bedrooms_clean using the IF() function.
Top Listing Identification
Added column top_listing in listings.
top_listing = 1 if listing is in top 10 neighborhoods and matches the most popular property size.
Revenue Calculation
Added revenue_earned in calendar:
=IF(available="f", adjusted_price, 0)
Summed 30-day total revenue and estimated annual revenue by multiplying by 12.
Used SUMIF() to pull total revenue from calendar into listings.
 Analysis & Insights
1. Most Attractive Neighborhoods
Used number_of_reviews_ltm as a proxy for attractiveness.
Built a pivot table showing total reviews per neighborhood.
Identified Top 10 neighborhoods with the highest review counts.
Added a bar chart visualizing top 10 neighborhoods.
 Insight: These neighborhoods showed the highest demand and should be prioritized for investment.
2. Most Popular Property Sizes
Built a pivot table to analyze rental popularity by bedrooms_clean.
Determined the most common property sizes (studios, 1-bedroom, 2-bedroom).
 Insight: 1-bedroom properties were most popular across most neighborhoods, except Midtown, where studios performed best.
3. Revenue Analysis for Top Listings
Focused on listings in top neighborhoods with the most popular property sizes.
Ranked top listings using total revenue_earned from the calendar table.
Estimated annual revenue using:
Annual Revenue = 30-day Revenue × 12
Insight: The top listing earned $29,940 in 30 days, equivalent to nearly $360,000 annually.
 Checklist
☑ Unnecessary columns hidden
☑ Executive summary and table of contents included
☑ Data cleaning and change log documented
☑ Consistent formatting and styling applied
☑ All multiple-choice questions answered in the spreadsheet
 Tools & Techniques Used
Excel — Pivot Tables, SUMIF, IF, and data cleaning functions
Data Validation & Cleaning — Standardized text fields and missing data
Visualizations — Bar charts and summary dashboards
Analytical Reasoning — Revenue estimation and investment recommendation
 Key Takeaways
Neighborhoods with higher review counts indicate strong rental demand.
1-bedroom listings generally yield the most consistent popularity.
Studio apartments in Midtown outperform larger listings in that area.
Combining review frequency and revenue data gives a reliable view of profitability.
 Files Included
File	Description
airbnb_manhattan.xlsx	Main analysis file with cleaned data, pivot tables, and visualizations.
README.md	Project documentation (this file).
 Summary
This project showcases Excel-based data analytics applied to a real-world business question — guiding investment strategy through insights on rental demand and revenue potential.
By integrating data cleaning, pivot analysis, and financial estimation, the results help identify the most profitable property types and neighborhoods for Manhattan vacation rentals.
