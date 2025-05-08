# Employee Attrition Prediction & Financial Impact Analysis

## Project Overview
This Project:
- **Classifies** which employees are at risk of attrition  
- **Regresses** next-period salary for those predicted to stay  
- **Calculates** expected salary loss due to churn  

## Data
- **Source:** IBM HR Analytics Employee Attrition CSV  
- **Size:** 1,470 rows × 35 columns  
- **Target (classification):** `Attrition` (Yes → 1, No → 0)  
- **Target (regression):** Simulated `FutureSalary` based on current income and performance rating  
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
