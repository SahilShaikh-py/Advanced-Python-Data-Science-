# 📊 Phase 5 Lesson 1: Power BI Star Schema, DAX & Live Web Publishing Guide

Welcome to Phase 5! In this guide, you will master **Data Modeling**, **DAX Formulas**, and **Power BI Live Web Publishing**.

---

## 📌 Topic 5.1: Data Modeling (Star Schema)

📌 **Definition:**
A **Star Schema** organizes data into central **Fact Tables** (containing metrics) surrounded by **Dimension Tables** (containing attributes).

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Fact Table:** Stores numerical facts (Sales Amount, Quantities, Taxes).
- 🔹 **Dimension Tables:** Stores descriptive attributes (Customer Name, Product Category, Store Location).
- 🔹 **Relationships:** Connected via 1-to-Many (`1:*`) Primary-Foreign key relationships.
- 🔹 **Performance Advantage:** Faster query execution and cleaner DAX calculation context.
- 🔹 **Industry Application:** Retail sales data modeling in enterprise BI environments.

---

## 📌 Topic 5.2: DAX Formulas (Calculated Columns vs Measures)

📌 **Definition:**
**DAX (Data Analysis Expressions)** is the formula language used in Power BI for dynamic analytics calculations.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Calculated Columns:** Evaluate row-by-row during data refresh and consume RAM storage.
- 🔹 **Measures:** Evaluate dynamically on the fly based on report slicer context.
- 🔹 **`CALCULATE()`:** Overrides or modifies the current filter context of a measure.
- 🔹 **Time Intelligence:** DAX functions (`TOTALYTD`, `SAMEPERIODLASTYEAR`) for period comparisons.
- 🔹 **Industry Application:** Tracking Monthly Recurring Revenue (MRR) and YoY growth.

💻 **DAX Example:**
```dax
Total_Revenue = SUM(Sales[Quantity]) * SUM(Sales[Unit_Price])
```

---

## 🌐 Live Web Publishing (Public Embed Links)

1. Save report in Power BI Desktop.
2. Click **Publish** ➔ Select **My Workspace** on Power BI Service (`app.powerbi.com`).
3. Click **File** ➔ **Embed Report** ➔ **Publish to Web (Public)**.
4. Copy the generated iframe URL and paste into your Markdown portfolio for live interactive viewing!
