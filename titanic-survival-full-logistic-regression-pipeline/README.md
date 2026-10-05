# 5. Titanic Survival — Full Logistic Regression Pipeline

End-to-end binary classification: preprocessing + logistic regression in one
script, trained and evaluated on a stratified 80/20 split.

## Run
```
python3 code/logistic_regression.py
```

## Results (test set, n=179)
- accuracy: 0.8156
- precision: 0.8103
- recall: 0.6812
- f1: 0.7402
- ROC-AUC: 0.8506

## Contents
- `csv/titanic.csv` — raw dataset
- `code/logistic_regression.py` — full pipeline (preprocessing inline +
  `LogisticRegression(max_iter=1000)`)
- `output/metrics.txt` — all metrics
- `output/confusion_matrix.png`, `output/roc_curve.png` — evaluation plots
- `output/logistic_model.joblib` — fitted end-to-end model
