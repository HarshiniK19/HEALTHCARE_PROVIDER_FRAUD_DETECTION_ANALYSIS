# HEALTHCARE PROVIDER FRAUD DETECTION ANALYSIS

This project focuses on detecting **fraudulent healthcare provider claims** using machine learning techniques.  
The goal is to build an accurate and robust model that can identify fraud early and reduce losses in the healthcare insurance system.

---

## Project Overview
- **Project Name:** Healthcare Provider Fraud Detection Analysis  
- **Dataset Name:** `Healthcare Provider Fraud Detection`  
- **Problem Type:** Binary Classification  
- **Best Model:** XGBoost (Tuned)  
- **Goal:** Detect fraudulent claims with high recall and accuracy.

---

## Dataset Description
The dataset contains details about insurance claims such as:
- `ClaimStartDt` & `ClaimEndDt` (dates of claims)
- `InscClaimAmtReimbursed` (amount reimbursed)
- `Provider` & `AttendingPhysician`
- `DiagnosisCodes`
- `PotentialFraud` (Target: 0 = Non-fraud, 1 = Fraud)

🗑 Unnecessary columns like `BeneID` and `ClaimID` were removed.

---

## Data Preprocessing
- Converted date columns to datetime and derived **claim duration**.  
- Handled missing values.  
- Encoded categorical variables.  
- Scaled numerical features.  
- Balanced data using **SMOTE** to handle class imbalance.

---

## EDA Insights
- Found strong **class imbalance** between fraud and non-fraud claims.  
- Fraudulent claims often show:
  - Unusual durations
  - High claim amounts
  - Repeated providers and physicians.
- Visualized claim amount distribution and fraud patterns.

---

## Models Trained

| Model                | Train Acc | Test Acc | Overfit | Remarks              |
|-----------------------|-----------|----------|---------|-----------------------|
| Logistic Regression   | 0.80      | 0.81     |  No   | Simple baseline       |
| KNN                   | 0.70      | 0.79     |  No   | Moderate performance  |
| Decision Tree         | 0.96      | 1.00     |  Yes  | Overfitting           |
| Random Forest         | 0.89      | 1.00     |  Yes  | Overfitting           |
| **XGBoost (Tuned)**   | **0.97**  | **0.97** |  No   | Final model  (well-generalized) |

---

## Final Model — XGBoost (Tuned)
- ✅ Accuracy: **97%**  
- ✅ Precision (Fraud): 0.99  
- ✅ Recall (Fraud): 0.93  
- ✅ F1 Score: 0.96  
- Train and test scores are well balanced.

---

## Evaluation Metrics
- Accuracy  
- Precision  
- Recall (Fraud class emphasized)  
- F1 Score  
- Confusion Matrix

---

## Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn

---
---

