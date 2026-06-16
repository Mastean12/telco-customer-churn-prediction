# Customer Churn Prediction

## Project Overview

This project develops machine learning classification models to predict customer churn using the IBM Telco Customer Churn Dataset.

Customer churn prediction is a critical business problem because retaining existing customers is significantly less expensive than acquiring new ones. The goal of this project is to identify customers who are likely to leave a service and understand the factors influencing churn behavior.

The project compares Decision Tree and Random Forest classifiers while evaluating performance using industry-standard classification metrics.

---

## Business Problem

Customer churn occurs when customers stop using a company's products or services.

For subscription-based businesses such as telecommunications companies, streaming platforms, and SaaS providers, predicting churn enables proactive customer retention strategies.

This project answers:

> Can we predict whether a customer is likely to churn based on demographic information, service subscriptions, contract type, and billing history?

---

## Dataset

Dataset: IBM Telco Customer Churn Dataset

### Features

Examples include:

- Gender
- Senior Citizen Status
- Partner
- Dependents
- Tenure
- Internet Service
- Online Security
- Contract Type
- Payment Method
- Monthly Charges
- Total Charges

### Target Variable

| Value | Meaning |
|---------|---------|
| 0 | Customer Stayed |
| 1 | Customer Churned |

Dataset Shape:

```text
7043 Rows × 21 Columns
```

---

## Project Workflow

### 1. Data Loading

- Loaded customer churn dataset
- Inspected data structure and feature types

### 2. Exploratory Data Analysis

Performed:

- Dataset inspection
- Missing value analysis
- Churn distribution analysis
- Contract type analysis
- Tenure analysis
- Monthly charges analysis

### Key Insights

- Approximately 26.5% of customers churned.
- Month-to-month customers exhibited significantly higher churn rates.
- Customers with shorter tenure were more likely to churn.
- Higher monthly charges were associated with increased churn.

### 3. Data Cleaning

- Converted TotalCharges to numeric format.
- Handled missing values.
- Removed customerID.
- Encoded categorical variables using one-hot encoding.

### 4. Feature Engineering

- Created machine-learning-ready dataset.
- Converted target variable into binary format.

### 5. Train-Test Split

Dataset split:

- Training Data: 80%
- Testing Data: 20%

### 6. Decision Tree Classification

Implemented:

```python
DecisionTreeClassifier()
```

Evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### 7. Random Forest Classification

Implemented:

```python
RandomForestClassifier()
```

Compared performance against the Decision Tree model.

### 8. Feature Importance Analysis

Used Random Forest feature importance scores to identify key factors driving customer churn.

---

## Model Performance

### Decision Tree Classifier

| Metric | Score |
|----------|----------|
| Accuracy | 70.97% |
| Precision | 45.19% |
| Recall | 45.31% |
| F1 Score | 45.25% |

Confusion Matrix:

```text
[[831 205]
 [204 169]]
```

---

### Random Forest Classifier

| Metric | Score |
|----------|----------|
| Accuracy | 78.92% |
| Precision | 64.29% |
| Recall | 45.84% |
| F1 Score | 53.52% |

Confusion Matrix:

```text
[[941 95]
 [202 171]]
```

---

## Feature Importance

Top predictors of churn:

| Feature | Importance |
|----------|----------|
| TotalCharges | 0.1897 |
| tenure | 0.1757 |
| MonthlyCharges | 0.1724 |
| InternetService_Fiber optic | 0.0361 |
| PaymentMethod_Electronic check | 0.0353 |
| Contract_Two year | 0.0304 |

---

## Key Findings

### Customers More Likely to Churn

- Month-to-month contract holders
- Customers with shorter tenure
- Customers with higher monthly charges
- Customers using electronic check payment methods

### Customers Less Likely to Churn

- Long-term customers
- Two-year contract customers

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

---

## Machine Learning Concepts Demonstrated

- Classification
- Decision Trees
- Random Forests
- Feature Importance
- Exploratory Data Analysis
- Data Cleaning
- One-Hot Encoding
- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---

## Future Improvements

Potential enhancements include:

- Hyperparameter tuning using GridSearchCV
- ROC-AUC analysis
- XGBoost
- LightGBM
- Class imbalance handling techniques
- Customer retention recommendation system

---

## Author

Stephen

AI Engineering & Machine Learning Portfolio Project

Focused on Machine Learning, Data Science, AI Systems Development, and Applied Artificial Intelligence.
