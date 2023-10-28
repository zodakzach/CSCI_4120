# Regression Model Comparison README

## Team Members
- Team Member 1: [Zachary Cervenka] - [cervenkaz19@students.ecu.edu]

## Overview
This project involves the comparison of three regression models: Linear Regression, Lasso Regression, and Ridge Regression. The goal is to determine which of these models provides the best performance in predicting the target variable.

## Dependencies
**pandas:** This library is used for data manipulation and handling DataFrames.

**matplotlib.pyplot:** It is used for data visualization and creating plots.

**numpy:** This library provides support for working with arrays and mathematical operations.

**sklearn.model_selection:** This module from scikit-learn is used for model selection, including cross-validation and hyperparameter tuning.

**sklearn.linear_model:** This module from scikit-learn provides various linear regression models, including Linear Regression, Lasso, and Ridge.

**sklearn.preprocessing:** This module from scikit-learn is used for data preprocessing, including feature scaling with StandardScaler.

``` bash
$ pip install pandas matplotlib numpy scikit-learn
```

## Model Comparison
Conducted a thorough analysis of the three regression models. Here are the key findings:

### Linear Regression
- **Cross-Validation Score:** 233675.59438598217
- **Alpha Value:** Not applicable (Linear Regression does not use alpha)
- **Performance:** This model provides a baseline for comparison.
### Lasso Regression
- **Cross-Validation Score:** 233371.92779237698
- **Performance:** Lasso Regression performed slightly better than Linear Regression.
### Ridge Regression
- **Cross-Validation Score:** 232567.31580303918
- **Best Ridge Alpha:** 40.37017258596558
- **Performance:** Ridge Regression outperformed both Linear and Lasso Regression.

# Conclusion
Based on the analysis, the Ridge Regression model stands out as the best performer with the lowest mean squared error. It provides the most accurate predictions for the dataset.

