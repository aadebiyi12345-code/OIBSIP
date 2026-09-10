# Task 2 — Customer Segmentation Analysis

**Track:** Data Analytics | **Level:** 1 | **Task:** 2
**Internship:** Oasis Infobyte Summer Internship Program (OIBSIP)

## Objective
Apply clustering algorithms to segment an e-commerce company's customer base into distinct groups based on purchasing behaviour, enabling targeted marketing strategies.

## Dataset
[UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail) — 541,909 invoice-line transactions from a UK-based online retailer, December 2010 to December 2011.

## Tech Stack
Python, pandas, scikit-learn (KMeans), matplotlib, seaborn, Jupyter Notebook

## What's in this notebook
1. Load & inspect the raw dataset
2. Data cleaning — drop missing Customer IDs, remove cancelled orders and invalid prices
3. Descriptive statistics — average purchase value, purchase frequency, customer lifetime value
4. RFM feature engineering (Recency, Frequency, Monetary)
5. Feature scaling with StandardScaler
6. K-Means clustering with the Elbow Method to choose K
7. Cluster visualisation (2 scatter plot feature combinations)
8. Cluster profiling — mean RFM values per cluster, customer type per segment
9. Number of customers per cluster (bar chart)
10. Insights — recommended marketing action per segment

## Key Findings
- Customer spend is heavily right-skewed — a small group of high-value customers pulls the average well above the median
- K=4 clusters (via the Elbow Method) produces cleanly separated, actionable segments
- Segments broadly map to: Champions, Loyal/Regular Customers, At-Risk/Lapsing Customers, and Low-Engagement/One-Time Buyers
- Marketing spend should be allocated proportionally to segment value rather than applied uniformly

## How to Run
1. Clone this repo
2. `pip install pandas numpy matplotlib seaborn scikit-learn openpyxl`
3. Open `Customer_Segmentation.ipynb` in Jupyter Notebook / JupyterLab / VS Code
4. Run all cells
