# Employee Attrition Prediction & Financial Impact Analysis

> **100% work done by K. Pranav Suhas Reddy**

## Project Overview
This project:
- **Classifies** which employees are at risk of attrition  
- **Regresses** next-period salary for those predicted to stay  
- **Calculates** expected salary loss due to churn  

All source code, Jupyter notebook, final report, and dataset are included in this repo.

## Data
- **Dataset (included):** `/WA_Fn-UseC_-HR-Employee-Attrition.csv`  
- **Size:** 1,470 rows × 35 columns  
- **Classification target:** `Attrition` (Yes → 1, No → 0)  
- **Regression target:** Simulated `FutureSalary` based on current income & performance rating  
- **Dropped columns:** `EmployeeCount`, `EmployeeNumber`, `Over18`, `StandardHours`

## Models
### Classification
- Logistic Regression  
- Decision Tree  
- Support Vector Machine  
- Random Forest  
- XGBoost  
- **Voting Classifier** (ensemble of LR, RF, XGB)

### Regression
- Random Forest Regressor  
- Ridge Regression  
- Lasso Regression  
- Support Vector Regressor  
- XGBoost Regressor  
- **Voting Regressor** (ensemble of RF, Ridge, Lasso, XGB)

## Results
- **Best Classifier (Voting):**  
  - Accuracy: 0.8673  
  - ROC-AUC: 0.7940  
  - F1 (weighted): 0.8709  

- **Best Regressor (Voting):**  
  - R²: 1.0000  
  - RMSE: 73.02  
  - MAPE: 0.0120  

- **Expected Salary Loss:**  
  - Total: \$3,261,024.27  
  - “Likely-to-Stay” subset: \$1,127,966.68  

## Libraries
- Python 3.8+  
- pandas, numpy  
- scikit-learn  
- xgboost  
- imbalanced-learn (SMOTE)  
- matplotlib, seaborn  
