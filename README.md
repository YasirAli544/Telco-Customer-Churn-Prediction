# Telco Customer Churn Prediction — Data Science Project II

## 📌 Project Overview

This project predicts **customer churn** for a telecom company using machine learning. The goal is to identify customers who are likely to leave the service so the company can take preventive actions.

The project is developed **strictly according to the CS4048 Project II manual** and follows the **Machine Learning Development Life Cycle (MLDLC)**.

---

## 🧠 Problem Statement

Customer churn is a major challenge for telecom companies. This project aims to build a predictive model that can accurately identify customers who are likely to churn based on their demographic details, service usage, and billing information.

**Target Variable:** `Churn` (0 = No, 1 = Yes)

---

## 🔁 Methodology (MLDLC)

### 1️⃣ Problem Framing

* Binary classification problem
* Predict whether a customer will churn

### 2️⃣ Data Gathering

* Dataset: **Telco Customer Churn Dataset**
* Source: IBM Sample Dataset
* Total Records: 7,043

### 3️⃣ Data Preprocessing

* Converted `TotalCharges` from object to numeric
* Removed missing values
* Dropped `customerID`
* Encoded categorical variables using One-Hot Encoding
* Scaled numerical features using StandardScaler

### 4️⃣ Exploratory Data Analysis (EDA)

Key findings:

* High churn for **Month-to-month contracts**
* Higher churn for **Fiber optic** users
* Customers using **Electronic check** churn the most
* Long-term contracts reduce churn

### 5️⃣ Feature Engineering & Selection

* Logistic Regression coefficients
* Random Forest feature importance
* Key features: `tenure`, `TotalCharges`, `Contract`, `InternetService`

### 6️⃣ Model Training & Evaluation

Models used (as per manual):

* Logistic Regression (Baseline)
* Decision Tree (Unconstrained)
* Decision Tree (Pruned)
* Random Forest

**Best Model:** Logistic Regression (highest Recall)

### 7️⃣ Model Evaluation

* Confusion Matrix
* ROC Curve
* AUC Score: **0.8362**


## 📊 Results Summary

| Model               | Test Accuracy | Recall     | F1 Score |
| ------------------- | ------------- | ---------- | -------- |
| Logistic Regression | 80.31%        | **56.95%** | 0.61     |
| Random Forest       | 78.82%        | 51.33%     | 0.56     |

---

## 🛠️ Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn
* Jupyter Notebook
