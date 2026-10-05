# ML SKILL

11 hands-on machine learning projects — EDA, preprocessing, regression, classification, ensembles, and interpretability. Each project is self-contained with its dataset, code, and outputs.

## Projects

| # | Project |
|---|---------|
| 1 | [Titanic Survival — EDA and ML Lifecycle Mapping](titanic-survival-eda-and-ml-lifecycle-mapping/) |
| 2 | [Titanic Survival — Preprocessing Pipeline and Cleaned Dataset](titanic-survival-preprocessing-pipeline-and-cleaned-dataset/) |
| 3 | [Adult Income — Feature Engineering and EDA](adult-income-feature-engineering-and-eda/) |
| 4 | [California Housing — Linear Regression and Regularisation](california-housing-linear-regression-and-regularisation/) |
| 5 | [Titanic Survival — Full Logistic Regression Pipeline](titanic-survival-full-logistic-regression-pipeline/) |
| 6 | [Diabetes Severity — Multinomial Logistic Regression](diabetes-severity-multinomial-logistic-regression/) |
| 7 | [Auto MPG — Linear Regression, Feature Scaling, and Encoding](auto-mpg-linear-regression-feature-scaling-and-encoding/) |
| 8 | [Heart Disease — Decision Tree Classification](heart-disease-decision-tree-classification/) |
| 9 | [Heart Disease — Random Forest Ensemble](heart-disease-random-forest-ensemble/) |
| 10 | [Heart Disease — XGBoost, LightGBM, and SHAP Interpretability](heart-disease-xgboost-lightgbm-and-shap-interpretability/) |
| 11 | [Wine Quality — Decision Tree and Random Forest Classification](wine-quality-decision-tree-and-random-forest-classification/) |

## Layout

Each project folder has:

```
<project>/
├── csv/        # dataset
├── code/       # python scripts
├── output/     # plots, metrics, cleaned data
└── README.md
```

## Run

```bash
pip install pandas scikit-learn matplotlib seaborn joblib
cd <project>/code
python <script>.py
```

## Notes

- Project 10 falls back to sklearn's `GradientBoostingClassifier` + permutation importance (xgboost/lightgbm/shap unavailable in the build environment).
