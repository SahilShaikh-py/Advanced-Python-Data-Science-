# 📘 Master Data Analytics Teaching Syllabus (150-Hour Zero-to-Hero Guide)

> **Course Philosophy:** Built for absolute beginners and non-programmers. Every single topic is structured into 3 clear parts:
> 1. 📌 **Definition:** Beginner-friendly explanation in simple English.
> 2. 📖 **Key Theory (5 Short Bullet Points):** Purpose, Analogy, Syntax, Pitfalls, and Business Application.
> 3. 💻 **Code / Formula Example with Explanation Comments:** Production code/formulas with line-by-line comments.

---

# Phase 1: Advanced Excel for Data Analytics (Days 1 – 6)

## Topic 1.1: Cell Referencing (Relative vs Absolute `$A$1` vs Mixed `$A1`)

📌 **Definition:**
**Cell Referencing** specifies cell addresses in formulas and controls whether coordinates change or stay locked when formulas are copied across rows/columns.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Relative Referencing (`A1`):** Cell reference automatically shifts when dragged down or across.
- 🔹 **Absolute Referencing (`$A$1`):** Dollar signs (`$`) lock both row and column coordinates permanently.
- 🔹 **Mixed Referencing (`$A1` / `A$1`):** Locks only the column (`$A1`) or only the row (`A$1`).
- 🔹 **Analogy:** Like anchoring a boat—no matter where you drag the formula, `$A$1` stays anchored to one cell.
- 🔹 **Industry Application:** Applying static tax rates (e.g., 18% GST in cell `$B$1`) across thousands of product prices.

💻 **Formula Example with Explanation Comments:**
```excel
=B2 * $B$1
' Explanation:
' B2 is Relative: multiplies current row product price
' $B$1 is Absolute: locks static 18% GST rate stored in cell B1
```

---

## Topic 1.2: Modern Lookup Formulas (`XLOOKUP` & Wildcards)

📌 **Definition:**
`XLOOKUP` searches a lookup column for a value and returns a corresponding result from another column.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Merges data across separate sheets without copying and pasting manually.
- 🔹 **Syntax:** `=XLOOKUP(lookup_val, lookup_range, return_range, [if_not_found], [match_mode])`.
- 🔹 **Left & Right Lookup:** Unlike `VLOOKUP`, `XLOOKUP` can look to the left or right seamlessly.
- 🔹 **Wildcard Search:** Supports wildcard characters (`*` for multi-character, `?` for single character).
- 🔹 **Industry Application:** Fetching product prices and customer addresses into transaction tables.

💻 **Formula Example with Explanation Comments:**
```excel
=XLOOKUP(A2, Products[Product_ID], Products[Unit_Price], "Not Found")
' Explanation:
' A2: The Order Product ID to search for
' Products[Product_ID]: Column in Catalog to search within
' Products[Unit_Price]: Column containing the price to return
' "Not Found": Fallback text if Product ID does not exist
```

---

## Topic 1.3: Dynamic Array Formulas (`FILTER`, `UNIQUE`, `SORT`)

📌 **Definition:**
**Dynamic Array Formulas** automatically spill multiple calculated results into neighboring cells based on a single formula.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **`FILTER(array, include)`:** Filters a data range based on boolean criteria.
- 🔹 **`UNIQUE(array)`:** Extracts a deduplicated list of unique values from a column.
- 🔹 **`SORT(array, [sort_index], [sort_order])`:** Sorts a range by a specified column index.
- 🔹 **Spill Range (`#`):** Reference spilled array ranges dynamically (e.g., `A2#`).
- 🔹 **Industry Application:** Building dynamic automated executive summary lists without Pivot Tables.

💻 **Formula Example with Explanation Comments:**
```excel
=SORT(FILTER(A2:D100, B2:B100="Mumbai"), 4, -1)
' Explanation:
' FILTER(A2:D100, B2:B100="Mumbai"): Filters sales rows where City is Mumbai
' SORT(..., 4, -1): Sorts the filtered results by column 4 (Sales Amount) in descending order (-1)
```

---

# Phase 2: SQL for Data Analytics (Days 7 – 12)

## Topic 2.1: Data Querying & Filtering (`SELECT`, `WHERE`, `ORDER BY`)

