# CardioLogicX – Heart Disease Prediction

CardioLogicX is an explainable machine-learning system designed to predict **Heart Disease** using a stacking ensemble model.  
The project integrates strong preprocessing, ENN-based noise removal, and transparent AI through **LIME** and **SHAP**.

---

## 📌 Dataset

This project uses the **Heart Disease Dataset** published on Kaggle:  
🔗 **https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction**

The dataset contains patient demographic, clinical, and ECG-related features.  
Target variable: **HeartDisease (0 = No, 1 = Yes)**.

The file included in this repo (`heart.csv`) is sourced from the above dataset.

---

## 📂 Repository Contents

heart.csv
heart_data_analysis.ipynb → Exploratory Data Analysis (EDA)
CardioLogicX_HeartDisease_Prediction.ipynb → Preprocessing + ENN + Stacking Model + LIME + SHAP
README.md
requirements.txt



---

## 🚀 Project Workflow

### **1. Data Preprocessing**
- Encode categorical features  
- Standardize numeric features (Z-score)  
- Remove noisy/ambiguous samples using **Edited Nearest Neighbours (ENN)**  

### **2. CardioLogicX Model (Stacking Ensemble)**  
Base learners:
- CatBoost  
- ExtraTrees  
- AdaBoost  
- XGBoost  
- MLP Neural Network  

**Meta-learner:** RandomForestClassifier  

### **3. Model Evaluation**
Includes:
- Accuracy  
- Precision, Recall, F1  
- ROC Curve & AUC  
- Specificity  
- Log Loss  
- Confusion Matrix  

---

## 🧠 Explainable AI (XAI)

### 🔵 **SHAP (SHapley Additive exPlanations)**
SHAP is a game-theory–based explainability method that provides:
- **Exact contribution of each feature** to a prediction  
- **Waterfall plots** showing how features push the prediction ↑ or ↓  
- **Summary plots** to show global impact across all patients  
- SHAP also explains the **meta-learner** (stacking) in this project  

SHAP helps answer **“Why did the model predict Heart Disease for this patient?”**

---

### 🟩 **LIME (Local Interpretable Model-Agnostic Explanations)**
LIME explains **single predictions** by approximating the local decision boundary.  
It highlights the **top features** influencing the final output for each patient.

LIME helps answer **“Which features mattered most for this specific prediction?”**

---
