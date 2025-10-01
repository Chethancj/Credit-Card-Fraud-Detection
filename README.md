
---

# 2️⃣ Credit Card Fraud Detection

```markdown
# Credit Card Fraud Detection 💳

## Overview
A machine learning project to detect fraudulent credit card transactions.  
It tackles **imbalanced classification, cost-sensitive analysis, and real-time fraud simulation**.

## Dataset
- [Kaggle Credit Card Fraud Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- Transactions (features are PCA components)
- Target: `Class` (0 = Legit, 1 = Fraud)

## Workflow
1. Data Preprocessing  
   - Scale `Time` and `Amount`  
   - Train/Test split  
2. Handle Imbalance  
   - Apply SMOTE (oversampling minority class)  
3. Model Training  
   - Logistic Regression (baseline)  
   - Random Forest  
   - XGBoost  
4. Evaluation  
   - Precision, Recall, F1  
   - ROC-AUC and PR-AUC  
5. Business Impact Analysis (NEW)  
   - Cost-sensitive evaluation (£500 for missed fraud, £5 for false alarms)  
6. Real-Time Simulation (NEW)  
   - Streams transactions one by one and flags fraud instantly  

## Results
- Random Forest AUC: **~0.95**  
- Cost-sensitive analysis shows **false negatives dominate financial loss**  

## Usage
```bash
pip install -r requirements.txt
python fraud_train.py
