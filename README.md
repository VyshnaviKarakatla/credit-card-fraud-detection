# Credit Card Fraud Detection

A Machine Learning project that detects fraudulent transactions using Logistic Regression, scaling, and threshold tuning.  
The model is designed to **maximize recall**, ensuring that fraudulent transactions are never missed.

---

##  Project Summary

Credit card fraud is rare and highly dangerous.  
Out of 2,84,807 transactions, only **0.17 percent** are fraud.

A normal model would achieve **99.8 percent accuracy** by always predicting **Not Fraud**, which is useless.

This project focuses on:
- Handling imbalanced data  
- Improving fraud detection accuracy  
- Using probability thresholds instead of default predictions  
- Achieving **maximum recall**  

---

##  Dataset

Source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Contains:
- Features: V1–V28 (PCA Components)  
- Amount  
- Time  
- Target: `Class`  
  - 0 → Normal  
  - 1 → Fraud  

---

##  Machine Learning Workflow

### ✔ 1. Data Cleaning  
- Removed duplicates  
- Verified no missing values  

### ✔ 2. Preprocessing  
- Feature/target separation  
- StandardScaler applied  
- Stratified train-test split  

### ✔ 3. Model  
Algorithm used:  
**Logistic Regression with class_weight="balanced"**

Why?  
- Works well on imbalanced datasets  
- Fast and interpretable  
- Handles fraud detection effectively  

### ✔ 4. Threshold Tuning  
Instead of using default 0.5 threshold,  
the model tested thresholds from **0.001 to 0.20**.

### ✔  Final Optimal Threshold = **0.001**  
This threshold produced:

- **Recall = 1.0 (100 percent frauds detected)**  
- False negatives = 0  
- Higher false positives (expected, acceptable in fraud detection)  


##  Project Structure

