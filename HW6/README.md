
# SVM Kernels Comparison Readme
This readme provides an overview of the parameters selected and results obtained for Linear, Radial, and Polynomial Support Vector Machine (SVM) kernels in a classification task.

## Team Members
- Team Member 1: [Zachary Cervenka] - [cervenkaz19@students.ecu.edu]

## Linear SVM

### Parameters:
C: 1.0

### Results:
```text
Classification Report for Linear SVM:

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        33
           1       0.93      0.96      0.95        28
           2       1.00      1.00      1.00        33
           3       1.00      1.00      1.00        34
           4       1.00      1.00      1.00        46
           5       0.98      0.94      0.96        47
           6       0.97      1.00      0.99        35
           7       1.00      0.97      0.99        34
           8       0.93      0.90      0.92        30
           9       0.93      0.97      0.95        40

    accuracy                           0.97       360
   macro avg       0.97      0.97      0.97       360
weighted avg       0.98      0.97      0.97       360
```
The linear SVM achieved an accuracy of 97% on the test set. The precision, recall, and f1-score for each class are well-balanced, with a weighted average f1-score of 97%.

### Cross-validation:
`Cross-validation scores for Linear SVM: [0.97222222 0.95138889 0.94773519 0.97560976 0.95470383]`

The average cross-validation score for the linear SVM is 96.03%, indicating the model's generalization performance.

## Radial SVM
### Parameters:
C: 1000.0

Gamma: 0.1

### Results:
```text
Classification Report for Radial SVM:

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        33
           1       0.97      1.00      0.98        28
           2       1.00      1.00      1.00        33
           3       1.00      1.00      1.00        34
           4       1.00      1.00      1.00        46
           5       0.96      0.98      0.97        47
           6       1.00      1.00      1.00        35
           7       1.00      0.97      0.99        34
           8       0.94      0.97      0.95        30
           9       0.95      0.90      0.92        40

    accuracy                           0.98       360
   macro avg       0.98      0.98      0.98       360
weighted avg       0.98      0.98      0.98       360
```
The radial SVM outperformed the linear SVM with an accuracy of 98%. The precision, recall, and f1-score for each class are high, resulting in a weighted average f1-score of 98%.

### Cross-validation:
`Cross-validation scores for Radial SVM: [0.97916667 0.98263889 0.96864111 0.98954704 0.97560976]`

The average cross-validation score for the radial SVM is 97.91%, demonstrating strong generalization performance.

## Polynomial SVM

### Parameters:
C: 100.0

Degree: 3

### Results:
```text
Classification Report for Polynomial SVM:

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        33
           1       1.00      0.96      0.98        28
           2       0.97      1.00      0.99        33
           3       1.00      1.00      1.00        34
           4       1.00      1.00      1.00        46
           5       0.94      0.96      0.95        47
           6       1.00      1.00      1.00        35
           7       0.97      0.97      0.97        34
           8       0.94      0.97      0.95        30
           9       0.89      0.85      0.87        40

    accuracy                           0.97       360
   macro avg       0.97      0.97      0.97       360
weighted avg       0.97      0.97      0.97       360
```
The polynomial SVM achieved an accuracy of 97%. While it performed well, it slightly lagged behind the radial SVM. The precision, recall, and f1-score for each class are balanced, resulting in a weighted average f1-score of 97%.

### Cross-validation:
`Cross-validation scores for Polynomial SVM: [0.97916667 0.97916667 0.95818815 0.99303136 0.96864111]`

The average cross-validation score for the polynomial SVM is 97.56%, indicating consistent performance across different data folds.

## Conclusion:
- The radial SVM with a gamma of 0.1 and C of 1000.0 achieved the highest accuracy and generalization performance in this - particular classification task.
- The linear SVM also performed well, demonstrating a good balance between simplicity and accuracy.
- The polynomial SVM, while effective, showed a slightly lower accuracy compared to the radial SVM.
