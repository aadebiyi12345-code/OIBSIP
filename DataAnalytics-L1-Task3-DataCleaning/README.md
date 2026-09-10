# Task 3 — Data Cleaning

**Track:** Data Analytics | **Level:** 1 | **Task:** 3
**Internship:** Oasis Infobyte Summer Internship Program (OIBSIP)

## Objective
Demonstrate professional-level data cleaning skills by taking a deliberately messy dataset and systematically transforming it into a clean, analysis-ready dataset, documenting every decision.

## Dataset
[Dirty Cafe Sales](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training) (Kaggle) — 10,000 cafe transactions, deliberately corrupted with missing values, invalid placeholder strings ("ERROR", "UNKNOWN"), and inconsistent types.

## Tech Stack
Python, pandas, numpy, matplotlib, seaborn, Jupyter Notebook

## What's in this notebook
1. Data quality report — nulls, "ERROR"/"UNKNOWN" placeholder counts, dtype issues (before cleaning)
2. Standardising invalid markers ("ERROR", "UNKNOWN") into true `NaN`
3. Data type correction (numeric columns, date column)
4. Logical missing-value imputation using the Item ↔ Price relationship and the `Total Spent = Quantity × Price` identity
5. Dropping rows with unrecoverable core fields, and rows missing a transaction date (with justification)
6. Filling secondary fields (Payment Method, Location) with `'Unknown'` rather than dropping (with justification)
7. Duplicate removal
8. Outlier detection (IQR method) — reasoning for why flagged points were retained
9. Before vs. after summary table
10. Export of `cleaned_cafe_sales.csv`

## Key Decisions & Justifications
- **"ERROR"/"UNKNOWN" treated as missing, not as valid categories** — they're placeholder junk values, not real data.
- **Logical imputation over statistical guessing** — since Item and Price Per Unit have a fixed 1:1 relationship in this cafe's menu, and `Total Spent = Quantity × Price Per Unit`, many "missing" values could be recovered exactly rather than estimated.
- **Rows dropped only when truly unrecoverable** — core transaction fields (Item/Quantity/Price/Total Spent/Date) with no missing-value recovery path were dropped rather than filled with fabricated values.
- **Secondary fields filled with 'Unknown' instead of dropped** — Payment Method and Location had high missingness (25–33%); dropping would have discarded too much valid sales data, so gaps were labelled explicitly instead.
- **Outliers retained** — the dataset's fixed price/quantity structure means IQR-flagged points are legitimate high-value transactions, not data errors.

## How to Run
1. Clone this repo
2. `pip install pandas numpy matplotlib seaborn`
3. Open `Data_Cleaning.ipynb` in Jupyter Notebook / JupyterLab / VS Code
4. Run all cells
