# Fraud Risk Analytics & Anomaly Detection System

> **An end-to-end fraud risk analytics pipeline that identifies anomalous financial transactions using imbalance-aware machine learning, threshold optimization, and fraud-focused evaluation metrics to support risk monitoring and operational decision-making.**

---

## Project Overview

Financial institutions process millions of transactions every day, making it challenging to identify fraudulent activity while minimizing disruption to legitimate customers. Since fraudulent transactions account for less than **1%** of all transactions, conventional accuracy-based machine learning approaches are insufficient.

This project develops a fraud risk analytics pipeline that combines exploratory data analysis, imbalance-aware modeling, threshold optimization, and fraud-focused evaluation metrics to detect anomalous transactions while balancing fraud detection performance with false-positive reduction.

---

## Business Objective

Develop a fraud risk analytics pipeline capable of identifying anomalous financial transactions while balancing fraud detection performance, operational efficiency, and customer experience.

---

## Executive Summary

| Metric       | Value                         |
| ------------ | ----------------------------- |
| Dataset Size | 284,807 Transactions          |
| Fraud Cases  | 492 (<1%)                     |
| Best Model   | Threshold-Tuned Random Forest |
| Precision    | **87%**                       |
| Recall       | **75%**                       |
| F1-Score     | **80%**                       |

### Key Outcome

Threshold tuning improved **Random Forest precision from 79% to 87%**, significantly reducing false-positive fraud alerts while maintaining strong fraud detection capability.

---

## Business Questions

This analysis aims to answer the following questions:

### Risk Identification

* What characteristics distinguish fraudulent transactions from legitimate ones?
* Which transaction patterns contribute most to fraud detection?

### Operational Efficiency

* How can fraud detection performance be improved while minimizing false-positive alerts?
* Which model provides the best balance between fraud detection capability and operational cost?

### Model Performance

* How does extreme class imbalance affect model performance?
* What threshold provides the optimal trade-off between Precision and Recall?

### Business Impact

* How can threshold tuning reduce unnecessary manual investigations?
* Which model is most suitable for deployment in a real-time fraud monitoring workflow?

---

## Dataset Information

The dataset contains anonymized credit card transaction records with:

* PCA-transformed features (**V1–V28**)
* Transaction Amount
* Transaction Time
* Binary Target Variable

  * **0 → Legitimate Transaction**
  * **1 → Fraudulent Transaction**

Fraudulent transactions represent **less than 1%** of the dataset, making class imbalance one of the primary analytical challenges.

---

## Project Workflow

```
Transaction Dataset
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Data Preprocessing
        │
        ▼
SMOTE (Class Imbalance Handling)
        │
        ▼
Model Development
(Logistic Regression • Random Forest • XGBoost)
        │
        ▼
Model Evaluation
        │
        ▼
Threshold Optimization
        │
        ▼
Fraud Risk Insights
        │
        ▼
Business Recommendations
```

---

## Key Features

* Exploratory Data Analysis (EDA)
* Class imbalance handling using SMOTE
* Comparison of multiple Machine Learning models
* Threshold tuning for fraud-focused optimization
* Precision, Recall, F1-score and ROC-AUC evaluation
* Feature importance analysis
* Fraud risk insights with business recommendations

---

## Fraud Risk Insights

### Operational Insights

* Fraudulent transactions represented **less than 1%** of the dataset, confirming the need for imbalance-aware modeling.
* Threshold tuning increased **Random Forest precision from 79% to 87%**, reducing false-positive fraud alerts.
* Random Forest achieved the strongest balance between fraud detection capability (**75% recall**) and operational efficiency.

### Business Recommendations

* Prioritize high-confidence fraud alerts for manual investigation.
* Periodically recalibrate decision thresholds as fraud patterns evolve.
* Combine ML predictions with rule-based fraud monitoring systems.

### Potential Business Impact

* Reduce unnecessary manual fraud investigations through higher precision.
* Improve analyst productivity by prioritizing high-risk transactions.
* Support more reliable fraud monitoring while minimizing customer friction.

---

## Model Selection Rationale

### Threshold-Tuned Random Forest

Random Forest was selected because it achieved the strongest balance between **Precision**, **Recall**, **F1-score**, and **false-positive reduction** after threshold optimization, making it the most suitable model for fraud risk monitoring.

---

## Technology Stack

| Category                | Technologies                         |
| ----------------------- | ------------------------------------ |
| Programming Language    | Python                               |
| Data Processing         | Pandas, NumPy                        |
| Data Visualization      | Matplotlib, Seaborn                  |
| Machine Learning        | Scikit-learn, XGBoost                |
| Imbalance Handling      | SMOTE (Imbalanced-learn)             |
| Model Evaluation        | Precision, Recall, F1-score, ROC-AUC |
| Development Environment | Google Colab                         |
| Version Control         | Git, GitHub                          |

---

## Future Enhancements

* Real-time fraud transaction scoring
* Explainable AI using SHAP values
* Interactive fraud analytics dashboard
* Automated threshold optimization
* Cloud deployment for model serving
* Continuous model retraining using recent transaction data
