# 🔬 Dry Eye Disease Prediction: A Comparative Study of MLP and Logistic Regression

This project uses supervised machine learning models to predict **Dry Eye Disease (DED)** from a dataset of 20,000 health, behavioral, and physiological records. It compares the performance of **Logistic Regression** and **Multilayer Perceptron (MLP)** to support both clinical decision-making and automated screening tools.

---

## 📊 Dataset

The dataset contains 25 features collected through health and lifestyle surveys, including:

- **Demographics**: Age, Gender
- **Lifestyle & Behavioral**: Caffeine/Alcohol/Smoking use, Sleep quality, Screen time
- **Physiological**: Blood pressure, Heart rate, Weight, Height, Daily steps
- **Ocular Symptoms**: Redness, Eye strain, Irritation
- **Target**: Binary value indicating presence (1) or absence (0) of Dry Eye Disease

### Data Preprocessing

- Imputation for missing values (median/mode)
- Label encoding and one-hot encoding for categorical variables
- StandardScaler used for numerical normalization
- Class imbalance addressed using SMOTE and class weighting

---

## 📈 Exploratory Data Analysis (EDA)

Performed to identify strong predictors and eliminate noise:

- **Chi-Square Test** for categorical feature importance
- **ANOVA F-test** and **Mutual Information** for numerical features
- **Visualizations**: KDE plots, Box plots, Heatmaps
- **Key features**: Screen time, Eye strain, Sleep quality, Age, Stress level

---

## 🧠 Machine Learning Models

### 🔹 Logistic Regression

- **Accuracy**: 65.25%
- **Recall (DED)**: 0.81
- **F1-score (DED)**: 0.76
- **AUC-ROC**: 0.58
- Class weight balanced, L2 regularization
- Highly interpretable – suitable for clinical decision support

### 🔹 Multilayer Perceptron (MLP)

- **Accuracy**: 65.57%
- **Recall (DED)**: 0.93
- **F1-score (DED)**: 0.81
- **AUPRC**: 0.71
- Used SMOTE for class balancing
- Optimizer: Adam | Loss: Binary Crossentropy | Regularization: Dropout + Early Stopping

> MLP achieved better sensitivity and generalization, while Logistic Regression offered clinical interpretability.

---

## 📊 Results Summary

| Metric                  | Logistic Regression | MLP             |
|-------------------------|---------------------|-----------------|
| Accuracy                | 65.25%              | 65.57%          |
| Recall (DED)            | 0.81                | 0.93            |
| F1-score (DED)          | 0.76                | 0.81            |
| ROC-AUC                 | 0.58                | 0.57            |
| AUPRC                   | 0.67                | 0.71            |
| Interpretability        | ⭐⭐⭐⭐⭐              | ⭐⭐             |

---

## 👩‍💻 About Me
Aarthi Vijayaragavan
🎓 MSc Data Analytics – National College of Ireland
📫 Email: x23438533@student.ncirl.ie
