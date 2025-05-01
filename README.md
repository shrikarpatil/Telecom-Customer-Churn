# 📉 Telecom Customer Churn Prediction

This project focuses on predicting customer churn in the telecom industry using machine learning. Churn prediction helps companies retain customers by identifying those likely to leave.

## 🎯 Objective

To build a reliable machine learning model that classifies customers as likely to churn or stay based on their service usage patterns, payment behavior, and demographics.

---

## 📁 Dataset

- **Source:** Publicly available telecom dataset
- **Target Variable:** `Churn` (binary classification)
- **Features:** Customer tenure, service subscriptions, payment methods, and more
- **Size:** ~7,000 rows and 20+ columns

---

## 🧰 Tools & Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- imbalanced-learn (SMOTE)
- Matplotlib, Seaborn

---

## 🔧 Workflow

1. **Data Preprocessing**
   - Missing value handling
   - Data type conversions
   - Encoding categorical variables
   - Feature scaling

2. **Feature Engineering**
   - Contract duration analysis
   - Tenure segmentation
   - Combined streaming and security service features

3. **Imbalanced Class Handling**
   - Applied SMOTE to oversample the minority class (Churn = Yes)

4. **Model Building**
   - Trained base models: Logistic Regression, Random Forest, XGBoost
   - Built Stacking Classifiers with multiple final estimators

5. **Evaluation Metrics**
   - Accuracy
   - Precision, Recall, F1-score
   - Confusion Matrix
   - ROC AUC Score

---

## 🧠 Model Performance: Stacking Classifier

| **Final Estimator**    | **Accuracy** | **Precision (Churn = 1)** | **Recall (Churn = 1)** | **F1-Score (Churn = 1)** | **ROC AUC** |
|------------------------|--------------|----------------------------|------------------------|--------------------------|-------------|
| Logistic Regression     | 76.29%       | 0.55                       | 0.61                   | 0.58                     | 0.83        |
| Random Forest           | **81.26%**   | **0.68**                   | 0.55                   | 0.61                     | **0.86**    |
| XGBoost                 | 80.98%       | 0.67                       | 0.55                   | 0.61                     | 0.84        |

✅ **Best Final Estimator:** Random Forest (highest accuracy and ROC AUC)

---

## 📌 Insights

- Longer contracts and higher tenure reduce churn likelihood.
- SMOTE improved the model's ability to detect churners.
- Ensemble (stacking) models outperform standalone classifiers.
