# Predicting Loan Defaults Using Machine Learning Models

## Overview

This project aims to forecast loan defaults using data from a peer-to-peer lending network. By accurately predicting loan defaults, lending institutions can significantly reduce their financial risk. The primary objective is to identify the most effective machine learning model based on dataset variables to predict a borrower's likelihood of default.

### Key Objectives:
- **Risk Mitigation**: Reduce financial risk for lending institutions by accurately forecasting loan defaults.
- **Model Comparison**: Evaluate and compare multiple machine learning models to determine the best predictive performance.
- **Feature Importance**: Identify key factors influencing loan defaults through advanced feature analysis.

---

## Dataset Description

The dataset used in this project includes:

- **trainData**: Contains training data with features related to borrowers and loan details.
- **testData**: Used to evaluate model performance with similar features as `trainData`.
- **varDescription**: Provides detailed descriptions of each feature in `trainData` and `testData`.

---

## Methodology

### Data Preparation
1. **Handling Missing Values**:
   - Numerical columns: Imputed missing values with the mean.
   - Categorical columns: Imputed missing values with the most frequent value.
2. **Encoding Categorical Variables**:
   - One-hot encoding was applied to convert categorical variables into numerical format.
3. **Normalizing Numerical Features**:
   - Numerical features were normalized to ensure equal contribution to the model.

### Models Implemented
1. **Linear Regression**
   - Baseline model providing a good starting point.
   - Training MSE: 0.0678 | Testing MSE: 0.0686
2. **Ridge Regression**
   - Introduces L2 regularization to address multicollinearity.
   - Best Lambda: 3.0 | Training MSE: 0.0678 | Testing MSE: 0.0686
3. **Lasso Regression**
   - Performs feature selection by shrinking coefficients to zero.
   - Training MSE: 0.0709 | Testing MSE: 0.0716
4. **Random Forest**
   - Ensemble method combining multiple decision trees.
   - Training MSE: 0.0028 | Testing MSE: 0.0204
5. **Neural Network**
   - Captures complex, non-linear relationships.
   - Training Accuracy: 0.9467 | Testing Accuracy: 0.9454

---

## Model Evaluation and Comparison

### Key Findings:
- **Random Forest** emerged as the best-performing model with the lowest Mean Squared Error (MSE) on both training and test datasets.
  - **Training MSE**: 0.0028
  - **Testing MSE**: 0.0204
  - **Strengths**:
    - Superior predictive accuracy.
    - Robust against overfitting due to its ensemble nature.
    - Provides insights into feature importance.
- **Neural Network** showed high accuracy but was slightly less effective compared to Random Forest.
  - **Training Accuracy**: 0.9467
  - **Testing Accuracy**: 0.9454
  - **Limitations**:
    - Requires longer training times and more computational resources.
    - Less interpretable than linear models.

---

## Correlation Analysis

A detailed correlation analysis was conducted to understand the relationship between features and the target variable (`loan status`). Key findings include:

- **Most Correlated Variables**:
  1. Recoveries: 0.506
  2. Interest Rate: 0.295
  3. Total Recovered Principal: 0.282
  4. Installment: 0.280
  5. Last Payment Amount: 0.260

- **Least Correlated Variables**:
  1. Employment Length: 0.015
  2. Verification Status: 0.020
  3. Home Ownership: 0.025

This analysis highlights the significance of financial metrics and payment history in predicting loan defaults.

---

## Conclusion

The **Random Forest model** was identified as the most reliable and accurate model for predicting loan defaults. Its robustness, ability to capture complex interactions, and provision of feature importance make it the ideal choice for this task.

---

## Future Improvements

To further enhance the predictive performance of the models, consider the following:
- **Advanced Imputation Techniques**: Use more sophisticated methods to handle missing data.
- **Feature Engineering**: Create new features based on domain knowledge.
- **Ensemble Methods**: Combine models to leverage their strengths.
- **Hyperparameter Tuning**: Utilise automated optimisation techniques for better model performance.

---
**Happy Coding!** 🚀
