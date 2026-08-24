# 📊 Phase 1 Lesson 2: XLOOKUP, Pivot Tables & Power Query Guide

[![Open in Google Sheets](https://img.shields.io/badge/Open_in-Google_Sheets-green.svg)](https://github.com/SahilShaikh-py/Data_Analytic_/blob/main/datasets/e_commerce_sales.csv)

Welcome to Phase 1 Lesson 2! In this guide, you will master **`XLOOKUP`**, **Pivot Tables**, and **Power Query** in Excel and Google Sheets.

---

## 📌 Topic 2.1: Modern Lookup with `XLOOKUP`

📌 **Definition:**
`XLOOKUP` searches a lookup column for a value and returns a corresponding result from another column.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Purpose:** Merges data across separate sheets without copying and pasting manually.
- 🔹 **Syntax:** `=XLOOKUP(lookup_val, lookup_range, return_range, [if_not_found])`.
- 🔹 **Left & Right Lookup:** Unlike `VLOOKUP`, `XLOOKUP` can look to the left or right seamlessly.
- 🔹 **Exact Match Default:** Automatically performs exact matching without specifying `FALSE`.
- 🔹 **Industry Application:** Fetching product prices and customer addresses into transaction tables.

💻 **Formula Example:**
```excel
=XLOOKUP(A2, Products[Product_ID], Products[Unit_Price], "Not Found")
```

---

## 📌 Topic 2.2: Summarization with Pivot Tables

📌 **Definition:**
A **Pivot Table** is an interactive reporting tool that instantly aggregates, filters, and summarizes large raw datasets.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **4 Core Zones:** Filters, Columns, Rows, Values.
- 🔹 **Grouping:** Dates can be auto-grouped into Months, Quarters, and Years.
- 🔹 **Calculated Fields:** Allows inserting custom formulas directly inside Pivot Tables.
- 🔹 **Slicers:** Visual buttons for filtering reports with a single click.
- 🔹 **Industry Application:** Building dynamic monthly sales summary dashboards for executives.

---

## 📝 Live Student Practice Exercises

1. **Exercise 1:** Use `XLOOKUP` to fetch product unit prices from a master catalog table into your order transactions sheet.
2. **Exercise 2:** Create a Pivot Table showing total revenue and average customer rating by City, and add a Slicer for Category.
