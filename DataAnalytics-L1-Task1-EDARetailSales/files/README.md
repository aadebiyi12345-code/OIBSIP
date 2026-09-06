# Task 1 — EDA on Retail Sales Data

**Track:** Data Analytics | **Level:** 1 | **Task:** 1
**Internship:** Oasis Infobyte Summer Internship Program (OIBSIP)

## Objective
Perform a thorough Exploratory Data Analysis on a retail sales dataset to uncover patterns, customer behaviour trends, and actionable business insights.

## Dataset
[Retail Sales Dataset](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset) from Kaggle — 1,000 transactions with the following columns:

| Column | Description |
|---|---|
| Transaction ID | Unique ID per transaction |
| Date | Date of transaction |
| Customer ID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| Product Category | Clothing / Electronics / Beauty |
| Quantity | Units purchased |
| Price per Unit | Price per single unit |
| Total Amount | Total transaction value |

## Tech Stack
Python, pandas, matplotlib, seaborn, Jupyter Notebook

## What's in this notebook
1. Initial inspection (shape, dtypes, nulls, duplicates)
2. Descriptive statistics (mean, median, mode, std)
3. Time series analysis — monthly & quarterly sales trends
4. Customer demographics — age group distribution & gender breakdown
5. Product/category analysis — revenue by category, top 10 customers by spend
6. Correlation heatmap of numerical variables
7. Additional insight — sales by day of the week
8. Conclusion with 4 actionable business recommendations

## Data Limitation
This dataset provides category-level detail (3 broad categories) rather than individual product names, so a literal "top 10 best-selling products" ranking wasn't possible. Revenue-by-category and a top-10-customers-by-spend view were used as the closest available substitutes, with this limitation flagged directly in the notebook.

## Key Findings
- Revenue and unit volume don't move together across all categories — informs pricing vs. stocking strategy
- Neither age nor gender shows a strong correlation with spend — supports broad rather than narrowly-targeted campaigns
- Sales vary by day of week and by quarter — useful for timing promotions
- A small group of top customers accounts for a disproportionate share of revenue — candidates for a loyalty program

## How to Run
1. Clone this repo
2. `pip install pandas numpy matplotlib seaborn`
3. Open `EDA_Retail_Sales.ipynb` in Jupyter Notebook / JupyterLab / VS Code
4. Run all cells
