<div align="center">

# 🩺 Diabetes Prediction using Machine Learning

### Predicting Diabetes Risk from Medical Diagnostic Measurements

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.x-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Colab](https://img.shields.io/badge/Google-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

> **Early diabetes prediction using classification models trained on the Pima Indians Diabetes Dataset —
> helping identify high-risk individuals before symptoms escalate.**

<br/>

![Outcome Distribution](outcome_distribution.png)

</div>

---

## 📌 Overview

Diabetes is one of the most prevalent chronic diseases worldwide, affecting millions of people across all age groups. **Early and accurate prediction** can help healthcare professionals identify high-risk individuals and enable timely medical intervention — potentially saving lives.

This project builds, trains, and evaluates **machine learning classification models** to predict diabetes risk based on key patient health indicators including glucose levels, BMI, blood pressure, insulin, and age. The complete ML workflow — from raw data to model evaluation — is implemented end-to-end.

---

## 📊 Dataset

| Property | Details |
|---|---|
| **Name** | Pima Indians Diabetes Dataset |
| **Source** | [Kaggle / UCI ML Repository](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) |
| **Records** | 768 patients |
| **Features** | 8 medical attributes |
| **Target** | `Outcome` — `0` (Non-Diabetic) / `1` (Diabetic) |

### 🔬 Feature Descriptions

| Feature | Description |
|---|---|
| `Pregnancies` | Number of times pregnant |
| `Glucose` | Plasma glucose concentration (2-hr oral glucose tolerance test) |
| `BloodPressure` | Diastolic blood pressure (mm Hg) |
| `SkinThickness` | Triceps skin fold thickness (mm) |
| `Insulin` | 2-hour serum insulin (mu U/ml) |
| `BMI` | Body Mass Index (weight in kg / height in m²) |
| `DiabetesPedigreeFunction` | Genetic risk score based on family history |
| `Age` | Patient age (years) |

---

## 🛠️ Tech Stack

<div align="center">

| Category | Tools |
|---|---|
| **Language** | Python 3.8+ |
| **Data Manipulation** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Machine Learning** | Scikit-Learn |
| **Environment** | Google Colab / Jupyter Notebook |

</div>

---

## 🔄 ML Workflow

```
Raw Data  →  EDA  →  Preprocessing  →  Model Training  →  Evaluation  →  Insights
```

### 1️⃣ Data Loading & Exploration
- Loaded the dataset and inspected shape, types, and summary statistics
- Identified missing/zero values in critical medical columns

### 2️⃣ Exploratory Data Analysis (EDA)
- Outcome distribution analysis (class imbalance check)
- Feature correlation heatmap
- Distribution plots for each feature by outcome class

### 3️⃣ Data Preprocessing
- Handled zero-value anomalies in medical features
- **Train-Test Split:** 80% training / 20% testing
- **Feature Scaling:** `StandardScaler` for normalized feature ranges

### 4️⃣ Model Training
- **Logistic Regression** — interpretable baseline classifier
- **Random Forest Classifier** — ensemble tree-based model

### 5️⃣ Model Evaluation
- Accuracy Score
- Precision, Recall, F1-Score (Classification Report)
- Confusion Matrix visualization

---

## 🤖 Model Results

<div align="center">

| Model | Accuracy | Notes |
|---|---|---|
| ✅ **Logistic Regression** | **75.32%** | **Best performing model** |
| 🌲 Random Forest | 72.08% | Ensemble method; prone to overfitting on small datasets |

</div>

> **Winner: Logistic Regression** with **75.32% accuracy** on the test set.
> On small, tabular medical datasets, simpler models often generalize better than complex ensembles.

---

## 📈 Visualizations

<div align="center">

| Outcome Distribution | Correlation Heatmap | Confusion Matrix |
|:---:|:---:|:---:|
| ![Outcome Distribution](outcome_distribution.png) | ![Correlation Heatmap](correlation_heatmap.png) | ![Confusion Matrix](confusion_matrix.png) |

</div>

---

## 💡 Key Findings

- 🔴 **Glucose** showed the **strongest correlation** with diabetes outcome — the single most predictive feature
- 🟠 **BMI** and **Age** were the next most significant indicators of diabetes risk
- 🟡 **Insulin** and **SkinThickness** had notable zero-value anomalies, indicating potential data collection gaps
- ✅ **Logistic Regression outperformed Random Forest** on this dataset — likely due to the small sample size (768 records) limiting ensemble gains
- 📊 **Data visualization** was critical for identifying feature distributions, outliers, and class imbalances before modeling

---

## 🚀 Getting Started

### ▶️ Run on Google Colab *(Recommended — No Setup Required)*

1. Open `Diabetes_Prediction_ML_Project.ipynb` in Google Colab
2. Click **Runtime → Run All**
3. All cells execute sequentially — results and visualizations appear inline

---

### 💻 Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/diabetes-prediction-ml.git
cd diabetes-prediction-ml
```

**2. Install dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**3. Launch the notebook**
```bash
jupyter notebook Diabetes_Prediction_ML_Project.ipynb
```

---

## 📁 Project Structure

```
diabetes-prediction-ml/
│
├── 📓 Diabetes_Prediction_ML_Project.ipynb   # Main notebook (EDA + Models)
├── 📊 outcome_distribution.png               # Class distribution plot
├── 🔥 correlation_heatmap.png                # Feature correlation heatmap
├── 🟦 confusion_matrix.png                   # Model evaluation matrix
└── 📄 README.md                              # Project documentation
```

---

## 🔮 Future Improvements

- [ ] **Hyperparameter Tuning** — GridSearchCV / RandomizedSearchCV for optimal model parameters
- [ ] **Cross-Validation** — K-Fold CV for more robust performance estimation
- [ ] **XGBoost / LightGBM** — Advanced gradient boosting models
- [ ] **Explainable AI (XAI)** — SHAP values for feature importance and model interpretability
- [ ] **Streamlit Deployment** — Interactive web app for real-time diabetes risk prediction
- [ ] **Handling Zero Values** — Advanced imputation strategies for missing medical measurements
- [ ] **ROC-AUC Analysis** — Threshold tuning for better precision-recall trade-offs in medical context

---

## 🧠 Skills Demonstrated

<div align="center">

`Data Analysis` &nbsp; `Exploratory Data Analysis` &nbsp; `Data Visualization`
`Feature Engineering` &nbsp; `Data Preprocessing` &nbsp; `Model Training`
`Classification` &nbsp; `Model Evaluation` &nbsp; `End-to-End ML Workflow`

</div>

---

## 👨‍💻 Author

<div align="center">

**Your Name**
*Machine Learning Enthusiast | Engineering Student*

[![GitHub](https://img.shields.io/badge/GitHub-@yourusername-181717?style=for-the-badge&logo=github)](https://github.com/yourusername)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/yourusername)

</div>

---

<div align="center">

⭐ **If you found this project useful or insightful, consider starring the repository!**

*It helps others discover the project and keeps me motivated to build more.*

</div>
