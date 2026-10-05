# 1. Titanic Survival — EDA and ML Lifecycle Mapping

Exploratory data analysis of the Titanic passenger dataset (891 rows),
plus a mapping of each finding to an ML lifecycle stage.

## Run
```
python3 code/eda_lifecycle.py
```

## Contents
- `csv/titanic.csv` — raw dataset
- `code/eda_lifecycle.py` — full EDA script (pandas / matplotlib / seaborn)
- `output/` — PNG plots: missing values, survival distribution, survival by
  sex/class, age & fare distributions, age by survival, fare by class,
  correlation heatmap
- `output/lifecycle_mapping.md` — each EDA finding mapped to an ML lifecycle
  stage (problem framing → deployment) with one concrete action per stage

## Key findings
- 38.4% survived; females 74% vs males 19%; 1st class 63% vs 3rd class 24%
- `Age` 20% missing, `Cabin` 77% missing, `Embarked` 2 missing
- Strongest numeric signal is `Pclass` (corr −0.34 with survival)
