# Supervised ML Model Comparison

A structured machine learning portfolio project comparing supervised learning models across two practical tasks:

1. **Regression** – predicting diamond prices
2. **Binary Classification** – predicting whether a diamond belongs to a high-clarity group

The project was created to demonstrate a complete supervised machine learning workflow in Python, including preprocessing, pipelines, baseline models, hyperparameter tuning, cross-validation, final test-set evaluation, model comparison, exported reports, result tables, and practical interpretation.

---

## Project Purpose

The main goal of this repository is not only to find a single best-performing model, but to compare many supervised machine learning algorithms in a consistent, practical, and reproducible way.

This project demonstrates:

- End-to-end supervised machine learning workflows
- Regression and binary classification modelling
- Consistent preprocessing using scikit-learn pipelines
- Model benchmarking across many algorithm families
- Hyperparameter tuning and cross-validation
- Final test-set evaluation
- Practical model comparison
- Exported HTML reports and visual summaries
- Portfolio-ready project documentation

---

## Repository Structure

```text
supervised-ml-model-comparison/
├── README.md
├── COPYRIGHT.md
├── .gitignore
├── requirements.txt
│
├── regression/
│   ├── README.md
│   ├── notebooks/
│   │   └── supervised_regression_model_comparison.ipynb
│   ├── reports/
│   │   └── supervised_regression_model_comparison.html
│   ├── images/
│   │   ├── supervised_regression_model_comparison.png
│   │   ├── supervised_regression_actual_vs_predicted.png
│   │   ├── supervised_regression_residuals.png
│   │   └── supervised_regression_feature_importance.png
│   └── results/
│       ├── supervised_regression_final_results.csv
│       └── supervised_regression_practical_comparison.csv
│
└── binary-classification/
    ├── README.md
    ├── notebooks/
    │   └── supervised_binary_classification_model_comparison.ipynb
    ├── reports/
    │   └── supervised_binary_classification_model_comparison.html
    ├── images/
    │   ├── supervised_binary_classification_model_comparison.png
    │   ├── supervised_binary_classification_confusion_matrix.png
    │   ├── supervised_binary_classification_roc_curve.png
    │   ├── supervised_binary_classification_precision_recall_curve.png
    │   └── supervised_binary_classification_feature_importance.png
    └── results/
        ├── supervised_binary_classification_final_results.csv
        └── supervised_binary_classification_practical_comparison.csv
```

---

## Projects Included

### 1. Regression Model Comparison

The regression project compares a wide range of supervised regression models for predicting diamond prices.

**Main target variable:**

```text
price
```

**Main evaluation metrics:**

- MAE
- MSE
- RMSE
- R² Score

**Project folder:**

[Open Regression Project](regression/README.md)

**Notebook:**

[supervised_regression_model_comparison.ipynb](regression/notebooks/supervised_regression_model_comparison.ipynb)

**HTML report:**

[supervised_regression_model_comparison.html](regression/reports/supervised_regression_model_comparison.html)

---

### 2. Binary Classification Model Comparison

The binary classification project compares supervised classification models for predicting whether a diamond belongs to a high-clarity group.

**Main target variable:**

```text
is_high_clarity
```

**Main evaluation metrics:**

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

**Project folder:**

[Open Binary Classification Project](binary-classification/README.md)

**Notebook:**

[supervised_binary_classification_model_comparison.ipynb](binary-classification/notebooks/supervised_binary_classification_model_comparison.ipynb)

**HTML report:**

[supervised_binary_classification_model_comparison.html](binary-classification/reports/supervised_binary_classification_model_comparison.html)

---

## Example Visual Summaries

### Regression Model Comparison

![Regression Model Comparison](regression/images/supervised_regression_model_comparison.png)

### Binary Classification Model Comparison

![Binary Classification Model Comparison](binary-classification/images/supervised_binary_classification_model_comparison.png)

---

## Machine Learning Workflow

Both projects follow a similar workflow:

1. Load and inspect the dataset
2. Define the target variable
3. Split the data into training and test sets
4. Build preprocessing pipelines
5. Train baseline models
6. Evaluate baseline performance
7. Tune selected models
8. Compare tuned models
9. Evaluate final models on the test set
10. Save result tables and reports
11. Analyse predictions and model behaviour
12. Interpret feature importance where appropriate

---

## Technologies Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn
- XGBoost
- LightGBM
- CatBoost
- joblib

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/supervised-ml-model-comparison.git
```

2. Open the project folder:

```bash
cd supervised-ml-model-comparison
```

3. Create and activate a virtual environment.

4. Install the required packages:

```bash
pip install -r requirements.txt
```

5. Open Jupyter Notebook:

```bash
jupyter notebook
```

6. Run the notebooks from top to bottom.

---

## Notes for Reviewers

This repository is designed as a portfolio project. The notebooks show not only final results, but also the modelling process, comparison logic, and practical reasoning behind model selection.

The HTML reports are included to make the project easier to review without running the notebooks locally.

---

## Author

**Milan Olah**  
Data Science / Machine Learning Portfolio Project

---

## Copyright

© 2026 Milan Olah. All rights reserved.

This project is shared publicly for portfolio and educational demonstration purposes.  
No permission is granted to copy, redistribute, modify, sell, or present this work as your own without written permission.

For details, see [COPYRIGHT.md](COPYRIGHT.md).
