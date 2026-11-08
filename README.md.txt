# NSP1 Machine Learning Assignment 2

## a. Problem Statement
The objective of this assignment is to implement, evaluate, and deploy five distinct machine learning classification models using an end-to-end workflow (modeling, evaluation, UI design via Streamlit, and cloud deployment). The task solves a binary classification problem to predict whether a breast cancer tumor is malignant or benign based on cell nuclei characteristics.

## b. Dataset Description
- **Dataset Name:** Breast Cancer Wisconsin (Diagnostic) Dataset (Public Repository: UCI / Scikit-Learn)
- **Total Instances:** 569 samples (Exceeds minimum requirement of 500)
- **Total Features:** 30 numerical features computed from digitized images of fine needle aspirates (FNAs) of breast masses (Exceeds minimum requirement of 12 features)
- **Target Variable:** Binary classification (0 = Malignant, 1 = Benign)

## c. GitHub Repository Link
[Insert Your GitHub Repository URL Here]

## d. Models Used & Comparison Table

| ML Model Name | Accuracy | AUC | Precision | Recall | F1 | MCC |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Logistic Regression** | 0.9737 | 0.9925 | 0.9722 | 0.9859 | 0.9790 | 0.9427 |
| **Decision Tree** | 0.9298 | 0.9234 | 0.9420 | 0.9437 | 0.9428 | 0.8427 |
| **KNN** | 0.9386 | 0.9748 | 0.9315 | 0.9718 | 0.9512 | 0.8601 |
| **Naive Bayes** | 0.9386 | 0.9832 | 0.9444 | 0.9577 | 0.9510 | 0.8603 |
| **Support Vector Machine** | 0.9649 | 0.9902 | 0.9589 | 0.9859 | 0.9722 | 0.9224 |

### Observations on Model Performance
| ML Model Name | Observation about Model Performance |
| :--- | :--- |
| **Logistic Regression** | Achieved the highest overall accuracy and MCC score after feature scaling. Converged rapidly with exceptionally high precision and recall, proving well-suited for linear boundaries in high-dimensional biological data. |
| **Decision Tree** | Prone to slight variance, resulting in lower accuracy compared to linear and distance-based models. Captured non-linear splits well but showed minor overfitting on training splits. |
| **KNN** | Performed strongly after standard scaling of features. Relies heavily on proximity measures, achieving robust recall though slightly lower precision than Logistic Regression. |
| **Naive Bayes** | Performed reliably given the conditional independence assumption. Generated an impressive AUC score due to well-calibrated probability distributions. |
| **Support Vector Machine** | Second-best performing model overall. Leveraged the RBF kernel effectively to capture complex margin separations, matching Logistic Regression in recall. |

**Overall Winner:** **Logistic Regression** achieved the highest accuracy ($97.37\%$) and Matthews Correlation Coefficient ($0.9427$) on this dataset, striking an optimal balance between precision and recall.