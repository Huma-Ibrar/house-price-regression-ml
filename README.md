# House Price Prediction — Regression Model Comparison

A machine learning project that predicts house prices from property features and compares four regression models to identify the best fit for the data.

## 📌 Project Overview

This project uses a house price dataset to

- Explore relationships between features and price
- Train and evaluate four different regression models
- Compare their performance and select the best-performing model
- Save the final model for reuse

## 📊 Dataset

House Price Regression Dataset (Kaggle) — 1000 rows, 8 columns, no missing values.

Features `Square_Footage`, `Num_Bedrooms`, `Num_Bathrooms`, `Year_Built`, `Lot_Size`, `Garage_Size`, `Neighborhood_Quality`
Target `House_Price`

## 🧠 Models Compared

## Model MAE RMSE R² Score

Linear Regression 27,179.53 32,885.95 0.9832
KNN 29,118.66 36,030.89 0.9799
Random Forest 32,452.33 40,851.26 0.9741
Decision Tree 36,676.98 46,488.95 0.9665

## 🔍 Key Finding

`Square_Footage` has a ~0.99 correlation with `House_Price`, and the relationship is clearly linear. Because of this, Linear Regression outperforms the more complex models (Decision Tree, Random Forest) — a reminder that model choice should be driven by the shape of the data, not by complexity or popularity.

## 🛠️ Workflow

1. Exploratory Data Analysis (correlation matrix, heatmap, scatter plot)
2. Train-test split (8020)
3. Feature scaling (for KNN only)
4. Model training and evaluation (MAE, RMSE, R², train-vs-test R² for overfitting checks)
5. Cross-validation (5-fold) to confirm results
6. Model comparison table
7. Final model saved with `joblib`

## 📦 Tech Stack

- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- joblib

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

Open `house_price_regression_professional.ipynb` in Jupyter or VS Code and run all cells in order.

## 📁 Files

- `house_price_regression_professional.ipynb` — full analysis and model comparison notebook
- `house_price_regression_dataset.csv` — dataset used
- `house_price_model.pkl` — saved final model (Linear Regression)
