#  SQL Analysis Project

Welcome to the VentureInsight SQL Project, where I completed a series of real-world data analysis tasks designed to simulate the responsibilities of a Data Analyst at a venture research firm.  
Each question in this project was answered using SQL, applying concepts such as aggregation, filtering, pattern matching, grouping, and joins.

---

##  Project Overview

At VentureInsight, a fictional research firm, analysts support venture capital clients by uncovering insights from startup, funding, and acquisition data.  
The database contains several interconnected tables:

- **company** — information about startups (funding, status, category)  
- **fund** — details about venture capital funds  
- **funding_round** — investment round data  
- **investment** — records of specific investments  
- **acquisition** — details about company acquisitions  
- **people** — data on founders, employees, and investors  
- **education** — educational backgrounds of individuals  

Each task in this project represents a real business question that could influence investment strategy and portfolio management.  

---

##  SQL Tasks and Objectives

Below is a summary of each analytical task completed in this project.  
All questions were answered using SQL queries.

### 1. Startup Landscape Analysis
**Goal:** Determine how many companies have failed (closed down) versus those still operating or acquired.  
**Skills Used:** `SELECT`, `COUNT`, `WHERE` filtering  

---

### 2. Sector Analysis for US Investors
**Goal:** Identify how much funding news-related companies from the USA have raised historically.  
**Skills Used:** `WHERE` with multiple conditions, `ORDER BY`  

---

### 3. Analyzing Cash Acquisitions
**Goal:** Find the total cash-based acquisitions from 2011–2013 to understand post-recession acquisition trends.  
**Skills Used:** `SUM`, `WHERE` (date range), `AND` logic  

---

### 4. Identifying Industry Influencers
**Goal:** Retrieve people whose Twitter usernames start with "Silver" for marketing outreach.  
**Skills Used:** `LIKE` pattern matching  

---

### 5. Finding Finance Influencers
**Goal:** Identify finance influencers with `"money"` in their Twitter handle and last names starting with `'K'`.  
**Skills Used:** `LIKE`, multiple `WHERE` conditions  

---

### 6. Geographic Investment Analysis
**Goal:** Calculate the total amount of funding raised by companies per country.  
**Skills Used:** `GROUP BY`, `SUM`, `ORDER BY`  

---

### 7. Funding Round Volatility Analysis
**Goal:** Examine days with both small and large funding rounds, excluding days with zero funding.  
**Skills Used:** `GROUP BY`, `HAVING`, aggregation filters  

---

### 8. Fund Activity Classification
**Goal:** Classify funds into three categories:  
- `high_activity` (≥100 investments)  
- `middle_activity` (20–99 investments)  
- `low_activity` (<20 investments)  
**Skills Used:** `CASE`, conditional logic  

---

### 9. Investment Strategy by Fund Activity
**Goal:** Compare the average number of funding rounds across fund activity levels to identify strategy trends.  
**Skills Used:** `CASE`, `AVG`, `GROUP BY`, `ORDER BY`  

---

### 10. Employee Education Impact on Startup Success
**Goal:** Analyze whether education correlates with company success by:  
- Finding companies that closed after one funding round  
- Joining employee and education data  
- Calculating average degrees per employee at failed startups  
**Skills Used:** `JOIN`, `SUBQUERY`, `AVG`  

``` sql
SELECT AVG(t.total_degree_type)
FROM 
    (SELECT p.id,
      COUNT(e.degree_type) AS total_degree_type
      FROM people AS p JOIN education AS e ON p.id = e.person_id
      WHERE company_id IN (SELECT id
                           FROM company 
                           WHERE id IN (SELECT company_id
                                        FROM funding_round
                                        WHERE is_first_round = 1 AND is_last_round = 1)
                                        AND status = 'closed')
      GROUP BY p.id) AS t;
```
---

##  Key Concepts Practiced
- SQL data exploration and cleaning  
- Aggregation (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`)  
- Filtering and logical operators  
- Pattern matching with `LIKE`  
- Data grouping and summarization (`GROUP BY`, `HAVING`)  
- Conditional categorization using `CASE`  
- Complex joins and subqueries  

---

###  Summary

This project demonstrates practical SQL proficiency applied to real-world business analysis scenarios — from startup success tracking to investor strategy insights.  
Each question showcases data manipulation, querying logic, and analytical reasoning essential for any aspiring Data Analyst or Business Intelligence professional.
