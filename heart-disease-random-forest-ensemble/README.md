# Heart Disease — Random Forest Ensemble

Random forest (200 trees) with out-of-bag evaluation on the UCI Cleveland heart disease dataset.

## Pipeline
1. Load `csv/heart.csv`, median imputation
2. 80/20 stratified train/test split
3. `RandomForestClassifier(n_estimators=200, oob_score=True)`

## Results
See `output/metrics.txt` (accuracy + OOB score).
Plots: `output/feature_importance.png`, `output/confusion_matrix.png`.

## Run
```
python3 code/random_forest.py
```
