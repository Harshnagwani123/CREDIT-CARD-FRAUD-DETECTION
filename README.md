# CREDIT-CARD-FRAUD-DETECTION

# 💳 Credit Card Fraud Detection (Machine Learning Project)

## 📌 Project Overview
Credit card fraud is a serious problem worldwide. In this project, we use **Machine Learning models** to detect fraudulent transactions.  
The dataset is highly **imbalanced** (fraud cases are very rare), so we apply **cross-validation, ensemble methods, and evaluation metrics** that handle imbalance.

---

## 📂 Dataset
- Source: [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- 284,807 transactions  
- 492 frauds (≈0.17%)  
- Features are **anonymized PCA components** + `Time`, `Amount`  
- Target: `Class` (0 → Normal, 1 → Fraud)

---

## ⚙️ Steps / Workflow
### 1. Data Loading & Preprocessing
- Load CSV using pandas  
- Handle imbalance using **stratified train-test split**  
- Scale `Amount` & `Time`  
- Pipeline for preprocessing  

### 2. Exploratory Data Analysis (EDA)
- Fraud ratio visualization  
- Distribution of features (`Amount`, `Time`)  
- Correlation heatmap  

### 3. Modeling
We implemented and compared different ML models:
- ✅ **Logistic Regression (Baseline)**  
- 🌳 **Random Forest (Optimized with GridSearchCV)**  
- ⚡ **XGBoost & AdaBoost**  

All models were wrapped in a **Pipeline + Cross-Validation** setup.

### 4. Model Evaluation
Since the dataset is **imbalanced**, we use:
- **ROC-AUC** (Receiver Operating Curve)  
- **PR-AUC** (Precision-Recall Curve, more relevant for imbalance)  
- **Confusion Matrix**  

### 5. Results
| Model              | ROC-AUC | PR-AUC |
|---------------------|---------|--------|
| Logistic Regression | 0.97    | 0.65   |
| Random Forest       | 0.99    | 0.85   |
| XGBoost             | 0.99+   | 0.87   |
| AdaBoost            | 0.98    | 0.82   |

*(values are indicative, will vary with runs)*

---

## 📊 Feature Engineering
- StandardScaler applied to `Amount`, `Time`  
- Feature importance extracted from **Random Forest** & **XGBoost**  

---

## 🚀 How to Run
1. Clone repo  
   ```bash
   git clone https://github.com/your-username/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
