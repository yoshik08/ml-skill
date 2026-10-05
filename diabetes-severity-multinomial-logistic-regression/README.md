# 06 — Diabetes Severity: Multinomial Logistic Regression

Buckets the sklearn diabetes regression target into 3 severity classes
(Low / Medium / High by tertiles) and fits a softmax (multinomial)
logistic regression.

## Layout
- `csv/diabetes.csv` — 442 rows; features + `progression` + `severity`
- `code/multinomial_lr.py` — train/test split (stratified, 25% test),
  StandardScaler, LogisticRegression (lbfgs, multinomial)
- `output/metrics.txt` — accuracy + per-class precision/recall/f1
- `output/confusion_matrix.png`
- `output/coefficient_heatmap.png` — coefficients per class × feature

## Run
```
python3 code/multinomial_lr.py
```
