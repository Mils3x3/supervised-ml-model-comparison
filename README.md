# Supervised ML Model Comparison

A machine learning portfolio project focused on structured supervised model comparison.

The current public version contains the completed **Regression Model Comparison** project, which compares a wide range of supervised regression models for predicting diamond prices. A **Binary Classification** project is planned as a future extension and will be added after the regression project is fully finalised.

---

## Current Project Status

| Project | Status |
|---|---|
| Regression Model Comparison | Completed |
| Binary Classification Model Comparison | Planned / not included yet |

---

## Project Purpose

The main goal of this repository is not only to find a single best-performing model, but to compare many supervised machine learning algorithms in a consistent, practical, and reproducible way.

The regression project demonstrates:

- End-to-end supervised machine learning workflow
- Data preprocessing with scikit-learn pipelines
- Baseline model training
- Hyperparameter tuning
- Cross-validation
- Final test-set evaluation
- Practical model comparison
- Prediction and error analysis
- Feature / permutation importance
- Exported HTML report
- Portfolio-ready visual summaries and result tables

---

## Repository Structure

```text
ml-supervised-model-comparison/
├── .gitattributes
├── .gitignore
├── COPYRIGHT.md
├── README.md
├── requirements.txt
├── environment.yml
│
└── regression/
    ├── README.md
    │
    ├── notebooks/
    │   └── supervised_regression_model_comparison.ipynb
    │
    ├── reports/
    │   └── supervised_regression_model_comparison.html
    │
    ├── images/
    │   ├── supervised_regression_model_comparison.png
    │   ├── supervised_regression_tuned_model_comparison_table.png
    │   ├── supervised_regression_practical_comparison_table.png
    │   ├── supervised_regression_selected_test_sample_predictions.png
    │   ├── supervised_regression_prediction_range_difference_summary.png
    │   ├── supervised_regression_best_model_performance_by_price_range.png
    │   ├── supervised_regression_actual_vs_predicted_best_model.png
    │   ├── supervised_regression_actual_vs_predicted_all_models.png
    │   ├── supervised_regression_actual_vs_predicted_distributions_by_model_group.png
    │   ├── supervised_regression_residuals_best_model.png
    │   ├── supervised_regression_residuals_all_models.png
    │   ├── supervised_regression_error_distribution_best_model.png
    │   ├── supervised_regression_error_distribution_all_models.png
    │   └── supervised_regression_permutation_importance.png
    │
    └── results/
        ├── supervised_regression_tuned_model_comparison_table.csv
        ├── supervised_regression_practical_comparison.csv
        ├── supervised_regression_selected_test_sample_predictions.csv
        ├── supervised_regression_prediction_range_difference_summary.csv
        └── supervised_regression_best_model_performance_by_price_range.csv
```

---

## Regression Model Comparison

The regression project compares a wide range of supervised regression models for predicting diamond prices.

### Target Variable

```text
price
```

### Main Evaluation Metrics

- MAE
- MSE
- RMSE
- R² Score

### Main Notebook

[supervised_regression_model_comparison.ipynb](regression/notebooks/supervised_regression_model_comparison.ipynb)

### HTML Report

[supervised_regression_model_comparison.html](regression/reports/supervised_regression_model_comparison.html)

### Detailed Regression README

[Open the Regression Project README](regression/README.md)

---

## Example Visual Summaries

### Tuned Regression Model Comparison

![Tuned Regression Model Comparison](regression/images/supervised_regression_model_comparison.png)

### Practical Comparison of Regression Models

![Practical Comparison of Regression Models](regression/images/supervised_regression_practical_comparison_table.png)

### Actual vs Predicted Values for All Tuned Regression Models

![Actual vs Predicted - All Models](regression/images/supervised_regression_actual_vs_predicted_all_models.png)

### Prediction Error Distributions for All Tuned Regression Models

![Error Distributions - All Models](regression/images/supervised_regression_error_distribution_all_models.png)

### Permutation Importance for the Best Regression Model

![Permutation Importance](regression/images/supervised_regression_permutation_importance.png)

---

## Regression Models Compared

The project compares a broad range of regression model families, including:

- Dummy Regressor
- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Bayesian Ridge
- RANSAC Regressor
- Huber Regressor
- SGD Regressor
- Passive Aggressive Regressor
- Poisson Regressor
- Gamma Regressor
- Quantile Regressor
- Support Vector Regression
- K-Nearest Neighbors Regressor
- Decision Tree Regressor
- Random Forest Regressor
- Extra Trees Regressor
- AdaBoost Regressor
- Gradient Boosting Regressor
- HistGradientBoosting Regressor
- XGBoost Regressor
- LightGBM Regressor
- CatBoost Regressor
- Bagging Regressor
- Voting Regressor
- Stacking Regressor
- MLP Regressor

---

## Machine Learning Workflow

The regression notebook follows this workflow:

1. Load and inspect the dataset
2. Define the target variable
3. Split the data into training and test sets
4. Build preprocessing pipelines
5. Train baseline models
6. Evaluate baseline performance
7. Tune selected models
8. Compare tuned models
9. Evaluate final models on the test set
10. Save selected result tables and visual outputs
11. Analyse prediction behaviour
12. Analyse residuals and error distributions
13. Review practical strengths and weaknesses of the models
14. Interpret permutation importance for the best model

---

## Technologies Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- SciPy
- scikit-learn
- matplotlib
- seaborn
- XGBoost
- LightGBM
- CatBoost
- joblib

---

## How to Run

### Recommended: Conda / Miniforge

The recommended setup is to create the environment from `environment.yml`:

```bash
conda env create -f environment.yml
conda activate supervised-ml-model-comparison
```

Then start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
regression/notebooks/supervised_regression_model_comparison.ipynb
```

Run the notebook from top to bottom.

### Alternative: pip

A `requirements.txt` file is also included as a simpler pip-compatible package list:

```bash
pip install -r requirements.txt
```

The conda environment is recommended because this project uses several machine learning libraries that are often easier to manage through `conda-forge`.

---

## Notes for Reviewers

This repository is designed as a portfolio project.

The notebook shows not only final results, but also the modelling process, tuning logic, practical comparison, prediction analysis, and visual interpretation.

The HTML report is included to make the project easier to review without running the notebook locally.

---

## Planned Extension

A Binary Classification Model Comparison project is planned as a future extension of this repository.

When completed, it will be added under:

```text
binary-classification/
```

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
