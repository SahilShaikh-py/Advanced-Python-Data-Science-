# 🗓️ 30-Day Data Analytics Master Bootcamp Schedule (150 Hours Total)

**Course Format:** 30 Days | 5 Hours Daily | 150 Total Hours  
**Daily 5-Hour Split Formula:**  
- ⏱️ **Hour 1 (Core Concept & Business Scenario):** Simple English theory + real-world analogy.  
- ⏱️ **Hour 2 (Deep-Dive Mechanics & Edge Cases):** Advanced sub-points, syntax variations, performance tips, and pitfalls.  
- ⏱️ **Hour 3 (Instructor Live Demo & Code-Along):** Step-by-step live demonstration of code/formulas.  
- ⏱️ **Hour 4 (Student Hands-On Lab):** 3 live practice exercises for students in Colab / Sheets.  
- ⏱️ **Hour 5 (Advanced Challenge & Q&A):** 1 real-world business challenge problem + doubt resolution.

---

## 📊 Phase 1: Advanced Excel for Data Analytics (Days 1 – 6 | 30 Hours)

### Day 1: Excel Interface, Data Types & Advanced Referencing
- **Hour 1:** Workbook structure, rows/columns, Primitive Data Types (Text, Number, Date, Currency).
- **Hour 2:** Relative (`A1`), Absolute (`$A$1`), and Mixed (`$A1`, `A$1`) cell referencing mechanics.
- **Hour 3:** Instructor Live Demo: Invoice automation using locked tax rate `$B$1`.
- **Hour 4:** Student Lab: 3 exercises calculating regional tax rates.
- **Hour 5:** Advanced Challenge: Multi-currency conversion model with locked FX rates.

### Day 2: Text Cleaning, String Methods & Flash Fill
- **Hour 1:** Messy data issues: trailing spaces, erratic capitalization, non-printable characters.
- **Hour 2:** `TRIM()`, `PROPER()`, `UPPER()`, `LOWER()`, `CLEAN()`, `TEXTJOIN()`, and Flash Fill (`Ctrl+E`).
- **Hour 3:** Instructor Live Demo: Cleaning messy customer CRM columns.
- **Hour 4:** Student Lab: 3 exercises parsing customer email domains and phone numbers.
- **Hour 5:** Advanced Challenge: Extracting first name, last name, and zipcode from raw text blocks.

### Day 3: Modern Lookup Formulas (`XLOOKUP`, `INDEX-MATCH` & Wildcards)
- **Hour 1:** Lookup architecture—why table merging is crucial in analytics.
- **Hour 2:** `XLOOKUP(val, lookup_rng, return_rng, [if_not_found], [match_mode])` with wildcards (`*`).
- **Hour 3:** Instructor Live Demo: Multi-column lookup and left-lookup operations.
- **Hour 4:** Student Lab: 3 exercises looking up catalog prices into daily orders.
- **Hour 5:** Advanced Challenge: Nested `XLOOKUP` for 2-way matrix table lookup.

### Day 4: Multi-Condition Aggregations (`SUMIFS`, `COUNTIFS`, `AVERAGEIFS`)
- **Hour 1:** Business reporting requirements for multi-criteria conditional math.
- **Hour 2:** Syntax mechanics of `SUMIFS`, `COUNTIFS`, `AVERAGEIFS` with date range operators (`">="&DATE()`).
- **Hour 3:** Instructor Live Demo: Aggregating sales by City, Category, and Date range.
- **Hour 4:** Student Lab: 3 exercises building category revenue summary tables.
- **Hour 5:** Advanced Challenge: Calculating average order value for Electronics items with rating ≥ 4.0.

### Day 5: Pivot Tables, Dynamic Array Formulas (`FILTER`, `UNIQUE`, `SORT`)
- **Hour 1:** Pivot Table architecture: Rows, Columns, Values, Filters, Calculated Fields.
- **Hour 2:** Modern Dynamic Array formulas: `FILTER()`, `UNIQUE()`, `SORT()` for instant reporting.
- **Hour 3:** Instructor Live Demo: Grouping dates into Quarters and creating dynamic Slicers.
- **Hour 4:** Student Lab: 3 exercises constructing dynamic summary lists using `FILTER` and `UNIQUE`.
- **Hour 5:** Advanced Challenge: Building a dynamic retail sales dashboard combining Pivot Tables and Dynamic Arrays.

