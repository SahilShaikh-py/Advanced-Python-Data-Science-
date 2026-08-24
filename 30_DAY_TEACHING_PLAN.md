# 🗓️ 30-Day Data Analytics Bootcamp Master Teaching Schedule

**Course Format:** 30 Days | 3 Hours Daily | 90 Total Hours  
**Daily Split Formula:**  
- ⏱️ **Hour 1 (Concept & Business Scenario):** Simple English theory + Real-world analogy.  
- ⏱️ **Hour 2 (Instructor Live Practical Demo):** Screen share live practical coding/formulas.  
- ⏱️ **Hour 3 (Student Practice Lab & Doubts):** 2 live practice exercises for students + doubt resolution.

---

## 📊 Phase 1: Advanced Excel for Data Analytics (Days 1 – 6 | 18 Hours)

### Day 1: Excel Interface, Data Types & Cell Referencing
- **Hour 1:** Excel workbook structure, rows/columns, Primitive Data Types (Text, Number, Date, Currency).
- **Hour 2:** Relative Referencing (`A1`) vs Absolute Referencing (`$A$1`) for tax calculations.
- **Hour 3:** Lab Exercise: Building an automated invoice calculator using `$A$1` tax rates.

### Day 2: Text Cleaning & Data Wrangling Formulas
- **Hour 1:** Common messy text data issues (spaces, inconsistent capitalization).
- **Hour 2:** Applying `TRIM()`, `PROPER()`, `UPPER()`, `LOWER()`, `CONCATENATE()`, and Flash Fill (`Ctrl+E`).
- **Hour 3:** Lab Exercise: Cleaning messy customer CRM name and phone number columns.

### Day 3: Modern Lookup Formulas (`XLOOKUP` & `VLOOKUP`)
- **Hour 1:** Why lookup formulas are essential for merging tables in Excel.
- **Hour 2:** Master `XLOOKUP(lookup_val, lookup_range, return_range, [if_not_found])` vs `VLOOKUP()`.
- **Hour 3:** Lab Exercise: Merging Product Prices into Order Transaction tables using `XLOOKUP`.

### Day 4: Multi-Condition Aggregations (`SUMIFS` & `COUNTIFS`)
- **Hour 1:** Conditional math logic for business executive reporting.
- **Hour 2:** `SUMIFS(sum_range, criteria_range1, criteria1, ...)` and `COUNTIFS()`.
- **Hour 3:** Lab Exercise: Summarizing total city sales for Electronics items > ₹1,000.

### Day 5: Pivot Tables, Grouping & Interactive Slicers
- **Hour 1:** Pivot Table architecture—Rows, Columns, Values, Filters.
- **Hour 2:** Grouping dates into Months/Quarters, Calculated Fields, and adding Slicers.
- **Hour 3:** Lab Exercise: Building a dynamic retail sales Pivot Table report.

### Day 6: Power Query ETL & Excel Dashboarding
- **Hour 1:** Introduction to Power Query for automated data extraction and cleaning.
- **Hour 2:** Unpivoting columns, removing duplicates, and connecting Pivot Charts into an Executive Dashboard.
- **Hour 3:** Lab Exercise: Building an interactive 1-page Excel Sales Dashboard.

---

## 🛢️ Phase 2: SQL for Data Analytics (Days 7 – 12 | 18 Hours)

### Day 7: Relational Databases & Basic Queries (`SELECT`, `WHERE`)
- **Hour 1:** Relational Database concepts (Tables, Rows, Columns, Primary/Foreign Keys).
- **Hour 2:** Writing `SELECT`, `DISTINCT`, `WHERE` filtering with SQLite in Python Colab.
- **Hour 3:** Lab Exercise: Querying customer orders with ratings ≥ 4.5.

### Day 8: Sorting, Pattern Matching & Operators
- **Hour 1:** Operators in SQL (`LIKE '%text%'`, `IN ('A', 'B')`, `BETWEEN x AND y`).
- **Hour 2:** Sorting query outputs using `ORDER BY column ASC/DESC` and `LIMIT n`.
- **Hour 3:** Lab Exercise: Extracting top 5 highest order sales in Mumbai and Delhi.

