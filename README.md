# Supervised Machine Learning Model Comparison

A machine learning portfolio repository focused on structured supervised model comparison on tabular data.

This repository contains two completed supervised learning projects using the `diamonds` dataset:

- **Regression Model Comparison** – predicting diamond prices
- **Binary Classification Model Comparison** – predicting whether a diamond belongs to a higher-clarity group

Both projects compare a wide range of supervised machine learning models using consistent preprocessing, training, tuning, evaluation, export, and practical model selection workflows.

---

## Current Project Status

| Project | Type | Status | Detailed README |
|---|---|---|---|
| Regression Model Comparison | Supervised Regression | Completed | [regression/README.md](regression/README.md) |
| Binary Classification Model Comparison | Supervised Binary Classification | Completed | [binary-classification/README.md](binary-classification/README.md) |

---

## Project Purpose

The main goal of this repository is not only to find a single best-performing model, but to compare many supervised machine learning algorithms in a consistent, practical, and reproducible way.

The projects demonstrate:

- End-to-end supervised machine learning workflows
- Data preprocessing with scikit-learn pipelines
- Baseline model training
- Hyperparameter tuning
- Cross-validation
- Final test-set evaluation
- Practical model comparison
- Runtime and prediction speed comparison
- Saved fitted model size comparison
- Prediction, residual, and error analysis
- Confusion matrix, ROC, and Precision-Recall analysis for classification
- Decision threshold analysis for classification
- Feature / permutation importance
- Exported HTML reports
- Portfolio-ready visual summaries and result tables

---

## Dataset

Both projects use the `diamonds` dataset.

The dataset contains information about diamonds, including physical measurements and quality-related attributes such as carat, cut, colour, clarity, depth, table, dimensions, and price.

The same dataset is used for both projects so that the focus remains on comparing supervised learning approaches rather than changing the data source.

---

## Final Regression Result

The best-performing model in the final regression comparison was the **Tuned Stacking Regressor**.

| Model | Test MAE | Test RMSE | Test R² |
|---|---:|---:|---:|
| Tuned Stacking Regressor | 264.66 | 522.41 | 0.9829 |
| Tuned Voting Regressor | 263.88 | 523.72 | 0.9828 |

The **Tuned Stacking Regressor** achieved the best overall RMSE, while the **Tuned Voting Regressor** produced a very similar result and achieved the lowest MAE among the top models.

The full notebook runtime for the final completed regression run was:

```text
11:42:29
```

From a practical model selection perspective, the best statistical model is not always the only reasonable choice. The regression project also considers training time, prediction time, saved fitted model size, model complexity, and deployment practicality. In this context, models such as tuned LightGBM and tuned CatBoost can be attractive practical alternatives because they provide strong performance with simpler model artifacts than the largest ensemble combinations.

---

## Final Binary Classification Result

The best-performing model in the final binary classification comparison was the **Tuned Stacking Classifier**.

| Model | Test Accuracy | Test Precision | Test Recall | Test F1-score | Test ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Tuned Stacking Classifier | 0.9122 | 0.8815 | 0.8624 | 0.8719 | 0.9682 |
| Tuned Voting Classifier | 0.9118 | 0.8957 | 0.8434 | 0.8688 | 0.9673 |

The **Tuned Stacking Classifier** achieved the best overall default-threshold test performance based on the primary F1-score metric.

The **Tuned Voting Classifier** produced a very similar result and was the strongest fast ensemble alternative, with a much shorter measured model time.

The full notebook runtime for the final completed binary classification run was:

```text
6:17:19
```

The decision threshold mini experiment showed that the tuned Stacking Classifier's F1-score could be slightly improved from **0.8719** to **0.8742** by lowering the decision threshold from **0.50** to **0.35**. This increased recall but reduced precision, showing the practical trade-off between false positives and false negatives.

---

## Repository Structure

