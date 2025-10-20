# 🎓 Predicting Student Dropout and Academic Success: A Responsible AI Approach

This project applies **machine learning, explainable AI, and fairness auditing** to predict student dropout and academic success using the *Predict Student Dropout and Academic Success* dataset.  
It demonstrates how AI systems can be designed to be both **accurate and responsible**, aligning with human-centered and ethical AI principles.

---

## 🧭 Overview

The goal is to identify students at risk of dropping out based on pre-enrollment data while ensuring that model predictions are **transparent and fair** across demographic groups.

### Key Objectives
- Build a predictive model for student outcomes (Graduate, Dropout, Enrolled).  
- Use **SHAP** and **LIME** to explain how features influence predictions.  
- Conduct a **Fairlearn audit** to assess potential bias across gender, age, nationality, and other sensitive attributes.

---

## ⚙️ Methods

- **Model:** XGBoost Classifier  
- **Explainability:** SHAP (global feature importance) and LIME (individual prediction insight)  
- **Fairness Framework:** Fairlearn MetricFrame for disparity analysis  
- **Sensitive Attributes:** Gender, Age, Nationality, International status, Displacement, and Educational special needs  

---

## 📊 Results Summary

| Aspect | Key Findings |
|--------|---------------|
| **Model Accuracy** | ~60% overall |
| **Top Predictors** | Tuition fees up to date, Scholarship holder, Admission grade, Parental qualification |
| **Insight** | Financial and academic factors dominate predictions; may reflect structural inequities |
| **Bias Findings** | Disparities observed across age, gender, and international status |
| **Interpretability** | SHAP and LIME clarify why specific predictions are made, supporting human understanding and accountability |

---

## ⚖️ Responsible AI Insights

Even after removing explicit sensitive features, the model exhibits **proxy bias**, where neutral-looking variables (e.g., parental occupation, financial status) indirectly encode disadvantage.  
This highlights the importance of **auditing, transparency, and iterative model refinement** before deploying predictive systems in education.

---

## 🧩 Future Work

- Apply bias mitigation strategies (reweighting, fairness constraints).  
- Explore causal reasoning to distinguish correlation from discrimination.  
- Develop interactive dashboards for explainability and fairness tracking.

---

## 🛠️ Tools & Libraries

`Python · Pandas · Scikit-learn · XGBoost · SHAP · LIME · Fairlearn · Matplotlib · Seaborn`

---

## 👩🏽‍💻 Author

**Amirat Abdulsalam**  
*MPhil in Human-Inspired AI, University of Cambridge*  
Focus: Responsible AI · Human-Centered Machine Learning · Algorithmic Fairness

---

## 📜 License

Released under the [MIT License](LICENSE).

