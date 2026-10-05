# Heart Disease — Boosting and Interpretability

Compares gradient boosting vs random forest on the UCI Cleveland heart disease dataset,
with permutation importance for model interpretability.

## Fallback note
`xgboost`, `lightgbm`, and `shap` could not be installed in this environment
(disk full during pip install), so sklearn's `GradientBoostingClassifier` is used
as the boosting model and **permutation importance** replaces SHAP. On a machine
with those libraries, swap in `XGBClassifier` / `LGBMClassifier` and `shap.TreeExplainer`
for a true SHAP beeswarm plot.

## Pipeline
1. Load `csv/heart.csv`, median imputation, 80/20 stratified split
2. Train GradientBoosting vs RandomForest, compare accuracy + ROC-AUC
3. Permutation importance (10 repeats) on the better model

## Results
See `output/metrics.txt`. Plot: `output/permutation_importance.png`.

## Run
```
python3 code/boosting_shap.py
```