### Day 9: Data Aggregation & Grouping (`GROUP BY`, `HAVING`)
- **Hour 1:** Aggregate Functions (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`).
- **Hour 2:** Categorical summarization using `GROUP BY` and filtering groups using `HAVING`.
- **Hour 3:** Lab Exercise: Calculating total revenue and average rating per product category.

### Day 10: Relational Table Joins (`INNER`, `LEFT` Joins)
- **Hour 1:** Entity Relationship Diagrams (ERD) and why datasets are normalized.
- **Hour 2:** Writing `INNER JOIN` and `LEFT JOIN` queries between Customers and Orders tables.
- **Hour 3:** Lab Exercise: Joining customer profiles with transaction history.

### Day 11: Subqueries & Common Table Expressions (`WITH` CTEs)
- **Hour 1:** Nested logic in SQL (Subqueries in `WHERE` vs `FROM` clauses).
- **Hour 2:** Writing clean, readable queries using Common Table Expressions (`WITH cte_name AS ()`).
- **Hour 3:** Lab Exercise: Finding customers whose spend is above the overall average customer spend.

### Day 12: SQL Window Functions (`DENSE_RANK()`, `ROW_NUMBER()`)
- **Hour 1:** Difference between `GROUP BY` (collapses rows) and Window Functions (keeps rows).
- **Hour 2:** Applying `ROW_NUMBER() OVER (PARTITION BY ... ORDER BY ...)` and `DENSE_RANK()`.
- **Hour 3:** Lab Exercise: Ranking top 3 products sold in each city.

---

## 🐍 Phase 3: Python & NumPy Fundamentals (Days 13 – 18 | 18 Hours)

### Day 13: Python Setup, Variables & Primitive Data Types
- **Hour 1:** Google Colab workflow, Code vs Text cells, Variable assignment in memory.
- **Hour 2:** Primitive types (`int`, `float`, `str`, `bool`), type casting (`int()`, `float()`), `type()`.
- **Hour 3:** Lab Exercise: Building a dynamic delivery bill calculator script.

### Day 14: Decision Logic & Control Flow (`if`, `elif`, `else`)
- **Hour 1:** Boolean conditions, comparison operators (`==`, `>=`, `!=`), logical operators (`and`, `or`).
- **Hour 2:** Multi-branch decision blocks with 4-space indentation rules.
- **Hour 3:** Lab Exercise: Writing an automated customer loyalty tier classification function.

### Day 15: Iteration Loops (`for`, `while`) & Functions (`def`)
- **Hour 1:** Automated repetition using `for item in sequence` and `range(start, stop)`.
- **Hour 2:** Modular functions with `def name(param=default): return result`.
- **Hour 3:** Lab Exercise: Writing a reusable function to calculate GST and discounts on sales lists.

### Day 16: Advanced Data Structures (Lists & Dictionaries)
- **Hour 1:** Lists, 0-based indexing, list slicing `[start:stop]`, and List Comprehensions `[x for x in list]`.
- **Hour 2:** Dictionaries (Key-Value storage), `.get()`, and parsing nested JSON API payloads.
- **Hour 3:** Lab Exercise: Extracting customer order totals from nested JSON dictionaries.

### Day 17: NumPy 1D & 2D Arrays & Matrix Slicing
- **Hour 1:** Why NumPy is $100\times$ faster than Python lists (contiguous memory architecture).
- **Hour 2:** Creating arrays `np.array()`, inspecting `.shape`, `.dtype`, 2D matrix slicing.
- **Hour 3:** Lab Exercise: Processing a $4 \times 4$ store sales matrix to calculate regional totals.

### Day 18: Vectorization, Broadcasting & Business Statistics
- **Hour 1:** Vectorized math (`array * 1.05`), broadcasting alignment rules.
- **Hour 2:** Central Tendency (Mean vs Median in skewed data) & IQR Outlier Detection ($Q3 - Q1$).
- **Hour 3:** Lab Exercise: Detecting credit card transaction outliers using the IQR rule.

---

## 🐼 Phase 4: Pandas Wrangling, Visualization & EDA (Days 19 – 24 | 18 Hours)

### Day 19: Pandas DataFrames & Loading GitHub CSVs
- **Hour 1:** Pandas Series vs DataFrames architecture.
- **Hour 2:** Reading CSVs from GitHub raw URLs (`pd.read_csv`), inspecting `.head()`, `.info()`, `.describe()`.
- **Hour 3:** Lab Exercise: Loading `e_commerce_sales.csv` and inspecting column summary stats.

### Day 20: Data Filtering (`.loc[]`, `.iloc[]`) & Feature Engineering
- **Hour 1:** Conditional row filtering using boolean indexing `df[(df["City"]=="Mumbai")]`.
- **Hour 2:** Selecting rows/columns via `.loc[]` (label-based) and `.iloc[]` (position-based); creating new columns.
- **Hour 3:** Lab Exercise: Creating a `Total_Sales` column and filtering high-value UPI orders.

### Day 21: Data Cleaning (Missing Data, Duplicates, Text Cleanup)
- **Hour 1:** Identifying missing values (`isna().sum()`) and duplicate rows (`duplicated()`).
- **Hour 2:** Imputing missing values (`fillna(median)`), dropping rows (`dropna()`), string operations (`.str`).
- **Hour 3:** Lab Exercise: Cleaning a dirty customer CRM DataFrame.

### Day 22: GroupBy Aggregations & Merging DataFrames
- **Hour 1:** Split-Apply-Combine pattern using `df.groupby()`.
- **Hour 2:** Multi-metric summarization `.agg()`, `pivot_table()`, and merging tables (`pd.merge()`).
- **Hour 3:** Lab Exercise: Building an executive summary of revenue and ratings grouped by City.

### Day 23: Matplotlib & Seaborn Visual Storytelling
- **Hour 1:** Visual encoding principles (choosing Bar charts vs Line plots vs Histograms).
- **Hour 2:** Customizing plots with Matplotlib (`plt.figure()`, `plt.title()`, `plt.savefig()`) and Seaborn styling.
- **Hour 3:** Lab Exercise: Plotting Category Revenue Bar Charts and Rating Distributions.

### Day 24: Correlation Heatmaps & 5-Step EDA Case Study
- **Hour 1:** Pairwise Pearson correlation ($r$) and Seaborn Heatmaps (`sns.heatmap(annot=True)`).
- **Hour 2:** The 5-Step Exploratory Data Analysis (EDA) Workflow framework.
- **Hour 3:** Lab Exercise: Performing an end-to-end EDA on the `e_commerce_sales.csv` dataset.

---

## 📊 Phase 5: Power BI & Capstone Projects (Days 25 – 30 | 18 Hours)

### Day 25: Power BI Desktop & Power Query Transformation
- **Hour 1:** Power BI Desktop interface, Data Connectors, and importing CSV/Excel files.
- **Hour 2:** Data transformation in Power Query Editor (changing data types, splitting columns).
- **Hour 3:** Lab Exercise: Importing and cleaning raw sales data inside Power Query.

### Day 26: Data Modeling & Relationships (Star Schema)
- **Hour 1:** Fact Tables vs Dimension Tables concept.
- **Hour 2:** Building 1-to-Many relationships in Data Model View (Star Schema design).
- **Hour 3:** Lab Exercise: Modeling FactSales with DimCustomer and DimProduct tables.

### Day 27: DAX Fundamentals (Calculated Columns vs Measures)
- **Hour 1:** Introduction to Data Analysis Expressions (DAX) formula syntax.
- **Hour 2:** Writing Measures using `SUM()`, `AVERAGE()`, `COUNTROWS()`, and `CALCULATE()`.
- **Hour 3:** Lab Exercise: Creating dynamic DAX measures for Total Revenue and Order Count.

### Day 28: Time Intelligence DAX & Dynamic Visual Dashboards
- **Hour 1:** Date tables and Time Intelligence DAX functions (`TOTALYTD`, `SAMEPERIODLASTYEAR`).
- **Hour 2:** Building interactive visual reports using KPI Cards, Slicers, Line Charts, and Matrix visuals.
- **Hour 3:** Lab Exercise: Designing a dynamic 1-page Sales Performance Dashboard.

### Day 29: Power BI Live Web Publishing & Embedding
- **Hour 1:** Publishing Power BI reports to Power BI Service (`app.powerbi.com`).
- **Hour 2:** Generating Public Web Embed links (**Publish to Web**) for online portfolio viewing.
- **Hour 3:** Lab Exercise: Embedding live interactive dashboards into Markdown notebooks.

### Day 30: End-to-End Guided Capstone Project & Portfolio Setup
- **Hour 1:** Capstone Project presentation (E-Commerce Revenue Optimization).
- **Hour 2:** Structuring GitHub Data Analytics portfolio repositories.
- **Hour 3:** Resume building, LinkedIn profile optimization, and Mock Technical Interview Q&A.
