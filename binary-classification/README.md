# Supervised Binary Classification Model Comparison

A structured machine learning portfolio project comparing multiple supervised binary classification models for predicting whether a diamond belongs to a higher-clarity group.

This project is part of the larger repository:

[Supervised Machine Learning Model Comparison](../README.md)

---

## Project Objective

The objective of this project is to compare a wide range of supervised binary classification models using the same dataset, preprocessing strategy, evaluation workflow, and final test set.

The focus is not only on finding the best-performing classifier, but also on understanding the practical differences between model families.

The project compares models by:

- Predictive performance
- Binary classification metrics
- Cross-validation behaviour
- Final test-set performance
- Training and prediction speed
- Saved fitted model file size
- Practical strengths and weaknesses
- Prediction agreement and error behaviour
- Performance across price ranges
- High-price classification behaviour
- Confusion matrix behaviour
- ROC and Precision-Recall curve behaviour
- Decision threshold behaviour
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

The binary classification target is:

```text
is_high_clarity
```

The target is created from the original `clarity` feature.

Lower clarity grades are assigned to class 0, while higher clarity grades are assigned to class 1. The original `clarity` column is removed from the input features to prevent data leakage.

The task is to predict whether a diamond belongs to a higher-clarity group based on the remaining available features.

---

## Final Binary Classification Result

The best-performing model in the final binary classification comparison was the **Tuned Stacking Classifier**.

| Model | Test Accuracy | Test Precision | Test Recall | Test F1-score | Test ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Tuned Stacking Classifier | 0.9122 | 0.8815 | 0.8624 | 0.8719 | 0.9682 |
| Tuned Voting Classifier | 0.9118 | 0.8957 | 0.8434 | 0.8688 | 0.9673 |

The **Tuned Stacking Classifier** achieved the best overall default-threshold test performance based on the primary F1-score metric.

The **Tuned Voting Classifier** produced a very similar result and was the strongest fast ensemble alternative, with a much shorter measured model time.

The full notebook runtime for the final completed run was:

```text
6:17:19
```

The decision threshold mini experiment showed that the tuned Stacking Classifier's F1-score could be slightly improved from **0.8719** to **0.8742** by lowering the decision threshold from **0.50** to **0.35**. This increased recall but reduced precision, showing the practical trade-off between false positives and false negatives.

Although the tuned Stacking Classifier was the best model based on the primary F1-score metric, the project also considers practical model selection factors such as runtime, prediction speed, saved fitted model size, model complexity, and deployment simplicity.

---

## Files

### Notebook

[notebooks/supervised_binary_classification_model_comparison.ipynb](notebooks/supervised_binary_classification_model_comparison.ipynb)

The main Jupyter Notebook containing the full binary classification workflow.

### HTML Report

[reports/supervised_binary_classification_model_comparison.html](reports/supervised_binary_classification_model_comparison.html)

An exported HTML version of the notebook for easier viewing without running the notebook locally.

### Result Tables

[results/supervised_binary_classification_tuned_model_comparison_table.csv](results/supervised_binary_classification_tuned_model_comparison_table.csv)

Tuned binary classification model comparison table.

[results/supervised_binary_classification_practical_comparison.csv](results/supervised_binary_classification_practical_comparison.csv)

Practical comparison table describing model behaviour, usability, speed, memory usage, tuning cost, overfitting tendency, scaling sensitivity, threshold behaviour, and historical model context.

[results/supervised_binary_classification_selected_test_sample_predictions.csv](results/supervised_binary_classification_selected_test_sample_predictions.csv)

Prediction comparison on selected test samples.

[results/supervised_binary_classification_best_model_correctness_check.csv](results/supervised_binary_classification_best_model_correctness_check.csv)

Correctness check for selected predictions of the best model.

[results/supervised_binary_classification_prediction_agreement_error_summary.csv](results/supervised_binary_classification_prediction_agreement_error_summary.csv)

Prediction agreement and error summary across tuned models.

[results/supervised_binary_classification_best_model_performance_by_price_range.csv](results/supervised_binary_classification_best_model_performance_by_price_range.csv)

Best model performance by price range.

[results/supervised_binary_classification_high_price_metrics_summary.csv](results/supervised_binary_classification_high_price_metrics_summary.csv)

High-price classification performance summary.

[results/supervised_binary_classification_high_price_class_distribution.csv](results/supervised_binary_classification_high_price_class_distribution.csv)