### Day 6: Power Query ETL & Interactive Dashboard Design
- **Hour 1:** Introduction to Power Query for automated Extract, Transform, Load (ETL).
- **Hour 2:** Data transformations: Unpivoting columns, splitting text, removing duplicates, loading to Data Model.
- **Hour 3:** Instructor Live Demo: Connecting Pivot Charts, Slicers, and Timelines into an Executive Dashboard.
- **Hour 4:** Student Lab: 3 exercises unpivoting monthly sales tables in Power Query.
- **Hour 5:** Advanced Challenge: Building a 1-page C-suite Executive Excel Dashboard.

---

## 🛢️ Phase 2: SQL for Data Analytics (Days 7 – 12 | 30 Hours)

### Day 7: Relational Databases & Basic Queries (`SELECT`, `WHERE`, `ORDER BY`)
- **Hour 1:** Relational Database concepts (Tables, Primary/Foreign Keys, Normalization).
- **Hour 2:** Query mechanics: `SELECT`, `DISTINCT`, `WHERE` filtering, `ORDER BY`, `LIMIT`.
- **Hour 3:** Instructor Live Demo: Querying orders in SQLite inside Google Colab.
- **Hour 4:** Student Lab: 3 exercises filtering orders by city and price threshold.
- **Hour 5:** Advanced Challenge: Extracting top 10 highest value UPI orders from Mumbai.

### Day 8: Operators, Pattern Matching & Conditional Logic (`CASE WHEN`)
- **Hour 1:** Filtering operators: `LIKE '%text%'`, `IN ('A', 'B')`, `BETWEEN x AND y`, `IS NULL`.
- **Hour 2:** Conditional branching in SQL using `CASE WHEN condition THEN val ELSE val END`.
- **Hour 3:** Instructor Live Demo: Categorizing orders into 'High', 'Medium', and 'Low' value buckets.
- **Hour 4:** Student Lab: 3 exercises binning customer ratings into satisfaction tiers.
- **Hour 5:** Advanced Challenge: Writing a multi-branch `CASE WHEN` statement for regional tax rates.