```text
ml-supervised-model-comparison/
├── .gitattributes
├── .gitignore
├── COPYRIGHT.md
├── environment.yml
├── README.md
├── requirements.txt
│
├── regression/
│   ├── README.md
│   │
│   ├── notebooks/
│   │   └── supervised_regression_model_comparison.ipynb
│   │
│   ├── reports/
│   │   └── supervised_regression_model_comparison.html
│   │
│   ├── images/
│   │   ├── supervised_regression_model_comparison.png
│   │   ├── supervised_regression_tuned_model_comparison_table.png
│   │   ├── supervised_regression_practical_comparison_table.png
│   │   ├── supervised_regression_selected_test_sample_predictions.png
│   │   ├── supervised_regression_prediction_range_difference_summary.png
│   │   ├── supervised_regression_best_model_performance_by_price_range.png
│   │   ├── supervised_regression_actual_vs_predicted_best_model.png
│   │   ├── supervised_regression_actual_vs_predicted_all_models.png
│   │   ├── supervised_regression_actual_vs_predicted_distributions_by_model_group.png
│   │   ├── supervised_regression_residuals_best_model.png
│   │   ├── supervised_regression_residuals_all_models.png
│   │   ├── supervised_regression_error_distribution_best_model.png
│   │   ├── supervised_regression_error_distribution_all_models.png
│   │   └── supervised_regression_permutation_importance.png
│   │
│   └── results/
│       ├── supervised_regression_tuned_model_comparison_table.csv
│       ├── supervised_regression_practical_comparison.csv
│       ├── supervised_regression_selected_test_sample_predictions.csv
│       ├── supervised_regression_prediction_range_difference_summary.csv
│       └── supervised_regression_best_model_performance_by_price_range.csv
│
└── binary-classification/
    ├── README.md
    │
    ├── notebooks/
    │   └── supervised_binary_classification_model_comparison.ipynb
    │
    ├── reports/
    │   └── supervised_binary_classification_model_comparison.html
    │
    ├── images/
    │   ├── supervised_binary_classification_actual_vs_predicted_all_models.png
    │   ├── supervised_binary_classification_actual_vs_predicted_best_model.png
    │   ├── supervised_binary_classification_best_model_correctness_check.png
    │   ├── supervised_binary_classification_best_model_performance_by_price_range.png
    │   ├── supervised_binary_classification_confusion_matrices_all_models.png
    │   ├── supervised_binary_classification_confusion_matrix_best_model.png
    │   ├── supervised_binary_classification_decision_threshold_metrics_comparison.png
    │   ├── supervised_binary_classification_decision_threshold_results.png
    │   ├── supervised_binary_classification_decision_threshold_summary.png
    │   ├── supervised_binary_classification_errors_all_models.png
    │   ├── supervised_binary_classification_errors_best_model.png
    │   ├── supervised_binary_classification_high_price_class_distribution.png
    │   ├── supervised_binary_classification_high_price_confusion_matrix.png
    │   ├── supervised_binary_classification_high_price_metrics_summary.png
    │   ├── supervised_binary_classification_model_comparison.png
    │   ├── supervised_binary_classification_permutation_importance.png
    │   ├── supervised_binary_classification_practical_comparison_table.png
    │   ├── supervised_binary_classification_precision_recall_curve_all_models.png
    │   ├── supervised_binary_classification_precision_recall_curve_best_model.png
    │   ├── supervised_binary_classification_precision_recall_curve_by_model_family.png
    │   ├── supervised_binary_classification_precision_recall_curve_individual_models.png
    │   ├── supervised_binary_classification_prediction_agreement_error_summary.png
    │   ├── supervised_binary_classification_roc_curve_all_models.png
    │   ├── supervised_binary_classification_roc_curve_best_model.png
    │   ├── supervised_binary_classification_roc_curve_by_model_family.png
    │   ├── supervised_binary_classification_roc_curve_individual_models.png
    │   ├── supervised_binary_classification_selected_test_sample_predictions.png
    │   └── supervised_binary_classification_tuned_model_comparison_table.png
    │
    └── results/
        ├── supervised_binary_classification_best_model_correctness_check.csv
        ├── supervised_binary_classification_best_model_performance_by_price_range.csv
        ├── supervised_binary_classification_decision_threshold_metrics_comparison.csv
        ├── supervised_binary_classification_decision_threshold_results.csv
        ├── supervised_binary_classification_decision_threshold_summary.csv
        ├── supervised_binary_classification_high_price_class_distribution.csv
        ├── supervised_binary_classification_high_price_confusion_matrix.csv
        ├── supervised_binary_classification_high_price_metrics_summary.csv
        ├── supervised_binary_classification_practical_comparison.csv
        ├── supervised_binary_classification_prediction_agreement_error_summary.csv
        ├── supervised_binary_classification_selected_test_sample_predictions.csv
        └── supervised_binary_classification_tuned_model_comparison_table.csv
```

