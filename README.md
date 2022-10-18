# Adult Census Income Classification
Build classification model with different model and try to hyperparameter tuning with random search.
Dataset from this Kaggle [Adult Census Income](https://www.kaggle.com/datasets/uciml/adult-census-income)

## Data Pre-processing
* Check null values
* Exploration Data </br>
  At this process, I checked outliers and changed age and hours.per.week to categorical data.
* Data Transformation </br>
  Used label encode to categorical data and oversampling to handle imbalanced data after that do normalization.

## Hyperparameter tuning
Tuning hyperparameter with random search in XGB Classifier Model.
Here's my set of my best parms: n_estimators: 500, min_child_weight: 1, max_leaves: 8, max_depth: 15, learning_rate: 0.05

## Model results
Here's my result with testing data.
 | Model        | Accuracy  | Recall   | Precision | F1      |
 | ------------ | --------- | -------- | --------  | ----- - |
 | naive_bayes  | 81.2775   | 50.6335  | 55.8958   | 62.3789 |
 | logistic_reg | 75.8317   | 76.4963  | 59.7305   | 48.9927 |
 | base_xgb     | 83.2941   | 84.1415  | 70.2407   | 60.2817 |
 | tuning_xgb   | 82.9870   | 81.6077  | 60.0836   | 69.2108 |
