# House Prices Prediction

End-to-end regression project predicting house sale prices using the Kaggle House Prices dataset. 8 models tested with hyperparameter tuning.

## Model Results

| Model | RMSE | CV RMSE | R² |
|---|---|---|---|
| Linear Regression | 0.1214 | 0.1243 | 0.898 |
| Lasso | 0.1168 | 0.1153 | 0.906 |
| ElasticNet | 0.1168 | 0.1153 | 0.906 |
| XGBoost (tuned) | 0.1203 | 0.1172 | 0.900 |
| LightGBM (tuned) | 0.1278 | 0.1189 | 0.887 |
| **Ridge (alpha=10)** | **0.1164** | **0.1149** | **0.907** |

## Final Model

**Ridge Regression (alpha=10)** — best performance across all models.

- **RMSE:** 0.1164 — lowest test error
- **CV RMSE:** 0.1149 — best cross-validated generalization
- **R²:** 0.907 — explains 90.7% of variance in house prices

> Despite hyperparameter tuning, Ridge outperformed XGBoost and LightGBM — demonstrating that regularized linear models can beat complex ensembles when preprocessing is done well.

## Feature Engineering
- Created: `TotalSF`, `TotalBath`, `HouseAge`, `RemodAge`
- Log transformation on `SalePrice` (skewed target)
- Outlier removal based on GrLivArea vs SalePrice
- One-hot encoding for categorical variables

## Technologies
- Python, Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn, XGBoost, LightGBM