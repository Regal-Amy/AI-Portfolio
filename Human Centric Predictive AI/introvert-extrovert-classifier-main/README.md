# Introvert vs Extrovert Personality Prediction

This project is part of the Kaggle Playground Series - Season 5, Episode 7. The goal is to predict personality type — introvert or extrovert — from anonymized tabular features using machine learning.

---

## 📌 Project Overview

We developed a neural network classifier using TensorFlow/Keras to distinguish between introverts and extroverts. The model was trained on a public dataset and evaluated on a held-out test set.

---

## 📊 Dataset

The dataset consists of anonymized features (`feature_0` to `feature_49`) and a binary target (`Personality`), where:

- `0` = Introvert
- `1` = Extrovert

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib, Seaborn
- Git, GitHub

---

## 🧪 Modeling Approach

- Stratified Train/Test Split
- Normalization using StandardScaler
- Neural Network with 3 dense layers


---

## 📈 Results

The model achieved:

- **Accuracy**: 97.1%

See `results/model_metrics.json` and `notebook/personality_prediction.ipynb` for details.

---

## 📂 Project Structure




