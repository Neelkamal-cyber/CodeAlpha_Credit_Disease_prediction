# 🧠 Multi-Disease Prediction Using SVM

Hi, I'm Neelkamal, and this is my machine learning project where I built a unified system to predict the likelihood of 
**heart disease**, **diabetes**, and **cancer** using Support Vector Machines (SVM). 
The goal is to apply practical ML techniques to healthcare data and assist in early diagnosis and decision-making.

---

## 🎯 Objective

To build a modular and scalable classification system that predicts whether a patient is likely to have a specific disease based on medical and lifestyle features.
This helps in proactive healthcare screening and data-driven diagnostics.

---

## 🧠 Problem Type

- **Supervised Machine Learning**
- **Binary Classification**
- **Target Variables**:  
  - Heart Disease: `target` (1 = Yes, 0 = No)  
  - Diabetes: `Outcome`  
  - Cancer: `diagnosis` or similar

---

## 📊 Features Used

Each dataset includes features relevant to its disease domain. Examples include:

| Feature                     | Why It Matters                          |
|----------------------------|------------------------------------------|
| Age, Gender                | Demographic risk factors                 |
| Blood Pressure, Cholesterol| Cardiovascular indicators                |
| Glucose Level, BMI         | Diabetes-related metrics                 |
| Tumor Size, Texture        | Cancer-specific features                 |
| Smoking, Alcohol, Stress   | Lifestyle impact                         |
| Family History             | Genetic predisposition                   |
| CRP, Homocysteine Levels   | Inflammatory markers                     |

---

## ⚙️ ML Approach

1. **Data Preprocessing**
   - Cleaned missing values
   - Encoded categorical variables
   - Scaled numerical features
   - Imputed missing entries

2. **Feature Engineering**
   - Created derived features like `MonthlyRiskScore`, `LDL/HDL Ratio`, etc.
   - Ensured consistent formatting across datasets

3. **Model Training**
   - Used `SVC` with RBF kernel for each disease
   - Wrapped models in a unified `DiseaseSVM` class

4. **Evaluation**
   - Accuracy, Precision, Recall, F1-score
   - Confusion Matrix and ROC-AUC

5. **Single-Patient Prediction**
   - Accepts a DataFrame with one patient’s data
   - Automatically aligns features and predicts disease status

---

