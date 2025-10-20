# 🎓 Predicting Student Dropout and Academic Success: A Responsible AI Approach

This project develops a **machine learning system** to predict student dropout and academic success, while ensuring **transparency, explainability, and fairness** in its predictions.

Using a real educational dataset (`Predict_Student_Dropout_and_Academic_Success.csv`), the model integrates:
- **XGBoost** for predictive performance
- **SHAP** and **LIME** for explainable AI
- **Fairlearn** for fairness auditing across sensitive groups (gender, age, nationality, etc.)

---

## 🧭 Project Motivation

Student attrition is a major challenge for universities worldwide. Predictive models can help identify at-risk students early — but if built carelessly, they can reinforce **existing inequalities**.  
This project aims to:
1. Predict **student outcomes** (Graduate, Dropout, Enrolled).  
2. Provide **transparent explanations** of each prediction.  
3. Audit and mitigate **algorithmic bias** across demographic groups.

This aligns with **Human-Centered and Responsible AI** principles by ensuring that the system is not only accurate, but also **fair and interpretable**.

---

## 📁 Dataset Overview

**Source:** [Predict Student Dropout and Academic Success Dataset (UCI Repository)](https://www.kaggle.com/datasets/syedfaizanalii/predict-students-dropout-and-academic-success)

**Shape:** 4,424 students × 37 features  
**Target classes:**  
- `Graduate` (0)  
- `Dropout` (1)  
- `Enrolled` (2)

**Feature types:**
- **Demographic:** Gender, Age, Nationality, Marital Status  
- **Academic:** Admission grade, Previous qualification  
- **Financial:** Scholarship holder, Tuition fee status, Debtor status  
- **Parental background:** Qualification and occupation  
- **Macroeconomic:** Unemployment rate, GDP, Inflation (removed to avoid leakage)

---

## 🧹 Data Preparation

### 1️⃣ Data Cleaning
- Loaded dataset with `;` delimiter  
- Verified datatypes with `df.info()`  
- Converted coded categorical columns to `category` dtype  

### 2️⃣ Feature Selection
Removed **leaky** and **irrelevant** variables:
- Semester performance metrics (`Curricular units ...`) — these leak post-enrollment data.
- Macroeconomic indicators (`GDP`, `Inflation`, `Unemployment rate`) — reflect yearly trends, not individual traits.

### 3️⃣ Target Encoding
```python
target_mapping = {"Graduate": 0, "Dropout": 1, "Enrolled": 2}
df['Target'] = df['Target'].map(target_mapping)
