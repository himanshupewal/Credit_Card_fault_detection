

# `Credit Card Fraud Detection`

## Business Understanding

Credit Card Fraud Detection is a critical task in the finance industry, characterized by a class-imbalance problem where fraudulent transactions are significantly outnumbered by legitimate ones. Traditional approaches often result in models that overfit to the majority class (legitimate transactions), failing to generalize well to new, unseen data. Therefore, this problem is treated as an anomaly detection issue, aiming to accurately identify fraudulent transactions while minimizing false positives.


### Dataset Overview

The dataset used for this project is the [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud).

- **Features:**
  - **V1-V28:** Anonymized numerical features resulting from PCA transformation due to confidentiality.
  - **Time:** The seconds elapsed between each transaction and the first transaction in the dataset.
  - **Amount:** Transaction amount.
  
- **Target Variable:**
  - **Class:** Binary variable indicating whether the transaction is fraudulent (1) or legitimate (0).

### Data Characteristics

- **No Missing Values:**
  - The dataset does not contain any missing values, which simplifies preprocessing steps.

- **Numerical Features:**
  - All input features (V1-V28, Time, Amount) are numerical, facilitating direct use in machine learning models.

### Handling Class Imbalance

To address the class imbalance problem:
- **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to generate synthetic samples of the minority class (fraudulent transactions), thereby balancing the dataset. This approach helps in training the model effectively on both classes without bias towards the majority class.




## Overview

This project aims to detect fraudulent credit card transactions using machine learning techniques. Given the highly imbalanced nature of the dataset, techniques like SMOTE (Synthetic Minority Over-sampling Technique) were applied to balance the data. Exploratory Data Analysis (EDA) was performed to understand dataset characteristics and relationships between variables.


## Model Training and Evaluation

Three classifiers were trained and evaluated:

1. **Logistic Regression**
2. **Random Forest**
3. **XGBoost**
4. **SGDClassifier**
### Evaluation Metrics

- **Confusion Matrix and F1-Score**:
  - Random Forest: F1-Score of 0.8797.
  - XGBoost: F1-Score of 0.8678.
  
  Random Forest outperformed XGBoost in achieving a better balance between precision and recall for identifying fraudulent transactions.

- **Area Under the ROC Curve (AUC-ROC)**:
  - Random Forest: AUC-ROC score of 0.99.
  - XGBoost: AUC-ROC score slightly lower at 0.99.
  
  Both models performed exceptionally well in distinguishing between fraudulent and legitimate transactions.

- **Accuracy**:
  - Random Forest: Accuracy of 99.96%.
  - XGBoost: Accuracy of 99.95%.
  
  Both models demonstrated high accuracy rates with minimal prediction errors.

## Conclusion

Based on the evaluation metrics, particularly the F1-Score and AUC-ROC, the **Random Forest** model is recommended for credit card fraud detection in this scenario. However, both Random Forest and XGBoost classifiers proved effective in identifying fraudulent transactions with high accuracy and minimal false alarms.