📌 **Definition:**
**SQL (Structured Query Language)** is used to extract, filter, and sort tabular data stored inside relational database tables.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **`SELECT`:** Specifies which table columns to fetch in the output.
- 🔹 **`WHERE`:** Filters individual rows based on conditional logic before grouping.
- 🔹 **`ORDER BY`:** Sorts output rows in ascending (`ASC`) or descending (`DESC`) order.
- 🔹 **`LIMIT`:** Restricts the number of returned records.
- 🔹 **Industry Application:** Extracting top 10 customer orders in Mumbai with sales > ₹2,000.

💻 **Code Example with Explanation Comments:**
```sql
-- Query top 5 highest value orders from Mumbai
SELECT Order_ID, Customer_ID, Category, (Quantity * Unit_Price) AS Total_Sales
FROM orders
WHERE City = 'Mumbai' AND Rating >= 4.0   -- Filter for Mumbai with high rating
ORDER BY Total_Sales DESC                 -- Sort highest sales first
LIMIT 5;                                  -- Fetch top 5 rows only
```

---

## Topic 2.2: Conditional Branching (`CASE WHEN`)

📌 **Definition:**
`CASE WHEN` evaluates conditional logic inside SQL queries to return customized column values.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Implements `if-then-else` logic directly inside SQL query results.
- 🔹 **Syntax:** `CASE WHEN condition THEN result ELSE fallback END`.
- 🔹 **Binning Data:** Groups continuous numbers into categorical buckets (e.g., High, Medium, Low).
- 🔹 **Aggregation Support:** Can be wrapped inside aggregate functions `SUM(CASE WHEN ... THEN 1 ELSE 0 END)`.
- 🔹 **Industry Application:** Categorizing customer spend into VIP vs Regular tiers.

💻 **Code Example with Explanation Comments:**
```sql
-- Bin orders into value tiers using CASE WHEN
SELECT Order_ID, (Quantity * Unit_Price) AS Total_Sales,
       CASE 
           WHEN (Quantity * Unit_Price) >= 3000 THEN 'High Value Order'
           WHEN (Quantity * Unit_Price) >= 1500 THEN 'Medium Value Order'
           ELSE 'Low Value Order'
       END AS Order_Tier
FROM orders;
```

---

## Topic 2.3: SQL Window Functions (`DENSE_RANK()`, `LAG()`)

📌 **Definition:**
A **Window Function** performs calculations across a set of table rows related to the current row without collapsing individual rows.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Ranks records, calculates running totals, or computes moving averages while preserving row detail.
- 🔹 **`OVER (PARTITION BY ... ORDER BY ...)`:** Defines the window partition group and sorting order.
- 🔹 **`DENSE_RANK()`:** Assigns rank numbers without skipping rank numbers in case of ties.
- 🔹 **`LAG(column, offset)`:** Fetches values from previous rows within the partition.
- 🔹 **Industry Application:** Computing Month-over-Month (MoM) revenue growth percentages.

💻 **Code Example with Explanation Comments:**
```sql
-- Rank products by sales within each city partition
SELECT Order_ID, City, Product, (Quantity * Unit_Price) AS Total_Sales,
       DENSE_RANK() OVER (PARTITION BY City ORDER BY (Quantity * Unit_Price) DESC) AS City_Rank
FROM orders;
```

---

# Phase 3: Python & NumPy Fundamentals (Days 13 – 18)

## Topic 3.1: Variables & Memory Assignment

📌 **Definition:**
A **Variable** is a named reference pointing to a computer memory location where data (numbers, text, tables) is stored.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Holds raw values temporarily while analytical scripts run.
- 🔹 **Analogy:** Like labeled kitchen containers—the label is the variable name, and the item inside is the value.
- 🔹 **Naming Rules:** Must start with a letter or underscore (`_`); spaces and special characters are forbidden.
- 🔹 **Common Mistake:** Using Python reserved keywords (like `for`, `if`, `class`, `import`) causes syntax errors.
- 🔹 **Industry Standard:** Use snake_case (`customer_spend`, `total_revenue`) for clean, readable code.

💻 **Code Example with Explanation Comments:**
```python
# Storing Amazon customer transaction variables
customer_id = "CUST-9872"       # String variable for customer ID
order_amount = 2499.50          # Float variable for purchase value
items_count = 3                 # Integer variable for items count
is_prime_member = True          # Boolean variable for subscription

# Compute final bill
delivery_fee = 0 if is_prime_member else 80
final_bill = order_amount + delivery_fee

print(f"Customer ID: {customer_id}")
print(f"Total Payable: ₹{final_bill}")
```

