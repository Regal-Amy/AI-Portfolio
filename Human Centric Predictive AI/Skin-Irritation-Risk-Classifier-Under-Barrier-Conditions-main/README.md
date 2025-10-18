# 🧪 Skin Irritation Risk Classifier Under Barrier Conditions

A machine learning project that predicts the likelihood of skincare ingredient-induced irritation when used under occlusive or barrier-like conditions (e.g., makeup, patches, masks). This is crucial for improving skincare safety and guiding formulation development, especially for acne-prone or sensitive skin.

## 🌟 Project Overview

This project leverages structured ingredient data from the SkinSort database (19,000+ cosmetic ingredients) to build a predictive model for skin irritation risk. We enhance the dataset with inferred values for occlusivity, comedogenicity, and irritation potential using rules derived from public cosmetic science resources.

### ✅ Goals

- Predict if a skincare ingredient is **likely to cause irritation under barrier conditions**.
- Enrich raw INCI ingredient data with estimated **occlusivity**, **comedogenicity**, and **irritation scores**.
- Provide a useful reference for **formulators**, **skincare consumers**, and **AI-aided product design tools**.

---

## 🧾 Dataset

- **Source**: [SkinSort 19,000+ Ingredients Dataset]([https://skinsort.com/ingredients](https://www.kaggle.com/datasets/kazireyazulhasan/19000-skincare-products-database-of-skinsort)
- **Source**: [Sephora Skincare Ingredient](https://www.kaggle.com/datasets/dominoweir/skincare-product-ingredients)
- **Format**: CSV file containing INCI names and ingredient metadata.
- **Columns used/generated**:
  - `INCI Name`
  - `Function Type` (e.g., emollient, preservative)
  - `Chemical Type` (e.g., alcohol, ester)
  - `Predicted_Occlusivity`
  - `Predicted_Comedogenicity`
  - `Predicted_IrritationRisk`
  - `Irritation_Under_Barrier` *(Target variable)*

I used custom rule-based logic (Python functions) to estimate the above predictive features based on chemical and functional type.

---

## 🔍 Methodology

### 1. **Data Preprocessing**
- Cleaned and filtered the dataset to remove missing INCI entries.
- Mapped occlusivity and comedogenicity scores using custom logic.

### 2. **Feature Engineering**
- Derived binary features for barrier-related irritation risk using:
  - Comedogenic potential
  - Occlusivity level
  - Known irritant functions (e.g., alcohols, essential oils)

### 3. **Model Training**
- Model used: **Random Forest Classifier**
- Reason: Good interpretability, handles class imbalance, and works well on tabular data.
- Train-test split: 80/20
- Evaluation metrics: Accuracy, Precision, Recall, F1 Score

---

## 📈 Results

- **Model**: RandomForestClassifier 
- **AVG Accuracy**: ~99% 
- Good performance in identifying high-risk ingredients.
- 

---

## 📂 Repository Structure

