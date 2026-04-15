# House Prices Prediction Project

This project is an end-to-end regression study based on the Kaggle **House Prices: Advanced Regression Techniques** dataset.  
The goal is to predict house sale prices using data preprocessing, feature engineering, and model comparison.

## Project Summary

In this project, missing values were handled with feature-specific logic, important outliers were removed, and new variables such as `TotalSF`, `TotalBath`, `HouseAge`, and `RemodAge` were created.  
Since the target variable `SalePrice` was highly skewed, a `log1p` transformation was applied before modeling.

Categorical variables were encoded with one-hot encoding, and multiple models were tested, including:

- Linear Regression
- Ridge Regression
- Lasso
- ElasticNet
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM

## Final Result

Among all evaluated models, **Ridge Regression (`alpha=10`)** achieved the best performance.

- **Linear Regression RMSE:** 0.1214
- **Ridge RMSE:** 0.1164
- **Ridge CV RMSE Mean:** 0.1149

## Conclusion

This project demonstrates a complete machine learning workflow for a structured regression problem.  
It highlights the importance of careful preprocessing, feature engineering, and model evaluation in improving model performance.

## Project Structure

```bash
house-prices-prediction/
│
├── data/
├── notebooks/
├── outputs/
├── README.md
├── requirements.txt
└── .gitignore