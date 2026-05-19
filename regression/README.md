# Supervised Regression Model Comparison

A structured machine learning portfolio project comparing multiple supervised regression models for predicting diamond prices.

This project is part of the larger repository:

[Supervised ML Model Comparison](../README.md)

---

## Project Objective

The objective of this project is to compare a wide range of supervised regression models using the same dataset, preprocessing strategy, evaluation workflow, and final test set.

The focus is not only on finding the best-performing model, but also on understanding the practical differences between model families.

The project compares models by:

- Predictive performance
- Regression error metrics
- Cross-validation behaviour
- Final test-set performance
- Training and prediction speed
- Practical strengths and weaknesses
- Prediction behaviour across price ranges
- Residual and error distributions
- Permutation importance for the best model

---

## Dataset

This project uses the diamonds dataset.

The dataset contains physical and categorical information about diamonds, such as size, quality, and dimensions.

Typical features include:

- carat
- cut
- color
- clarity
- depth
- table
- x
- y
- z

---

## Target Variable

The regression target is:

```text
price
```

The task is to predict the price of a diamond based on its available features.

---

## Files

### Notebook

[notebooks/supervised_regression_model_comparison.ipynb](notebooks/supervised_regression_model_comparison.ipynb)

The main Jupyter Notebook containing the full regression workflow.

### HTML Report

[reports/supervised_regression_model_comparison.html](reports/supervised_regression_model_comparison.html)

An exported HTML version of the notebook for easier viewing without running the notebook locally.

### Result Tables

[results/supervised_regression_tuned_model_comparison_table.csv](results/supervised_regression_tuned_model_comparison_table.csv)

Tuned regression model comparison table.

[results/supervised_regression_practical_comparison.csv](results/supervised_regression_practical_comparison.csv)

Practical comparison table describing model behaviour, usability, speed, memory usage, tuning cost, overfitting tendency, scaling sensitivity, and historical model context.

[results/supervised_regression_selected_test_sample_predictions.csv](results/supervised_regression_selected_test_sample_predictions.csv)

Prediction comparison on selected test samples.

[results/supervised_regression_prediction_range_difference_summary.csv](results/supervised_regression_prediction_range_difference_summary.csv)

Prediction range and difference summary.

[results/supervised_regression_best_model_performance_by_price_range.csv](results/supervised_regression_best_model_performance_by_price_range.csv)

Best model performance by price range.

---

## Evaluation Metrics

The regression models are evaluated using:

| Metric | Meaning |
|---|---|
| MAE | Mean Absolute Error |
| MSE | Mean Squared Error |
| RMSE | Root Mean Squared Error |
| R² Score | Proportion of variance explained by the model |

The main comparison focuses especially on:

- **RMSE** – because it shows the typical prediction error in the target unit
- **R² Score** – because it shows how much variance is explained by the model

---

## Models Compared

The project compares a wide range of regression model families, including:

### Baseline Model

- Dummy Regressor

### Linear and Regularized Models

- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- Bayesian Ridge
- Quantile Regressor

### Robust and Online Linear Models

- Huber Regressor
- RANSAC Regressor
- SGD Regressor
- Passive Aggressive Regressor

### GLM / Distribution-Based Linear Models

- Poisson Regressor
- Gamma Regressor

### Support Vector Models

- SVR with linear kernel
- SVR with RBF kernel
- NuSVR

### Distance-Based Models

- K-Nearest Neighbors Regressor

### Tree-Based Models

- Decision Tree Regressor
- Random Forest Regressor
- Extra Trees Regressor

### Boosting Models

- AdaBoost Regressor
- Gradient Boosting Regressor
- HistGradientBoosting Regressor
- XGBoost Regressor
- LightGBM Regressor
- CatBoost Regressor

### Ensemble and Neural Models

- Bagging Regressor
- Voting Regressor
- Stacking Regressor
- MLP Regressor

---

## Workflow

The project follows this workflow:

1. Import libraries and configure global settings
2. Load and inspect the dataset
3. Define features and target
4. Split the data into training and test sets
5. Build preprocessing pipelines
6. Train baseline regression models
7. Evaluate baseline models
8. Tune selected models with cross-validation
9. Store best estimators and predictions where required
10. Compare tuned model performance
11. Evaluate final models on the test set
12. Export selected result tables and visual outputs
13. Analyse selected test sample predictions
14. Analyse actual vs predicted values
15. Analyse prediction ranges and price-range performance
16. Analyse residuals and error distributions
17. Interpret permutation importance for the best model
18. Compare practical strengths and weaknesses of the models