---

## Topic 3.2: NumPy Array Vectorization & Z-Score Outlier Detection

📌 **Definition:**
**Vectorization** executes mathematical operations on entire numerical arrays simultaneously without writing `for` loops. The **Z-Score** measures how many standard deviations a data point lies from the mean.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Vectorization Advantage:** Replaces slow Python loops with C-speed contiguous memory operations ($100\times$ faster).
- 🔹 **Broadcasting:** Automatically aligns array dimensions during arithmetic operations.
- 🔹 **Z-Score Formula:** $Z = \frac{X - \mu}{\sigma}$ (where $\mu$ is mean, $\sigma$ is standard deviation).
- 🔹 **Outlier Threshold:** $|Z| > 3$ flags data points that lie beyond 3 standard deviations.
- 🔹 **Industry Application:** Identifying abnormal credit card transaction fraud spikes.

💻 **Code Example with Explanation Comments:**
```python
import numpy as np

# Transaction values with 1 extreme outlier (95,000)
data = np.array([450, 500, 480, 520, 510, 490, 530, 470, 95000])

# Calculate Mean and Standard Deviation
mean_val = np.mean(data)
std_val = np.std(data)

# Compute Z-Scores
z_scores = (data - mean_val) / std_val

# Flag outliers (|Z| > 2 for small samples)
outliers = data[np.abs(z_scores) > 2]
print("Mean:", mean_val, "Std:", std_val)
print("Flagged Z-Score Outliers:", outliers)
```

---

# Phase 4: Pandas Wrangling & Visualization (Days 19 – 24)

## Topic 4.1: Data Cleaning (`isna()`, `fillna()`, Winsorizing)

📌 **Definition:**
**Data Cleaning** involves detecting, imputing, or capping (`Winsorizing`) anomalous values to ensure accurate analytical reporting.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **`isna().sum()`:** Counts total missing values in each column of a DataFrame.
- 🔹 **`fillna(value)`:** Replaces missing values with static constants, column means, or medians.
- 🔹 **`dropna()`:** Drops rows or columns containing missing values.
- 🔹 **Winsorizing:** Capping extreme outliers at upper/lower percentile limits instead of deleting rows.
- 🔹 **Common Mistake:** Blindly dropping rows (`dropna()`) reduces sample size and introduces statistical bias.

💻 **Code Example with Explanation Comments:**
```python
import pandas as pd
import numpy as np

# Sample dirty customer CRM DataFrame
data = {
    "Customer_ID": ["C101", "C102", "C103", "C104"],
    "Age": [28, np.nan, 35, 22],
    "Spend": [4500.0, 12000.0, np.nan, 3100.0]
}
df = pd.DataFrame(data)

# Impute missing Age with Median Age
median_age = df["Age"].median()
df["Age"] = df["Age"].fillna(median_age)

# Impute missing Spend with Mean Spend
mean_spend = df["Spend"].mean()
df["Spend"] = df["Spend"].fillna(mean_spend)

print(df)
```

---

# Phase 5: Power BI & Capstone Projects (Days 25 – 30)

## Topic 5.1: Power BI Data Modeling & DAX Time Intelligence

📌 **Definition:**
**DAX Time Intelligence** functions evaluate calculations across specified date periods (YTD, QTD, YoY comparison).

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Prerequisite:** Requires a dedicated, contiguous Date Table marked as a Date Table.
- 🔹 **`TOTALYTD(measure, dates)`:** Calculates cumulative year-to-date total metrics.
- 🔹 **`SAMEPERIODLASTYEAR(dates)`:** Returns dates shifted 1 year back for YoY comparisons.
- 🔹 **Filter Context:** Automatically respects active report slicers and visual filters.
- 🔹 **Industry Application:** Executive dashboard metrics comparing 2024 YTD revenue against 2023 YTD revenue.

💻 **Formula Example with Explanation Comments:**
```dax
-- DAX Measure: Total Sales Revenue
Total_Revenue = SUM(Sales[Quantity]) * SUM(Sales[Unit_Price])

-- DAX Time Intelligence Measure: Same Period Last Year Revenue
Revenue_SPLY = 
CALCULATE(
    [Total_Revenue],
    SAMEPERIODLASTYEAR(DimDate[Date])
)
```
