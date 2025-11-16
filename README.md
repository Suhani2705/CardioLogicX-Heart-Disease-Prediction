# CardioLogicX ❤️– Heart Disease Prediction

CardioLogicX is an explainable machine-learning system designed to predict **Heart Disease** using a stacking ensemble model.  
The project integrates strong preprocessing, ENN-based noise removal, and transparent AI through **LIME** and **SHAP**.

---

## 📌 Dataset

This project uses the **Heart Disease Dataset** from Kaggle:  
🔗 https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

The dataset contains demographic + clinical ECG features.  
Target variable: **HeartDisease (0 = No, 1 = Yes)**.

### 📁 Dataset File in This Repository
Click to view:  
➡️ **[`heart.csv`](heart.csv)**

---

## 📂 Repository Contents

| File | Description |
|------|-------------|
| **[`heart.csv`](heart.csv)** | The dataset used for model training |
| **[`heart_data_analysis.ipynb`](heart_data_analysis.ipynb)** | Exploratory Data Analysis (EDA) |
| **[`CardioLogicX_HeartDisease_Prediction.ipynb`](CardioLogicX_HeartDisease_Prediction.ipynb)** | ENN + Preprocessing + Stacking Model + LIME + SHAP |
| **README.md** | Project Overview |
| **requirements.txt** | List of required Python packages |

---

## 🚀 Project Workflow

### **1. Data Preprocessing**
- Encode categorical features  
- Standardize numeric features (Z-score)  
- Remove ambiguous samples using **Edited Nearest Neighbours (ENN)**  

### **2. CardioLogicX Model (Stacking Ensemble)**  
Base learners:
- CatBoost  
- ExtraTrees  
- AdaBoost  
- XGBoost  
- MLP Neural Network  

**Meta-learner:** RandomForestClassifier  

### **3. Model Evaluation**
- Accuracy  
- Precision, Recall, F1  
- ROC Curve (AUC)  
- Specificity  
- Log Loss  
- Confusion Matrix  


---
## 🧠 Explainable AI (XAI)

| Method | Purpose | What It Shows |
|--------|---------|----------------|
| **SHAP** (SHapley Additive exPlanations) | Global + local interpretability | Feature contribution, waterfall plots, summary plots |
| **LIME** (Local Interpretable Model-Agnostic Explanations) | Local interpretability | Top features influencing a single prediction |

---


## ▶️ How to Run

Install dependencies:

```bash
pip install -r requirements.txt
