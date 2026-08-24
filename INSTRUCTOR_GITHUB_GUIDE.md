# 👨‍🏫 Instructor's GitHub, Google Colab & Sheets Guide

This guide explains how to manage live teaching sessions, conduct hands-on student labs using Google Colab and Google Sheets, handle homework submissions, and update your GitHub course repository.

---

## 📌 1. Single-Click Student Access Strategy

To ensure students face zero setup friction, all course content is accessible in 1 click:
- **Python, SQL & EDA Notebooks:** Single-click **`[Open in Colab]`** badge opens the notebook live in Google Colab.
- **Excel Practice Files:** Single-click **`[Open in Google Sheets]`** badge opens the raw CSV in Google Sheets.
- **Power BI Dashboards:** Single-click **`[View Live Dashboard]`** link opens the embedded Power BI report.

---

## ⏱️ 2. The 3-Hour Daily Classroom Formula

- ⏱️ **Hour 1 (Concept & Business Scenario):** Explain the **Simple English Definition**, **Analogy**, and **5 Short Bullet Points** from `MASTER_TEACHING_SYLLABUS.md`.
- ⏱️ **Hour 2 (Instructor Live Practical Demo):** Share screen and demonstrate live execution of code/formulas cell-by-cell.
- ⏱️ **Hour 3 (Student Practice Lab & Doubts):** Give students 15–20 minutes to complete the 2 practice exercises at the bottom of the lesson notebook.

---

## 📝 3. Student Homework Submission Options

### Option A: Google Drive Shareable Link (Simplest Option)
1. Student opens the notebook in Google Colab.
2. Clicks **File** ➔ **Save a copy in Drive**.
3. Completes homework, clicks **Share** (set to "Anyone with link can view"), and submits the URL to the instructor.

### Option B: GitHub Fork & Pull Request (Portfolio Building)
1. Student clicks **Fork** on `https://github.com/SahilShaikh-py/Data_Analytic_.git`.
2. Completes assignments and commits to their personal repository.
3. Submits their repository URL for evaluation.

---

## 💻 4. Daily Git Maintenance Commands

Run these standard terminal commands to push new code or lesson updates live:

```bash
# 1. Stage all new and modified files
git add .

# 2. Commit with descriptive message
git commit -m "Update Phase 3 Python functions notebook and add solution key"

# 3. Push live to GitHub main branch
git push origin main
```
