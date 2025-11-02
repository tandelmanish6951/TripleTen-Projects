# 🏙️ Advanced Spreadsheets: Manhattan Airbnb Market Analysis  

## 📘 Project Overview  

This project analyzes **Airbnb listings in Manhattan** to help a client identify which **neighborhoods and property sizes** are most profitable for vacation rentals.  
By leveraging **pivot tables, data cleaning, and spreadsheet functions**, the analysis provides actionable insights into the **most attractive neighborhoods**, **popular property sizes**, and **revenue potential** of top listings.  

---

## 🧩 Business Objective  

A client interested in investing in Manhattan vacation rentals wants to know:
1. Which **neighborhoods and property sizes** (number of bedrooms) are most attractive for vacation rentals?  
2. How much **revenue** do these listings generate?

The analysis aims to guide investment decisions by identifying high-performing listings and estimating potential annual earnings.

---

## 💾 Dataset  

**Source:** NYC Airbnb Open Data  
- **listings** — contains property information such as neighborhood, room type, price, and number of reviews.  
- **calendar** — contains availability and pricing data for each day per listing.  

---

## 🧹 Data Cleaning Steps  

Data cleaning and preparation were performed using Excel functions and formulas.  

1. **Neighborhood Standardization**  
   - Cleaned inconsistent capitalization and removed trailing spaces.  
   - Created a new column: `neighborhood_clean`.  

2. **Bedrooms Cleaning**  
   - Replaced empty bedroom cells (representing studios) with `0`.  
   - Created a new column: `bedrooms_clean` using the `IF()` function.  

3. **Top Listing Identification**  
   - Created a new column `top_listing` in the listings dataset.  
   - Value = `1` if the listing belongs to the **top 10 neighborhoods** and matches the **most popular property size**; otherwise, `0`.  

4. **Revenue Calculation**  
   - In the **calendar**
