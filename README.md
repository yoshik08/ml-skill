# Heart Disease — Decision Tree Classification

Single decision tree (max_depth=4) on the UCI Cleveland heart disease dataset.

## Pipeline
1. Load `csv/heart.csv` (303 rows, 13 features, binary target)
2. Median imputation for missing values (`ca`, `thal`)
3. 80/20 stratified train/test split
4. `DecisionTreeClassifier(max_depth=4)`

## Results
See `output/metrics.txt`. Tree visualization in `output/tree.png`.

## Run
```
python3 code/decision_tree.py
```
