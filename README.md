# 04 — California Housing: Linear Regression and Regularisation

Predict median house value from 8 census features (MedInc, HouseAge,
AveRooms, AveBedrms, Population, AveOccup, Latitude, Longitude).

## structure
- `csv/housing.csv` — dataset from `sklearn.datasets.fetch_california_housing` (20,640 rows)
- `code/regularisation.py` — run: `python3 code/regularisation.py`
- `output/` — metrics, plots

## method
- 80/20 train/test split, StandardScaler
- models: LinearRegression vs RidgeCV / LassoCV / ElasticNetCV
  (alpha chosen by 3-fold CV over log-spaced grid)

## results (test set)
| model | rmse | mae | r2 |
|---|---|---|---|
| LinearRegression | 0.7456 | 0.5332 | 0.5758 |
| Ridge (α≈3.16) | 0.7455 | 0.5332 | 0.5759 |
| Lasso (α=0.001) | 0.7446 | 0.5331 | 0.5769 |
| ElasticNet (α=0.001) | 0.7448 | 0.5331 | 0.5767 |

Regularised models edge out plain linear regression; Lasso shrinks the
least-useful coefficients toward zero.

## output
- `metrics.txt` / `metrics.csv` — RMSE, MAE, R², CV-RMSE per model
- `coefficients.png` — coefficient comparison across models
- `predicted_vs_actual.png` — best model (Lasso) predictions vs actuals
