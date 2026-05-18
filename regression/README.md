# Supervised Regression Model Comparison

A structured machine learning project comparing multiple supervised regression models for predicting diamond prices.

This project is part of the larger repository:

[Supervised ML Model Comparison](../README.md)

---

## Project Objective

The objective of this project is to compare a wide range of supervised regression models using the same dataset, preprocessing strategy, evaluation workflow, and final test set.

The focus is not only on finding the best-performing model, but also on understanding the practical differences between model families.

The project compares models by:

- Predictive performance
- Error metrics
- Cross-validation behaviour
- Final test-set performance
- Training and prediction time
- Practical strengths and weaknesses
- Feature importance where appropriate

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

An exported HTML version of the notebook for easier viewing.

### Results

[results/supervised_regression_final_results.csv](results/supervised_regression_final_results.csv)

Final model evaluation table.

[results/supervised_regression_practical_comparison.csv](results/supervised_regression_practical_comparison.csv)

Practical comparison table describing model behaviour and usability.

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

### Robust and Online Linear Models

- Huber Regressor
- RANSAC Regressor
- SGD Regressor
- Passive Aggressive Regressor

### Support Vector Models

- Linear SVR
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
9. Store best estimators
10. Compare tuned model performance
11. Evaluate final models on the test set
12. Save final results
13. Analyse predictions
14. Visualise model behaviour
15. Interpret feature importance where appropriate

---

## Visual Outputs

### Model Comparison

![Regression Model Comparison](images/supervised_regression_model_comparison.png)

### Actual vs Predicted Values

![Actual vs Predicted](images/supervised_regression_actual_vs_predicted.png)

### Residual Analysis

![Residuals](images/supervised_regression_residuals.png)

### Feature Importance

![Feature Importance](images/supervised_regression_feature_importance.png)

---

## Example Result Summary

TODO: Replace this section with the final model results after the final full run.

| Model | RMSE | R² | Notes |
|---|---:|---:|---|
| TODO | TODO | TODO | Best overall regression model |
| TODO | TODO | TODO | Strong performance and practical speed |
| TODO | TODO | TODO | Good simple baseline |

---

## Practical Model Comparison

In addition to numerical performance, the project includes a practical comparison of regression models.

The practical comparison considers:

- Speed
- Memory usage
- Overfitting tendency
- Scaling sensitivity
- Hyperparameter sensitivity
- External library requirement
- Ability to continue training
- Interpretability
- Typical use case

This makes the project useful not only for score comparison, but also for understanding when different regression models may be appropriate in real-world use.

---

## Key Learning Outcomes

This project demonstrates the ability to:

- Build a complete regression modelling workflow
- Use scikit-learn pipelines correctly
- Compare many regression model families
- Apply cross-validation and hyperparameter tuning
- Evaluate models with appropriate regression metrics
- Interpret final results beyond a single score
- Save results, reports, and visual outputs
- Present a machine learning project clearly for portfolio purposes

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

From the root of the repository:

```bash
pip install -r requirements.txt
jupyter notebook
```

Then open:

```text
regression/notebooks/supervised_regression_model_comparison.ipynb
```

Run the notebook from top to bottom.

---

## Notes

Large exported models, temporary files, local cache files, and environment-specific files should not be included in the public repository.

The public version is intended to show the modelling process, results, and practical comparison clearly without unnecessary local files.

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
