

# 🔬 Dry Eye Disease Prediction: A Comparative Study of MLP and Logistic Regression  

This project leverages **supervised machine learning** to predict **Dry Eye Disease (DED)** using **Logistic Regression** and **Multilayer Perceptron (MLP)** on a dataset of **20,000 health records**. The goal is to support **clinical decision-making** and **automated screening**.  

---

## 📊 Dataset & Preprocessing  

- **Features:** Age, Gender, Sleep quality, Screen time, Heart rate, Ocular symptoms, etc.  
- **Target:** Binary classification (1 = DED, 0 = No DED)  
- **Preprocessing:**  
  ✅ Imputation (median/mode)  
  ✅ Encoding categorical variables  
  ✅ StandardScaler normalization  
  ✅ Addressing class imbalance (SMOTE, class weighting)  

---

## 🔍 Feature Selection  

Feature selection was performed to **enhance model accuracy**, **reduce overfitting**, and **improve interpretability**.  

### 🔹 **Categorical Feature Selection**  
- **Chi-Square Test**: Identified categorical variables significantly associated with DED.  
- **Histogram & KDE Plots**: Evaluated distribution of categorical features for different target classes.  
- **Selected Features:**  
  ✅ **Gender** – Population-level variability in DED susceptibility  
  ✅ **Eye strain, Redness, Irritation** – Strong indicators of DED  

### 🔹 **Numerical Feature Selection**  
- **ANOVA F-test**: Identified features with significant variance across target classes.  
- **Mutual Information (MI)**: Measured correlation between numerical variables and DED occurrence.  
- **Box Plots & KDE Distributions**: Visualized feature separation for better model interpretability.  
- **Selected Features:**  
  ✅ **Screen time** – Strongest predictor, linked to digital eye strain  
  ✅ **Age** – Older individuals show higher susceptibility  
  ✅ **Sleep quality & Stress level** – Impacts tear production and eye health  
  ✅ **Daily steps** – Indicator of overall physical health  

📌 **These selected features improve the model’s predictive power while ensuring interpretability in clinical applications.**  

---

## 📈 Exploratory Data Analysis (EDA)  

EDA identified **key predictors** using:  
🔹 **Chi-Square Test** (categorical importance)  
🔹 **ANOVA F-test & Mutual Information** (numerical features)  
🔹 **KDE plots, Box plots, Heatmaps**  

📌 **Top predictors:** Screen time, Eye strain, Sleep quality, Age, Stress level  

---

## 🧠 Machine Learning Models  

### 🔹 Logistic Regression  
✔ **Accuracy:** 65.25%  
✔ **Recall (DED):** 0.81 | **F1-score:** 0.76 | **AUC-ROC:** 0.58  
✔ Balanced class weight | L2 regularization  
✔ **Highly interpretable** – ideal for **clinical use**  

### 🔹 Multilayer Perceptron (MLP)  
✔ **Accuracy:** 65.57%  
✔ **Recall (DED):** 0.93 | **F1-score:** 0.81 | **AUPRC:** 0.71  
✔ SMOTE for class balancing | **Dropout & Early Stopping** for regularization  
✔ **Better sensitivity & generalization** – ideal for **automated screening**  

---

## 📊 Model Comparison  

| Metric         | Logistic Regression | MLP  |  
|---------------|--------------------|------|  
| **Accuracy**  | 65.25%  | 65.57%  |  
| **Recall (DED)** | 0.81  | **0.93**  |  
| **F1-score (DED)** | 0.76  | **0.81**  |  
| **ROC-AUC**  | 0.58  | 0.57  |  
| **AUPRC**  | 0.67  | **0.71**  |  
| **Interpretability**  | ⭐⭐⭐⭐⭐  | ⭐⭐  |  

📌 **MLP** excels in **sensitivity & recall**, while **Logistic Regression** is preferred for **clinical interpretability**.  

---

## 🚀 Future Enhancements  
✔ **Integrate real-time patient monitoring**  
✔ **Explore ensemble models (Random Forest, Gradient Boosting)**  
✔ **Improve feature selection & class balancing**  

---

## 👩‍💻 About Me  
**Aarthi Vijayaragavan**  
🎓 MSc Data Analytics – National College of Ireland  
📫 **Email:** x23438533@student.ncirl.ie  