Class distribution summary for the high-price subset.

[results/supervised_binary_classification_high_price_confusion_matrix.csv](results/supervised_binary_classification_high_price_confusion_matrix.csv)

Confusion matrix for the high-price subset.

[results/supervised_binary_classification_decision_threshold_summary.csv](results/supervised_binary_classification_decision_threshold_summary.csv)

Summary of the selected decision threshold experiment.

[results/supervised_binary_classification_decision_threshold_metrics_comparison.csv](results/supervised_binary_classification_decision_threshold_metrics_comparison.csv)

Comparison between the default threshold and the best F1 threshold.

[results/supervised_binary_classification_decision_threshold_results.csv](results/supervised_binary_classification_decision_threshold_results.csv)

Detailed decision threshold experiment results.

---

## Evaluation Metrics

The binary classification models are evaluated using:

| Metric | Meaning |
|---|---|
| Accuracy | Proportion of all predictions that are correct |
| Precision | Proportion of predicted positive cases that are actually positive |
| Recall | Proportion of actual positive cases correctly identified |
| F1-score | Harmonic mean of precision and recall |
| ROC-AUC | Ranking quality across classification thresholds |

The main comparison focuses especially on:

- **F1-score** – because it balances precision and recall and is the primary model-ranking metric in this project
- **ROC-AUC** – because it evaluates how well the model separates the two classes across thresholds
- **Precision and Recall** – because they show the trade-off between false positives and false negatives
- **Accuracy** – because it provides a general correctness measure, but can be less informative on its own

The project also considers confusion matrix behaviour, threshold behaviour, runtime, prediction speed, saved fitted model size, and practical usability.

---

## Models Compared

The project compares a wide range of binary classification model families, including:

### Baseline Model

- Dummy Classifier

### Logistic and Regularized Linear Models

- Logistic Regression with L2 regularization
- Logistic Regression with L1 regularization
- Logistic Regression with ElasticNet regularization
- Ridge Classifier
- SGD Classifier
- Passive Aggressive Classifier

### Support Vector / Margin-Based Models

- Linear SVC
- SVC with linear kernel
- SVC with RBF kernel

### Distance-Based Models

- K-Nearest Neighbors Classifier
- Nearest Centroid Classifier

### Probabilistic Models

- Gaussian Naive Bayes
- Bernoulli Naive Bayes

### Discriminant Analysis Models

- Linear Discriminant Analysis
- Quadratic Discriminant Analysis

### Tree-Based Models

- Decision Tree Classifier
- Extra Tree Classifier
- Random Forest Classifier
- Extra Trees Classifier

### Boosting Models

- AdaBoost Classifier
- Gradient Boosting Classifier
- HistGradientBoosting Classifier
- XGBoost Classifier
- LightGBM Classifier
- CatBoost Classifier

### Ensemble and Neural Models

- Bagging Classifier
- Voting Classifier
- Stacking Classifier
- MLP Classifier

---

## Workflow

The project follows this workflow:

1. Import libraries and configure global settings
2. Load and inspect the dataset
3. Create the binary target variable
4. Remove the original `clarity` column to prevent data leakage
5. Define features and target
6. Split the data into training and test sets
7. Build preprocessing pipelines
8. Train baseline binary classification models
9. Evaluate baseline models
10. Tune selected models with cross-validation
11. Store best estimators, predictions, probability scores, and decision scores where required
12. Compare tuned model performance
13. Evaluate final models on the test set
14. Export selected result tables and visual outputs
15. Analyse selected test sample predictions
16. Analyse prediction agreement and error behaviour
17. Analyse actual vs predicted class behaviour
18. Analyse price-range and high-price classification performance
19. Analyse confusion matrices
20. Analyse ROC curves and Precision-Recall curves
21. Compare practical strengths and weaknesses of the models
22. Compare runtime, model complexity, and saved fitted model size
23. Interpret permutation importance for the best model
24. Run a decision threshold mini experiment

---

## Voting and Stacking Strategy

The project uses a two-stage ensemble strategy for Voting and Stacking.

The initial Voting and Stacking classifiers are built from selected untuned classifier pipelines.

The tuned Voting and Stacking classifiers are built from the best estimators found by earlier hyperparameter searches. No additional Voting weight search or Stacking final-estimator grid search is applied in the final version, because these extra searches were computationally expensive and produced only small improvements in previous runs.

