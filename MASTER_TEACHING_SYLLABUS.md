# 📘 Master Data Analytics Teaching Syllabus (Zero-to-Hero Guide)

> **Course Philosophy:** Built for absolute beginners and non-programmers. Every single topic is structured into 3 clear parts:
> 1. 📌 **Definition:** Beginner-friendly explanation in simple English.
> 2. 📖 **Key Theory (5 Short Bullet Points):** Purpose, Analogy, Syntax, Pitfalls, and Business Application.
> 3. 💻 **Code / Formula Example with Explanation Comments:** Production code/formulas with line-by-line comments.

---

# Phase 1: Advanced Excel for Data Analytics (Days 1 – 6)

## Topic 1.1: Cell Referencing (Relative vs Absolute `$A$1`)

📌 **Definition:**
**Cell Referencing** tells Excel which cell address to read data from when copying formulas across rows or columns.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Controls whether cell coordinates change or stay locked when dragging formulas.
- 🔹 **Relative Referencing (`A1`):** Cell coordinates automatically change when copied down rows (e.g., `A1` becomes `A2`).
- 🔹 **Absolute Referencing (`$A$1`):** Inserting dollar signs (`$`) locks the column and row so the cell reference never changes.
- 🔹 **Analogy:** Absolute referencing is like anchoring a boat—no matter where you move the rope, the boat stays anchored to one spot.
- 🔹 **Industry Application:** Used in financial spreadsheets to apply a static tax rate (e.g., GST in `$B$1`) across thousands of sales rows.

💻 **Formula Example with Explanation Comments:**
```excel
=B2 * $B$1
' Explanation:
' B2 is Relative: multiplies current row product price
' $B$1 is Absolute: locks static 18% GST rate stored in cell B1
```

---

## Topic 1.2: Modern Lookup Formulas (`XLOOKUP` vs `VLOOKUP`)

📌 **Definition:**
**`XLOOKUP`** searches a row or column for a value and returns a matching value from another row or column.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Merges data from separate tables without copying and pasting manually.
- 🔹 **Syntax:** `=XLOOKUP(lookup_val, lookup_range, return_range, [if_not_found])`.
- 🔹 **Advantage over `VLOOKUP`:** Can lookup values to the left or right, and doesn't break if columns are inserted.
- 🔹 **Default Match:** Performs an exact match by default (unlike `VLOOKUP` which required specifying `FALSE`).
- 🔹 **Industry Application:** Looking up customer names and prices from a Master Catalog into daily sales orders.

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

# Phase 2: SQL for Data Analytics (Days 7 – 12)

## Topic 2.1: Data Querying & Filtering (`SELECT`, `WHERE`, `ORDER BY`)

📌 **Definition:**
**SQL (Structured Query Language)** is used to extract, filter, and sort tabular data stored inside relational database tables.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **`SELECT`:** Specifies which table columns to fetch in the output.
- 🔹 **`WHERE`:** Filters individual rows based on conditional logic before grouping.
- 🔹 **`ORDER BY`:** Sorts output rows in ascending (`ASC`) or descending (`DESC`) order.
- 🔹 **`LIMIT`:** Restricts the number of returned records (useful for previewing large database tables).
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

## Topic 2.2: SQL Window Functions (`DENSE_RANK()`)

📌 **Definition:**
A **Window Function** performs calculations across a set of table rows related to the current row without collapsing them into a single summary row.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Ranks records, calculates running totals, or computes moving averages while preserving row detail.
- 🔹 **`OVER (PARTITION BY ... ORDER BY ...)`:** Defines the window partition group and sorting order.
- 🔹 **`DENSE_RANK()`:** Assigns rank numbers without skipping rank numbers in case of ties.
- 🔹 **Difference from `GROUP BY`:** `GROUP BY` collapses multiple rows into 1 summary row; Window functions keep all original rows intact.
- 🔹 **Industry Application:** Ranking top sales representatives or top revenue products per city.

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

## Topic 3.2: NumPy Array Vectorization vs Python Loops

📌 **Definition:**
**Vectorization** is executing mathematical operations on entire data arrays simultaneously without writing explicit `for` loops.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Replaces slow Python loops with C-speed optimized contiguous memory arrays.
- 🔹 **Speed Advantage:** Executes up to $100\times$ faster than standard Python list loops.
- 🔹 **Homogeneous Data:** All elements in a NumPy array must be of the same data type (`int64`, `float64`).
- 🔹 **Broadcasting:** Automatically aligns array dimensions during arithmetic operations.
- 🔹 **Industry Impact:** Underpins all modern Data Science & Machine Learning libraries (Pandas, Scikit-learn).

💻 **Code Example with Explanation Comments:**
```python
import numpy as np

# Portfolio stock prices stored as a 1D NumPy Array
stock_prices = np.array([120.50, 450.00, 890.25, 1250.00, 310.75])

# Vectorized Operation: Apply 5% brokerage fee adjustment across all stocks instantly
adjusted_prices = stock_prices * 1.05

print("Original Prices:", stock_prices)
print("Adjusted Prices (+5% Fee):", np.round(adjusted_prices, 2))
```

---

# Phase 4: Pandas Wrangling & Visualization (Days 19 – 24)

## Topic 4.1: Data Cleaning (`isna()`, `fillna()`, `dropna()`)

📌 **Definition:**
**Data Cleaning** involves detecting, imputing, or removing missing (`NaN`) values to ensure accurate analytical reporting.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **`isna().sum()`:** Counts total missing values in each column of a DataFrame.
- 🔹 **`fillna(value)`:** Replaces missing values with static constants, column means, or medians.
- 🔹 **`dropna()`:** Drops rows or columns containing missing values.
- 🔹 **Imputation Strategy:** Use Median for numerical data and Mode for categorical text columns.
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

## Topic 5.1: Power BI Data Modeling & DAX Measures

📌 **Definition:**
**DAX (Data Analysis Expressions)** is the formula language used in Power BI to create custom calculated columns and dynamic measures.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Calculated Columns:** Evaluate row-by-row during data refresh and consume RAM storage.
- 🔹 **Measures:** Evaluate dynamically on the fly based on report slicer filters (does not consume disk RAM).
- 🔹 **`CALCULATE()` Function:** Modifies the filter context of a measure calculation.
- 🔹 **Star Schema:** Organization of Fact Tables (metrics) surrounded by Dimension Tables (attributes).
- 🔹 **Industry Application:** Calculating Year-over-Year (YoY) revenue growth and active customer counts.

💻 **Formula Example with Explanation Comments:**
```dax
-- DAX Measure: Total Sales Revenue
Total_Revenue = SUM(Sales[Quantity]) * SUM(Sales[Unit_Price])

-- DAX Measure: High Value Sales (Orders > 2000)
High_Value_Revenue = 
CALCULATE(
    [Total_Revenue],
    Sales[Unit_Price] >= 2000
)
```
