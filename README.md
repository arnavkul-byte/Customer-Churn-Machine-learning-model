# Telco Customer Churn Prediction

## Project Overview

This project analyzes and predicts customer churn for a telecommunications company using the [WA_Fn-UseC_-Telco-Customer-Churn.csv][1] dataset. The goal is to identify customers likely to leave the service, enabling proactive retention strategies.

---

## Dataset Summary

- **Source:** Telco Customer Churn public dataset  
- **Rows:** 7,043 customers  
- **Target:** `Churn` (Yes/No)  
- **Features:**  
  - **Demographics:** gender, SeniorCitizen, Partner, Dependents  
  - **Account info:** tenure, Contract, PaperlessBilling, PaymentMethod  
  - **Services:** PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies  
  - **Charges:** MonthlyCharges, TotalCharges

---

## Workflow

### 1. Data Preprocessing
- Handled missing values and converted data types.
- Encoded categorical variables (binary and one-hot encoding).
- Engineered features (e.g., tenure groups, total spend).
- Scaled numerical features.
- Addressed class imbalance using SMOTE and class weights.

### 2. Model Building
- **Neural Network:**  
  - Multi-layer perceptron with dropout regularization.
  - Tuned architecture and hyperparameters.
- **Random Forest:**  
  - Used scikit-learn’s RandomForestClassifier with class weighting.
  - Compared performance with neural network.

### 3. Evaluation
- Split data into training and test sets (80/20).
- Tracked metrics: **Precision, Recall, F1 Score, Accuracy, AUC**.
- Sampled and compared model predictions to actual churn outcomes.

### 4. Results
- **Neural Network Final Scores:**
  - Precision: ~0.64
  - Recall: ~0.51
  - F1 Score: ~0.57
- **Random Forest:** Similar or slightly better performance, depending on tuning.
- **Interpretation:**  
  - The model identifies more than half of actual churners with reasonable precision, providing actionable insights for retention teams.

### 5. Sampling and Validation
- Sampled random customers from the test set.
- Displayed predicted churn, probability, and actual churn status for transparency.
