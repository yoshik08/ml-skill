# ML SKILL

11 hands-on machine learning projects — EDA, preprocessing, regression, classification, ensembles, and interpretability. Each project is self-contained with its dataset, code, and outputs.

## Projects

| # | Project | Dataset | Focus |
|---|---------|---------|-------|
| 1 | [Titanic Survival — EDA and ML Lifecycle Mapping](01-titanic-eda-lifecycle/) | Titanic | EDA + mapping findings to ML lifecycle stages |
| 2 | [Titanic Survival — Preprocessing Pipeline](02-titanic-preprocessing/) | Titanic | Cleaning, encoding, scaling, train/test split |
| 3 | [Adult Income — Feature Engineering and EDA](03-adult-income-fe-eda/) | Adult (UCI) | EDA + engineered features |
| 4 | [California Housing — Linear Regression and Regularisation](04-california-housing-regression/) | California Housing | Ridge / Lasso / ElasticNet comparison |
| 5 | [Titanic Survival — Full Logistic Regression Pipeline](05-titanic-logistic-regression/) | Titanic | End-to-end classification pipeline |
| 6 | [Diabetes Severity — Multinomial Logistic Regression](06-diabetes-multinomial-lr/) | Diabetes | 3-class severity prediction |
| 7 | [Auto MPG — Linear Regression, Scaling, and Encoding](07-auto-mpg-regression/) | Auto MPG | Scaling effects + one-hot encoding |
| 8 | [Heart Disease — Decision Tree](08-heart-disease-decision-tree/) | Heart (Cleveland) | Single tree, visualized |
| 9 | [Heart Disease — Random Forest](09-heart-disease-random-forest/) | Heart (Cleveland) | Ensemble + feature importance |
| 10 | [Heart Disease — Boosting and Interpretability](10-heart-disease-xgb-lgbm-shap/) | Heart (Cleveland) | Gradient boosting + permutation importance |
| 11 | [Wine Quality — Decision Tree and Random Forest](11-wine-quality-trees/) | Wine Quality (UCI) | Tree vs forest comparison |

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
