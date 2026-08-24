# Instructor's GitHub, Google Colab and Classroom Guide

This guide explains how to conduct deep 2+ hour live teaching sessions, manage hands-on student labs using Google Colab, evaluate homework submissions, and maintain your course repository on GitHub.

---

## 1. Single-Click Student Access Strategy

To eliminate setup friction for beginner students, all course material is accessible in 1 click:
- **Google Colab Badges:** Every lesson notebook in the curriculum has a single-click **`[Open in Colab]`** badge that opens the live notebook directly in Google Colab.
- **GitHub Target Repository:** All badges point to `https://github.com/SahilShaikh-py/Advanced-Python-Data-Science-`.
- **Sample Datasets:** Datasets are hosted in the [`datasets/`](datasets/) folder and can be loaded directly into Colab via raw GitHub URLs.

---

## 2. Classroom Teaching Formula (2+ Hours Deep Class)

- **Part 1 (Concept, Theory and Intuition):** Teach Definition, Key Features, and Real-World Uses in short bullet points from `MASTER_TEACHING_SYLLABUS.md`.
- **Part 2 (Live Instructor Code-Along):** Demonstrate live code execution cell-by-cell in Google Colab. Explain the line-by-line comments.
- **Part 3 (Student Practice Lab):** Give students dedicated time to complete the hands-on lab exercises at the bottom of the notebook.
- **Part 4 (Q&A and Industry Edge Cases):** Discuss edge cases, hyperparameter tuning tradeoffs, and resolve student doubts.

---

## 3. Student Homework and Submission Workflows

### Option A: Google Drive Shareable Link (Simplest Method)
1. Student opens the lesson notebook in Google Colab via the `[Open in Colab]` link.
2. Clicks **File** -> **Save a copy in Drive**.
3. Completes exercises, clicks **Share** (set to "Anyone with link can view"), and submits their Colab URL.

### Option B: GitHub Fork and Pull Request (Portfolio Building Method)
1. Student clicks **Fork** on `https://github.com/SahilShaikh-py/Advanced-Python-Data-Science-.git`.
2. Completes homework notebooks and commits changes to their personal GitHub repository.
3. Submits their repository link for evaluation.

---

## 4. Daily Git Maintenance Commands

Run these standard terminal commands to push new code, lesson notebooks, or syllabus updates live to GitHub:

```bash
# 1. Stage all new and modified files
git add .

# 2. Commit with descriptive commit message
git commit -m "Update modular course syllabus and lesson notebooks"

# 3. Push live to GitHub main branch
git push origin main
```
