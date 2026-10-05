# 07 — Auto MPG: Linear Regression, Feature Scaling, and Encoding

Predicts `mpg` from the seaborn mpg dataset with LinearRegression.

## Layout
- `csv/mpg.csv` — 398 rows; horsepower median-imputed, `name` dropped,
  `origin` one-hot encoded (drop_first)
- `code/mpg_regression.py` — compares LinearRegression **without** scaling
  vs **with** StandardScaler (coefficient magnitudes differ, predictions
  identical), reports RMSE / R²
- `output/metrics.txt`
- `output/scaling_comparison.png` — |coefficients| raw vs standardized
- `output/residual_plot.png`

## Run
```
python3 code/mpg_regression.py
```

## Key result
Scaling does not change predictions (max |diff| ≈ 1e-14) or RMSE/R² —
it only rescales the coefficients, which matters for regularised models
and coefficient interpretability.