---

## Project Files

### Regression

- Main notebook: [supervised_regression_model_comparison.ipynb](regression/notebooks/supervised_regression_model_comparison.ipynb)
- HTML report: [supervised_regression_model_comparison.html](regression/reports/supervised_regression_model_comparison.html)
- Detailed README: [regression/README.md](regression/README.md)

### Binary Classification

- Main notebook: [supervised_binary_classification_model_comparison.ipynb](binary-classification/notebooks/supervised_binary_classification_model_comparison.ipynb)
- HTML report: [supervised_binary_classification_model_comparison.html](binary-classification/reports/supervised_binary_classification_model_comparison.html)
- Detailed README: [binary-classification/README.md](binary-classification/README.md)

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

The primary comparison metric is **RMSE**, while MAE, R², train-test gap, residual behaviour, runtime, model size, and practical usability are also considered.

---

## Binary Classification Model Comparison

The binary classification project compares a wide range of supervised binary classification models for predicting whether a diamond belongs to a higher-clarity group.

### Target Variable

```text
is_high_clarity
```

The target is created from the original `clarity` feature. The original `clarity` column is removed from the input features to prevent data leakage.

### Main Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

The primary comparison metric is **F1-score**, while ROC-AUC, precision, recall, confusion matrix behaviour, threshold behaviour, runtime, model size, and practical usability are also considered.

---

## Example Visual Summaries

The main visual examples are organised in a balanced way across both projects.

Each row compares the same type of output from the regression project and the binary classification project:

- full tuned model comparison
- practical model selection comparison
- best-model prediction behaviour
- best-model error analysis
- permutation importance

This keeps the two completed projects structurally comparable while still respecting the different nature of regression and classification tasks.

### Balanced Visual Overview

| Visual Focus | Regression Model Comparison | Binary Classification Model Comparison |
|---|---|---|
| **Full tuned model comparison** | ![Tuned Regression Model Comparison](regression/images/supervised_regression_model_comparison.png) | ![Tuned Binary Classification Model Comparison](binary-classification/images/supervised_binary_classification_model_comparison.png) |
| **Practical model selection comparison** | ![Practical Comparison of Regression Models](regression/images/supervised_regression_practical_comparison_table.png) | ![Practical Comparison of Binary Classification Models](binary-classification/images/supervised_binary_classification_practical_comparison_table.png) |
| **Best-model prediction behaviour** | ![Regression Best Model Actual vs Predicted](regression/images/supervised_regression_actual_vs_predicted_best_model.png) | ![Binary Classification Best Model Confusion Matrix](binary-classification/images/supervised_binary_classification_confusion_matrix_best_model.png) |
| **Best-model error analysis** | ![Regression Best Model Residuals](regression/images/supervised_regression_residuals_best_model.png) | ![Binary Classification Best Model Errors](binary-classification/images/supervised_binary_classification_errors_best_model.png) |
| **Best-model permutation importance** | ![Regression Permutation Importance](regression/images/supervised_regression_permutation_importance.png) | ![Binary Classification Permutation Importance](binary-classification/images/supervised_binary_classification_permutation_importance.png) |

The detailed project README files include the full set of exported visuals and result tables.

## Model Families Compared

Across the two projects, the repository compares a broad range of supervised model families, including:

