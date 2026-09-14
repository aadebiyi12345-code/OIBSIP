# Level 2 Task 1 — Predicting House Prices with Linear Regression

**Track:** Data Analytics | **Level:** 2 | **Task:** 1
**Internship:** Oasis Infobyte Summer Internship Program (OIBSIP)

## Objective
Build and evaluate a linear regression model that predicts house prices based on features such as area, location, number of rooms, and amenities. Develop end-to-end skills from data cleaning through to model interpretation.

## Dataset
[Housing Prices Dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset) (Kaggle) — 545 house sale records: area, bedrooms, bathrooms, stories, amenities (mainroad, guestroom, basement, hot water heating, air conditioning, parking, preferred area), furnishing status, and sale price.

## Tech Stack
Python, pandas, scikit-learn, matplotlib, seaborn, Jupyter Notebook

## What's in this notebook
1. EDA — null check, descriptive statistics, price distribution
2. Feature selection discussion — reasoning behind which features should predict price
3. Categorical encoding — binary mapping for yes/no columns, one-hot encoding for `furnishingstatus`
4. Correlation heatmap
5. Train/test split (80/20)
6. Linear Regression model training
7. Evaluation — MSE, RMSE, R² score
8. Actual vs. predicted scatter plot
9. Residual plot
10. Coefficient analysis — which features push price up/down
11. Bonus: Ridge & Lasso regression comparison

## Key Findings
- `area` is the strongest single predictor of price
- Model diagnostics (residual plot) reveal whether errors grow at the high end of the price range, consistent with the right-skewed price distribution
- Coefficient analysis identifies which amenities meaningfully affect price vs. which contribute little
- Ridge/Lasso comparison checks whether regularisation improves on plain linear regression for this dataset

## How to Run
1. Clone this repo
2. `pip install pandas numpy matplotlib seaborn scikit-learn`
3. Open `House_Price_Prediction.ipynb` in Jupyter Notebook / JupyterLab / VS Code
4. Run all cells