This keeps the comparison clear:

- **Initial Voting / Stacking:** built from selected untuned classifier pipelines
- **Tuned Voting / Stacking:** built from the best estimators found by earlier hyperparameter searches

---

## Visual Outputs

### Tuned Binary Classification Model Comparison

![Tuned Binary Classification Model Comparison](images/supervised_binary_classification_model_comparison.png)

### Tuned Binary Classification Model Comparison Table

![Tuned Binary Classification Model Comparison Table](images/supervised_binary_classification_tuned_model_comparison_table.png)

### Practical Comparison of Binary Classification Models

![Practical Comparison of Binary Classification Models](images/supervised_binary_classification_practical_comparison_table.png)

### Prediction Comparison on Selected Test Samples

![Prediction Comparison on Selected Test Samples](images/supervised_binary_classification_selected_test_sample_predictions.png)

### Best Model Correctness Check

![Best Model Correctness Check](images/supervised_binary_classification_best_model_correctness_check.png)

### Prediction Agreement and Error Summary

![Prediction Agreement and Error Summary](images/supervised_binary_classification_prediction_agreement_error_summary.png)

### Best Model Performance by Price Range

![Best Model Performance by Price Range](images/supervised_binary_classification_best_model_performance_by_price_range.png)

### High-Price Metrics Summary

![High-Price Metrics Summary](images/supervised_binary_classification_high_price_metrics_summary.png)

### High-Price Class Distribution

![High-Price Class Distribution](images/supervised_binary_classification_high_price_class_distribution.png)

### High-Price Confusion Matrix

![High-Price Confusion Matrix](images/supervised_binary_classification_high_price_confusion_matrix.png)

### Confusion Matrix for the Best Classification Model

![Confusion Matrix - Best Model](images/supervised_binary_classification_confusion_matrix_best_model.png)

### Confusion Matrices for All Tuned Classification Models

![Confusion Matrices - All Models](images/supervised_binary_classification_confusion_matrices_all_models.png)

### Actual vs Predicted Classes for the Best Classification Model

![Actual vs Predicted - Best Model](images/supervised_binary_classification_actual_vs_predicted_best_model.png)

### Actual vs Predicted Classes for All Tuned Classification Models

![Actual vs Predicted - All Models](images/supervised_binary_classification_actual_vs_predicted_all_models.png)

### Classification Errors for the Best Classification Model

![Classification Errors - Best Model](images/supervised_binary_classification_errors_best_model.png)

### Classification Errors for All Tuned Classification Models

![Classification Errors - All Models](images/supervised_binary_classification_errors_all_models.png)

### ROC Curve for the Best Classification Model

![ROC Curve - Best Model](images/supervised_binary_classification_roc_curve_best_model.png)

### ROC Curves for All Tuned Classification Models

![ROC Curves - All Models](images/supervised_binary_classification_roc_curve_all_models.png)

### ROC Curves by Model Family

![ROC Curves by Model Family](images/supervised_binary_classification_roc_curve_by_model_family.png)

### Individual ROC Curves

![Individual ROC Curves](images/supervised_binary_classification_roc_curve_individual_models.png)

### Precision-Recall Curve for the Best Classification Model

![Precision-Recall Curve - Best Model](images/supervised_binary_classification_precision_recall_curve_best_model.png)

### Precision-Recall Curves for All Tuned Classification Models

![Precision-Recall Curves - All Models](images/supervised_binary_classification_precision_recall_curve_all_models.png)

### Precision-Recall Curves by Model Family

![Precision-Recall Curves by Model Family](images/supervised_binary_classification_precision_recall_curve_by_model_family.png)

### Individual Precision-Recall Curves

![Individual Precision-Recall Curves](images/supervised_binary_classification_precision_recall_curve_individual_models.png)

### Decision Threshold Summary

![Decision Threshold Summary](images/supervised_binary_classification_decision_threshold_summary.png)

### Decision Threshold Metrics Comparison

![Decision Threshold Metrics Comparison](images/supervised_binary_classification_decision_threshold_metrics_comparison.png)

### Decision Threshold Results

![Decision Threshold Results](images/supervised_binary_classification_decision_threshold_results.png)

### Permutation Importance for the Best Classification Model

![Permutation Importance](images/supervised_binary_classification_permutation_importance.png)

---

## Practical Model Comparison

