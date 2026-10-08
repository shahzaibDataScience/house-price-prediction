# 🏠 House Price Prediction

Predict house prices from area, bedrooms, bathrooms, location, and age — comparing **Linear Regression** vs **Random Forest**.

## What you'll learn

- **Regression basics**: predicting a continuous number (price) instead of a category
- **EDA for regression**: scatter plots, boxplots, and reading relationships between features and price
- **One-hot encoding**: turning text categories (like Location) into numbers models can use
- **Train/test split**: why we test on data the model has never seen
- **MAE, RMSE, R²**: how to measure regression error and explained variance
- **Residual plots**: checking where and how a model goes wrong
- **Feature importance**: which inputs drive the model's decisions

## Dataset

`data/housing.csv` — 5,000 synthetic houses with 6 columns:

| Column | Description |
|---|---|
| Area_sqft | House area, 500–4000 sq ft |
| Bedrooms | 1–5 |
| Bathrooms | 1–4 |
| Location | Downtown / Suburb / Rural |
| Age_years | 0–30 years |
| Price | Target — built from a linear formula + noise |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook house_price_prediction.ipynb
```

Run all cells top to bottom.

## Key findings

- **Area** is the dominant price driver; location adds a clear premium (Downtown > Suburb > Rural).
- **LinearRegression** wins on this data (MAE ≈ $23.9k, RMSE ≈ $29.5k, **R² = 0.969**) — the underlying formula is linear, so the straight-line model fits best.
- **RandomForest** is close behind (R² = 0.953).
- Residuals scatter randomly around zero → no systematic bias.

## 🎓 Explain it yourself

1. What is the difference between regression and classification? Which one is this project?
2. Why do we split data into train and test sets? What goes wrong if we test on training data?
3. In one sentence: what does R² = 0.97 tell you about this model?
4. Why did one-hot encoding get applied to Location but not to Bedrooms?
5. The residual plot shows residuals scattered around zero — why is that a good sign?
