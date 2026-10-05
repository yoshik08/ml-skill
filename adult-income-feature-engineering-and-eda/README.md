# 03 — Adult Income: Feature Engineering and EDA

Income prediction dataset (UCI Adult, 1994 US census). Goal: explore what
drives >50K income and engineer useful features.

## structure
- `csv/adult.data` — raw download (no header)
- `csv/adult.csv` — cleaned: header added, whitespace stripped, `?` → NaN, missing rows dropped (30,162 rows)
- `code/fe_eda.py` — full pipeline, run: `python3 code/fe_eda.py`
- `output/` — plots, engineered dataset, report

## EDA
- income is imbalanced: ~75% ≤50K
- >50K rate rises steeply with education (Doctorate/Prof-school highest)
- males have a much higher >50K rate than females in this sample
- >50K earners work more hours/week on average

## feature engineering
- `capital_net` = capital-gain − capital-loss (positive corr with high income)
- `age_bin` — young / adult / middle / senior
- `hours_bin` — part-time / full-time / overtime
- `education_group` — dropout / high-school / college / bachelors / postgrad

## output
- `income_distribution.png`, `income_by_education.png`, `income_by_sex.png`, `hours_by_income.png`
- `adult_engineered.csv` — full dataset with new features
- `eda_report.txt` — numbers + key findings
