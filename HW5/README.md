# Homework 5: Feature Selection and Hyperparameter Tuning with RandomForestClassifier

## Team Members
- Team Member 1: [Zachary Cervenka] - [cervenkaz19@students.ecu.edu]

## Overview
This assignment involves utilizing the RandomForestClassifier from the scikit-learn library for a breast cancer classification task. The goal is to perform feature selection and hyperparameter tuning to optimize the model's performance.

## Dataset
The dataset used for this assignment is the Breast Cancer dataset available in scikit-learn. The data is loaded using the load_breast_cancer function, and the feature matrix X and target vector y are extracted.

## Data Splitting
The dataset is split into training and testing sets using the train_test_split function. 80% of the data is used for training, and 20% for testing.

## Feature Importance and Selection
A RandomForestClassifier is trained on the training data to determine feature importances. Features with importance greater than a specified threshold (0.12) are selected.

```python
sfm = SelectFromModel(rf_classifier, threshold=0.12)
sfm.fit(X_train, y_train)
X_train_selected = sfm.transform(X_train)
X_test_selected = sfm.transform(X_test)
```

## Cross-Validation
5-fold cross-validation is performed on the original training data to assess the model's performance before hyperparameter tuning.

```Cross-Validation Scores: [0.97802198 0.94505495 0.97802198 0.95604396 0.93406593]```

## Hyperparameter Tuning
A parameter grid is defined for the RandomForestClassifier, and GridSearchCV is employed to find the best combination of hyperparameters.

```Best Parameters: {'max_depth': 5, 'min_samples_split': 2, 'n_estimators': 50}```


## Model Evaluation with Best Parameters
The RandomForestClassifier is trained using the best parameters obtained from the grid search, and its performance is evaluated on the test set.

## Results
The output of the code provides Cross-Validation Scores, the Best Parameters found through hyperparameter tuning, Best Accuracy on the test set, and Average Accuracy per Feature.

```
Best Accuracy: 0.956140350877193

Average (accuracy per feature): 0.4780701754385965
```