- Baseline models
- Linear and regularized linear models
- Robust and online linear models
- GLM / distribution-based linear models
- Logistic and regularized logistic models
- Support vector / margin-based models
- Distance-based models
- Probabilistic models
- Discriminant analysis models
- Tree-based models
- Random forest and extra trees models
- Bagging models
- Boosting models
- XGBoost models
- LightGBM models
- CatBoost models
- Voting ensembles
- Stacking ensembles
- MLP neural network models

---

## Machine Learning Workflow

Both notebooks follow a consistent supervised learning workflow:

1. Load and inspect the dataset
2. Define the target variable
3. Split the data into training and test sets
4. Build preprocessing pipelines
5. Train baseline models
6. Evaluate baseline performance
7. Tune selected models with cross-validation
8. Compare tuned models
9. Evaluate final models on the test set
10. Save selected result tables and visual outputs
11. Analyse prediction behaviour
12. Analyse residuals, errors, or classification mistakes
13. Review practical strengths and weaknesses of the models
14. Compare runtime, model complexity, and saved fitted model size
15. Interpret permutation importance for the best model

The binary classification project also includes:

- Confusion matrix analysis
- ROC curve analysis
- Precision-Recall curve analysis
- Prediction agreement and error analysis
- High-price subset analysis
- Decision threshold analysis

---

## Voting and Stacking Strategy

Both projects use a two-stage ensemble strategy for Voting and Stacking.

The initial Voting and Stacking models are built from selected untuned model pipelines.

The tuned Voting and Stacking models are built from the best estimators found by earlier hyperparameter searches. No additional Voting weight search or Stacking final-estimator grid search is applied in the final version, because these extra searches were computationally expensive and produced only small improvements in previous runs.

This keeps the comparison clear:

- **Initial Voting / Stacking:** built from selected untuned model pipelines
- **Tuned Voting / Stacking:** built from the best estimators found by earlier hyperparameter searches

---

## Practical Model Selection

The repository does not select models based only on the lowest error score or the highest classification metric.

Practical model selection may also depend on:

- training time
- prediction time
- saved fitted model file size
- model complexity
- deployment simplicity
- interpretability
- maintenance cost

This means that a slightly less accurate model may still be a better practical choice in some real-world situations.

For example, the tuned Stacking models achieved the strongest overall performance in both projects, while the tuned Voting models were very close ensemble alternatives. However, individual boosting models such as tuned LightGBM, tuned CatBoost, tuned Hist Gradient Boosting, and tuned XGBoost can be attractive practical alternatives because they provide strong performance with simpler model artifacts than the largest ensemble combinations.

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

Open one of the project notebooks:

```text
regression/notebooks/supervised_regression_model_comparison.ipynb
binary-classification/notebooks/supervised_binary_classification_model_comparison.ipynb
```

Run the selected notebook from top to bottom.

### Alternative: pip

A `requirements.txt` file is also included as a simpler pip-compatible package list:

```bash
pip install -r requirements.txt
```

The conda environment is recommended because this project uses several machine learning libraries that are often easier to manage through `conda-forge`.

---

## Notes for Reviewers

This repository is designed as a portfolio project.

The notebooks show not only final results, but also the modelling process, tuning logic, practical comparison, prediction analysis, residual or classification error analysis, runtime considerations, saved model artifacts, and visual interpretation.

The HTML reports are included to make the projects easier to review without running the notebooks locally.

The final completed notebook runtimes were:

| Project | Full Notebook Runtime |
|---|---:|
| Regression Model Comparison | 11:42:29 |
| Binary Classification Model Comparison | 6:17:19 |

Runtime may vary depending on hardware, package versions, parallel processing configuration, and whether saved model artifacts are reloaded.

This repository does not include the saved fitted model artifacts or local `_exports` folders. The published version focuses on the notebooks, HTML reports, result tables, visual outputs, and documentation.

---

## Author

**Milan Olah**  
Supervised Machine Learning Model Comparison  
Data Science / Machine Learning Portfolio Project

---

## Copyright

© 2026 Milan Olah. All rights reserved.

This project is shared publicly for portfolio and educational demonstration purposes.  
No permission is granted to copy, redistribute, modify, sell, or present this work as your own without written permission.

For details, see [COPYRIGHT.md](COPYRIGHT.md).
