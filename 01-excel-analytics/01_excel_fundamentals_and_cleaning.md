# 📊 Phase 1 Lesson 1: Excel Fundamentals, Referencing & Text Cleaning Guide

[![Open in Google Sheets](https://img.shields.io/badge/Open_in-Google_Sheets-green.svg)](https://github.com/SahilShaikh-py/Data_Analytic_/blob/main/datasets/e_commerce_sales.csv)

Welcome to Phase 1 Lesson 1! In this guide, you will master **Cell Referencing** and **Text Cleaning Formulas** in Excel and Google Sheets.

---

## 📌 Topic 1.1: Cell Referencing (Relative vs Absolute `$A$1`)

📌 **Definition:**
Cell Referencing specifies cell addresses in formulas and controls whether coordinates change or stay locked when formulas are copied across rows/columns.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **Relative Referencing (`A1`):** Cell reference automatically shifts when dragged down or across.
- 🔹 **Absolute Referencing (`$A$1`):** Dollar signs (`$`) lock the row and column coordinates permanently.
- 🔹 **Analogy:** Like anchoring a boat—no matter where you drag the formula, `$A$1` stays anchored to one cell.
- 🔹 **Common Pitfall:** Forgetting `$` signs causes `#REF!` or incorrect tax/discount calculations when copying formulas.
- 🔹 **Industry Application:** Applying static tax rates (e.g., 18% GST in cell `$B$1`) across thousands of product prices.

💻 **Formula Example:**
```excel
=B2 * $B$1
```

---

## 📌 Topic 1.2: Text Cleaning Formulas (`TRIM`, `PROPER`, `CONCAT`)

📌 **Definition:**
Text Cleaning formulas fix messy, unformatted text data (extra spaces, inconsistent lower/upper cases) in spreadsheets.

📖 **Key Theory (5 Short Bullet Points):**
- 🔹 **`TRIM(text)`:** Removes all leading, trailing, and double spaces between words.
- 🔹 **`PROPER(text)`:** Capitalizes the first letter of each word (e.g., `"rahul sharma"` ➔ `"Rahul Sharma"`).
- 🔹 **`UPPER()` / `LOWER()`:** Converts text to ALL CAPS or all lowercase.
- 🔹 **`CONCATENATE(text1, text2)`:** Joins multiple text cells into one unified string.
- 🔹 **Flash Fill (`Ctrl+E`):** Shortcut to auto-detect and transform text patterns instantly.

💻 **Formula Example:**
```excel
=PROPER(TRIM(A2))
```

---

## 📝 Live Student Practice Exercises

1. **Exercise 1:** Open `e_commerce_sales.csv` in Google Sheets. Create a column calculating `Total_Price` including 18% tax using an absolute reference to cell `$K$1`.
2. **Exercise 2:** Use `=PROPER(TRIM(A2))` to clean a column of customer names containing extra spaces.
