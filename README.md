# 2. Titanic Survival — Preprocessing Pipeline and Cleaned Dataset

Reusable sklearn preprocessing pipeline with feature engineering.

## Run
```
python3 code/preprocess.py
```

## Pipeline
`FunctionTransformer` (engineers `FamilySize`, `IsAlone`) →
`ColumnTransformer`:
- numerics (`Age`, `Fare`, `SibSp`, `Parch`, `FamilySize`, `IsAlone`):
  median impute → standard scale
- categoricals (`Pclass`, `Sex`, `Embarked`):
  most-frequent impute → one-hot encode
- drops `Name`, `Ticket`, `Cabin`
- stratified 80/20 train/test split (`random_state=42`)

## Contents
- `csv/titanic.csv` — raw dataset
- `code/preprocess.py` — pipeline script
- `output/titanic_cleaned.csv` — cleaned full dataset (891×11, zero nulls)
- `output/preprocess_pipeline.joblib` — fitted pipeline (reuse in modeling)
- `output/splits.joblib` — train/test splits
- `output/preprocessing_report.txt` — shape/null counts before & after