### Day 9: Data Aggregation & Grouping (`GROUP BY`, `HAVING`)
- **Hour 1:** Aggregate Functions (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`).
- **Hour 2:** Categorical grouping using `GROUP BY` and filtering aggregated groups using `HAVING`.
- **Hour 3:** Instructor Live Demo: Calculating total revenue and average rating per product category.
- **Hour 4:** Student Lab: 3 exercises finding cities generating > ₹5,000 total revenue.
- **Hour 5:** Advanced Challenge: Aggregating daily sales metrics and filtering categories with > 5 orders.

### Day 10: Multi-Table Relational Joins (`INNER`, `LEFT`, `RIGHT`, `FULL OUTER`)
- **Hour 1:** Entity Relationship Diagrams (ERD) and table join mechanics.
- **Hour 2:** Writing `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, and chaining 3 tables together.
- **Hour 3:** Instructor Live Demo: Joining Orders, Customers, and Products tables.
- **Hour 4:** Student Lab: 3 exercises fetching customer names and product details for daily orders.
- **Hour 5:** Advanced Challenge: Finding customers who registered but have zero order transactions.

### Day 11: Subqueries & Common Table Expressions (`WITH` CTEs)
- **Hour 1:** Subquery types (Scalar, Column, Table) in `WHERE`, `FROM`, and `SELECT` clauses.
- **Hour 2:** Writing clean, modular queries using Common Table Expressions (`WITH cte_name AS ()`).
- **Hour 3:** Instructor Live Demo: Multi-step CTE query to find above-average spending customers.
- **Hour 4:** Student Lab: 3 exercises building subqueries to filter top product categories.
- **Hour 5:** Advanced Challenge: Chaining 2 CTEs to calculate monthly customer retention rates.

### Day 12: SQL Window Functions (`ROW_NUMBER()`, `DENSE_RANK()`, `LEAD()`, `LAG()`)
- **Hour 1:** Window Functions architecture: `OVER (PARTITION BY ... ORDER BY ...)`.
- **Hour 2:** Ranking functions (`ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`) and navigation functions (`LEAD()`, `LAG()`).
- **Hour 3:** Instructor Live Demo: Ranking top 3 sales products within each city partition.
- **Hour 4:** Student Lab: 3 exercises calculating row-by-row order difference using `LAG()`.
- **Hour 5:** Advanced Challenge: Computing Month-over-Month (MoM) revenue growth percentage using `LAG()`.

---

## 🐍 Phase 3: Python & NumPy Fundamentals (Days 13 – 18 | 30 Hours)

### Day 13: Python Environment, Variables & Primitive Types
- **Hour 1:** Google Colab environment, Notebook cells, Variable memory assignment.
- **Hour 2:** Primitive types (`int`, `float`, `str`, `bool`), Type casting (`int()`, `float()`), `type()`.
- **Hour 3:** Instructor Live Demo: Building a dynamic order bill calculator script.
- **Hour 4:** Student Lab: 3 exercises parsing user inputs and calculating final bills.
- **Hour 5:** Advanced Challenge: Multi-item invoice calculator with dynamic discount rates.

### Day 14: Decision Logic & Control Flow (`if`, `elif`, `else`)
- **Hour 1:** Boolean evaluation, Comparison (`==`, `>=`, `!=`), Logical operators (`and`, `or`, `not`).
- **Hour 2:** Nested decision blocks, 4-space indentation rules, Short-circuit evaluation.
- **Hour 3:** Instructor Live Demo: Automated customer loyalty tier classification function.
- **Hour 4:** Student Lab: 3 exercises building credit card fraud detection condition blocks.
- **Hour 5:** Advanced Challenge: Dynamic shipping charge calculator based on distance, weight, and prime status.

### Day 15: Iteration Loops (`for`, `while`) & Reusable Functions (`def`)
- **Hour 1:** Iteration mechanics: `for item in sequence`, `range(start, stop, step)`, `while` loops.
- **Hour 2:** Functions `def name(param=default): return result`, local vs global scope.
- **Hour 3:** Instructor Live Demo: Reusable function calculating GST and discount amounts across sales lists.
- **Hour 4:** Student Lab: 3 exercises creating helper functions for currency formatting.
- **Hour 5:** Advanced Challenge: Function processing a list of order dictionaries to filter high-value orders.

### Day 16: Advanced Data Structures (Lists, Dicts, Regex & Lambdas)
- **Hour 1:** Lists, 0-based indexing, list slicing `[start:stop]`, List Comprehensions `[x for x in list]`.
- **Hour 2:** Dictionaries, `.get()`, parsing nested JSON API payloads, Lambda functions `lambda x: x*2`.
- **Hour 3:** Instructor Live Demo: Parsing nested JSON customer payloads into clean flat dictionaries.
- **Hour 4:** Student Lab: 3 exercises filtering dictionary lists using list comprehensions and lambdas.
- **Hour 5:** Advanced Challenge: Text regex cleanup extracting phone numbers and email domains.

### Day 17: NumPy 1D/2D Arrays, Matrix Operations & Reshaping
- **Hour 1:** Why NumPy is $100\times$ faster than Python lists (contiguous memory architecture).
- **Hour 2:** Creating arrays `np.array()`, inspecting `.shape`, `.dtype`, 2D matrix indexing and slicing.
- **Hour 3:** Instructor Live Demo: Manipulating a $4 \times 4$ store revenue matrix.
- **Hour 4:** Student Lab: 3 exercises slicing sub-matrices and reshaping 1D arrays to 2D matrices.
- **Hour 5:** Advanced Challenge: Matrix multiplication (`np.dot()`) for product portfolio pricing.

### Day 18: Vectorization, Broadcasting & Statistics (Z-Score Outliers)
- **Hour 1:** Vectorized math (`array * 1.05`), broadcasting alignment rules across dimensions.
- **Hour 2:** Central Tendency (Mean vs Median), IQR Outlier Detection ($Q3 - Q1$), Z-Score formula ($Z = \frac{X - \mu}{\sigma}$).
- **Hour 3:** Instructor Live Demo: Detecting credit card transaction outliers using Z-Score and IQR.
- **Hour 4:** Student Lab: 3 exercises computing standard deviation and identifying outliers.
- **Hour 5:** Advanced Challenge: Building an automated outlier filtering pipeline using NumPy boolean masking.

---

## 🐼 Phase 4: Pandas Wrangling, Visualization & EDA (Days 19 – 24 | 30 Hours)

### Day 19: Pandas Series, DataFrames & GitHub CSV Import
- **Hour 1:** Pandas Series vs DataFrames architecture.
- **Hour 2:** Reading CSVs from GitHub raw URLs (`pd.read_csv`), inspecting `.head()`, `.info()`, `.describe()`.
- **Hour 3:** Instructor Live Demo: Loading `e_commerce_sales.csv` and inspecting summary statistics.
- **Hour 4:** Student Lab: 3 exercises setting index columns and inspecting dataset shape.
- **Hour 5:** Advanced Challenge: Memory optimization by downcasting numeric columns (`float64` to `float32`).

### Day 20: Data Filtering (`.loc[]`, `.iloc[]`) & Feature Engineering
- **Hour 1:** Boolean indexing `df[(df["City"]=="Mumbai") & (df["Spend"]>2000)]`.
- **Hour 2:** Selecting rows/columns via `.loc[]` (label-based) and `.iloc[]` (position-based); `.query()` method.
- **Hour 3:** Instructor Live Demo: Creating calculated features (`Total_Sales`, `Discount_Value`).
- **Hour 4:** Student Lab: 3 exercises filtering orders using `.loc[]` and `.query()`.
- **Hour 5:** Advanced Challenge: Multi-condition string filtering using `.str.contains()`.

### Day 21: Data Cleaning (Missing Values, Duplicates, String Cleanup)
- **Hour 1:** Missing data detection (`isna().sum()`) and duplicate detection (`duplicated()`).
- **Hour 2:** Imputing missing values (`fillna(median)`), dropping duplicates (`drop_duplicates()`), text cleaning (`.str.strip()`).
- **Hour 3:** Instructor Live Demo: Cleaning a dirty customer CRM DataFrame.
- **Hour 4:** Student Lab: 3 exercises imputing missing numerical values with group medians.
- **Hour 5:** Advanced Challenge: Outlier capping/winsorizing using IQR boundaries.

### Day 22: GroupBy Aggregations, Pivot Tables & Merging DataFrames
- **Hour 1:** Split-Apply-Combine framework using `df.groupby()`.
- **Hour 2:** Multi-metric summarization `.agg()`, `pivot_table()`, and table merging (`pd.merge(how='left')`).
- **Hour 3:** Instructor Live Demo: Merging Orders and Customers DataFrames and grouping by City.
- **Hour 4:** Student Lab: 3 exercises calculating revenue and average ratings grouped by Category.
- **Hour 5:** Advanced Challenge: Building a Multi-index GroupBy report with custom aggregation functions.

### Day 23: Matplotlib & Seaborn Visual Storytelling
- **Hour 1:** Principles of visual encoding (choosing Bar charts vs Line plots vs Histograms).
- **Hour 2:** Customizing plots with Matplotlib (`plt.figure()`, `plt.title()`, `plt.savefig()`) and Seaborn styling (`sns.set_theme()`).
- **Hour 3:** Instructor Live Demo: Plotting Category Revenue Bar Charts and Rating Distributions.
- **Hour 4:** Student Lab: 3 exercises plotting Violin plots and Boxplots for price distributions.
- **Hour 5:** Advanced Challenge: Creating a multi-panel $2 \times 2$ Seaborn visual dashboard grid.

### Day 24: Correlation Heatmaps & 5-Step EDA Case Study
- **Hour 1:** Pairwise Pearson correlation ($r$) and Seaborn Heatmaps (`sns.heatmap(annot=True)`).
- **Hour 2:** The 5-Step Exploratory Data Analysis (EDA) Workflow framework.
- **Hour 3:** Instructor Live Demo: Executing an end-to-end EDA on `e_commerce_sales.csv`.
- **Hour 4:** Student Lab: 3 exercises identifying key feature correlations and data anomalies.
- **Hour 5:** Advanced Challenge: Writing executive business recommendations based on EDA visual insights.

---

## 📊 Phase 5: Power BI & Capstone Projects (Days 25 – 30 | 30 Hours)

### Day 25: Power BI Desktop & Power Query Transformation
- **Hour 1:** Power BI Desktop interface, Data Connectors, importing CSV/Excel files.
- **Hour 2:** Power Query Editor transformations: data types, unpivoting, splitting columns, conditional columns.
- **Hour 3:** Instructor Live Demo: Importing raw CSVs and cleaning columns inside Power Query.
- **Hour 4:** Student Lab: 3 exercises unpivoting sales tables inside Power Query Editor.
- **Hour 5:** Advanced Challenge: Creating custom M-code parameters in Power Query.

### Day 26: Data Modeling & Relationships (Star Schema)
- **Hour 1:** Fact Tables vs Dimension Tables concept.
- **Hour 2:** Building 1-to-Many (`1:*`) relationships in Data Model View (Star Schema design).
- **Hour 3:** Instructor Live Demo: Modeling FactSales with DimCustomer, DimProduct, and DimDate tables.
- **Hour 4:** Student Lab: 3 exercises establishing active vs inactive table relationships.
- **Hour 5:** Advanced Challenge: Resolving circular relationship errors using Bridge tables.

### Day 27: DAX Masterclass (Calculated Columns vs Measures)
- **Hour 1:** Data Analysis Expressions (DAX) formula syntax and evaluation context.
- **Hour 2:** Writing Measures using `SUM()`, `AVERAGE()`, `COUNTROWS()`, `CALCULATE()`, and `ALL()`.
- **Hour 3:** Instructor Live Demo: Creating DAX measures for Total Revenue and Customer Churn Rate.
- **Hour 4:** Student Lab: 3 exercises writing DAX measures using `CALCULATE` and `FILTER`.
- **Hour 5:** Advanced Challenge: Dynamic ranking measure using `RANKX()`.

### Day 28: Time Intelligence DAX & Interactive Dashboards
- **Hour 1:** Marking Date Tables and Time Intelligence DAX functions (`TOTALYTD`, `SAMEPERIODLASTYEAR`, `DATEADD`).
- **Hour 2:** Designing interactive visuals using KPI Cards, Slicers, Line Charts, and Matrix tables.
- **Hour 3:** Instructor Live Demo: Designing a dynamic 1-page Executive Sales Dashboard.
- **Hour 4:** Student Lab: 3 exercises creating YTD revenue measures and period comparison visuals.
- **Hour 5:** Advanced Challenge: Implementing Row-Level Security (RLS) roles for regional managers.

### Day 29: Power BI Live Web Publishing & Embedding
- **Hour 1:** Publishing Power BI reports to Power BI Service (`app.powerbi.com`).
- **Hour 2:** Generating Public Web Embed links (**Publish to Web**) for online portfolio viewing.
- **Hour 3:** Instructor Live Demo: Embedding live interactive dashboards into Markdown portfolio notebooks.
- **Hour 4:** Student Lab: 3 exercises publishing reports and generating public embed links.
- **Hour 5:** Advanced Challenge: Setting up scheduled dataset refreshes in Power BI Service.

### Day 30: End-to-End Guided Capstone Project & Portfolio Setup
- **Hour 1:** Capstone Project presentation (E-Commerce Sales & Revenue Optimization).
- **Hour 2:** Structuring GitHub Data Analytics portfolio repositories.
- **Hour 3:** Instructor Live Demo: Code review and polishing student portfolio projects.
- **Hour 4:** Student Lab: Finalizing Capstone README and Colab links.
- **Hour 5:** Resume building, LinkedIn profile optimization, and Mock Technical Interview Q&A.