---

## Visual Outputs

### Tuned Regression Model Comparison

![Tuned Regression Model Comparison](images/supervised_regression_model_comparison.png)

### Tuned Regression Model Comparison Table

![Tuned Regression Model Comparison Table](images/supervised_regression_tuned_model_comparison_table.png)

### Practical Comparison of Regression Models

![Practical Comparison of Regression Models](images/supervised_regression_practical_comparison_table.png)

### Prediction Comparison on Selected Test Samples

![Prediction Comparison on Selected Test Samples](images/supervised_regression_selected_test_sample_predictions.png)

### Prediction Range and Difference Summary

![Prediction Range and Difference Summary](images/supervised_regression_prediction_range_difference_summary.png)

### Best Model Performance by Price Range

![Best Model Performance by Price Range](images/supervised_regression_best_model_performance_by_price_range.png)

### Actual vs Predicted Values for the Best Regression Model

![Actual vs Predicted - Best Model](images/supervised_regression_actual_vs_predicted_best_model.png)

### Actual vs Predicted Values for All Tuned Regression Models

![Actual vs Predicted - All Models](images/supervised_regression_actual_vs_predicted_all_models.png)

### Actual vs Predicted Price Distributions by Model Group

![Actual vs Predicted Distributions by Model Group](images/supervised_regression_actual_vs_predicted_distributions_by_model_group.png)

### Residual Plot for the Best Regression Model

![Residuals - Best Model](images/supervised_regression_residuals_best_model.png)

### Residual Plots for All Tuned Regression Models

![Residuals - All Models](images/supervised_regression_residuals_all_models.png)

### Error Distribution for the Best Regression Model

![Error Distribution - Best Model](images/supervised_regression_error_distribution_best_model.png)

### Error Distributions for All Tuned Regression Models

![Error Distributions - All Models](images/supervised_regression_error_distribution_all_models.png)

### Permutation Importance for the Best Regression Model

![Permutation Importance](images/supervised_regression_permutation_importance.png)

---

## Practical Model Comparison

In addition to numerical performance, the project includes a practical comparison of regression models.

The practical comparison considers:

- Approximate historical release / origin year
- Predictive performance
- Base fit speed
- Prediction speed
- Tuning cost
- Memory use
- Overfitting tendency
- Scaling sensitivity
- Whether scaling is required or recommended
- Hyperparameter sensitivity
- External library requirement
- Whether the model can continue training
- Practical summary of each model

The practical scores are project-based ratings on a 0–10 scale. They reflect the behaviour observed in this notebook and are intended as practical guidance for this project, not as universal theoretical rankings.

---

## Key Learning Outcomes

This project demonstrates the ability to:

- Build a complete regression modelling workflow
- Use scikit-learn pipelines correctly
- Compare many regression model families
- Apply cross-validation and hyperparameter tuning
- Evaluate models with appropriate regression metrics
- Interpret final results beyond a single score
- Analyse prediction errors and residual behaviour
- Compare model behaviour across different price ranges
- Save selected results, reports, and visual outputs
- Present a machine learning project clearly for portfolio purposes

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

From the root of the repository:

```bash
conda env create -f environment.yml
conda activate supervised-ml-model-comparison
jupyter notebook
```

Then open:

```text
regression/notebooks/supervised_regression_model_comparison.ipynb
```

Run the notebook from top to bottom.

### Alternative: pip

A `requirements.txt` file is also included as a simpler pip-compatible package list:

```bash
pip install -r requirements.txt
jupyter notebook
```

The conda environment is recommended because this project uses several machine learning libraries that are often easier to manage through `conda-forge`.

---

## Exported Files

The notebook can export selected portfolio outputs into a local `_exports/regression_models/` folder.

The public GitHub version includes the selected final outputs in:

```text
regression/images/
regression/results/
```

Large model artifacts, temporary files, local cache files, and environment-specific files should not be included in the public repository.

---

## Notes

The public version is intended to show the modelling process, result summaries, visual outputs, and practical comparison clearly without unnecessary local files.

The HTML report is included to make the project easy to review without running the notebook locally.

---

## Author

**Milan Olah**  
Data Science / Machine Learning Portfolio Project

---

## Copyright

© 2026 Milan Olah. All rights reserved.

This project is shared publicly for portfolio and educational demonstration purposes.  
No permission is granted to copy, redistribute, modify, sell, or present this work as your own without written permission.

For details, see [../COPYRIGHT.md](../COPYRIGHT.md).