In addition to numerical performance, the project includes a practical comparison of binary classification models.

The practical comparison considers:

- Approximate historical release / origin year
- Predictive performance
- Base fit speed
- Prediction speed
- Tuning cost
- Memory use
- Saved fitted model file size
- Overfitting tendency
- Scaling sensitivity
- Whether scaling is required or recommended
- Hyperparameter sensitivity
- External library requirement
- Whether the model can continue training
- Probability output support
- Threshold adjustment suitability
- Practical summary of each model

The practical scores are project-based ratings on a 0–10 scale. They reflect the behaviour observed in this notebook and are intended as practical guidance for this project, not as universal theoretical rankings.

---

## Practical Model Selection

Model selection is not only about predictive accuracy. In practical machine learning workflows, runtime, prediction speed, file size, memory use, threshold behaviour, and deployment complexity can also influence which model is the best choice.

The saved fitted model file sizes add a useful practical perspective to the final comparison. They give an approximate indication of how large each trained model artifact is when saved and reused. This is important because a highly accurate model may not always be the most practical option if it is slow to train, slow to predict, large to store, or more complex to deploy.

Search object sizes are not used for practical deployment comparison because search objects can contain cross-validation metadata, parameter search results, and additional information that would normally not be needed when deploying only the final fitted model.

In this project, the tuned Stacking Classifier achieved the best overall default-threshold F1-score, while the tuned Voting Classifier produced a very similar result with much lower measured model time. However, both models are ensemble-based and can be more complex or larger than some individual models. From a practical point of view, tuned LightGBM, tuned CatBoost, tuned Hist Gradient Boosting, and tuned XGBoost are especially attractive alternatives because they achieved strong predictive performance while remaining simpler than the largest ensemble combinations.

This shows that the best model depends on the practical goal. If the priority is the best default-threshold F1-score, the tuned Stacking Classifier is the best choice in this project. If the priority is a strong balance between accuracy, F1-score, ROC-AUC, training time, prediction speed, saved model size, and deployment simplicity, tuned LightGBM, tuned CatBoost, tuned Hist Gradient Boosting, or tuned XGBoost may be more practical choices.

---

## Decision Threshold Experiment

The notebook includes a decision threshold mini experiment for the best classification model.

Using the default threshold of **0.50**, the tuned Stacking Classifier achieved:

| Threshold | Precision | Recall | F1-score |
|---:|---:|---:|---:|
| 0.50 | 0.8815 | 0.8624 | 0.8719 |

The best F1-score in the threshold experiment was achieved at a threshold of **0.35**:

| Threshold | Precision | Recall | F1-score |
|---:|---:|---:|---:|
| 0.35 | 0.8521 | 0.8975 | 0.8742 |

This shows that lowering the threshold slightly improved F1-score and recall, but reduced precision. In a real-world classification setting, the preferred threshold would depend on the practical cost of false positives and false negatives.

---

## Key Learning Outcomes

This project demonstrates the ability to:

- Build a complete binary classification modelling workflow
- Create a suitable binary target variable from an existing categorical feature
- Prevent target leakage by removing the original source feature
- Use scikit-learn pipelines correctly
- Compare many binary classification model families
- Apply cross-validation and hyperparameter tuning
- Evaluate models with appropriate classification metrics
- Interpret final results beyond a single score
- Analyse prediction agreement and error behaviour
- Analyse confusion matrices, ROC curves, and Precision-Recall curves
- Compare model behaviour across different price ranges
- Compare runtime, practical usability, and saved fitted model size
- Explore the effect of decision threshold adjustment
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
binary-classification/notebooks/supervised_binary_classification_model_comparison.ipynb
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

The notebook can export selected portfolio outputs into a local `_exports/binary_classification_models/` folder.

The public GitHub version includes the selected final outputs in:

```text
binary-classification/images/
binary-classification/results/
```

Large model artifacts, search objects, temporary files, local cache files, and environment-specific files should not be included in the public repository.

---

## Notes for Reviewers

The public version is intended to show the modelling process, result summaries, visual outputs, practical comparison, and model selection reasoning clearly without unnecessary local files.

The HTML report is included to make the project easy to review without running the notebook locally.

The full notebook runtime for the final completed run was **6:17:19**. Runtime may vary depending on hardware, package versions, and parallel processing configuration.

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

For details, see [../COPYRIGHT.md](../COPYRIGHT.md).
