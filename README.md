# 🧠 Brain Stroke Prediction Model

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-green?style=flat-square&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

> A machine learning classification model that predicts stroke risk in patients using demographic and clinical health indicators — achieving ~95% accuracy.

---

## 📌 Project Overview

Stroke is a life-threatening neurological condition caused by a disruption of blood supply to the brain. Early identification of at-risk individuals can significantly improve clinical outcomes and reduce long-term disability.

This project develops a supervised machine learning pipeline to classify patients as stroke-prone or not, based on anonymised health records. The goal is to support healthcare professionals with a data-driven risk assessment tool that integrates seamlessly into clinical decision support systems.

---

## 🎯 Objectives

- Analyse demographic and lifestyle data to uncover key stroke risk factors
- Build and evaluate multiple classification models for early stroke detection
- Select the best-performing model based on rigorous evaluation metrics
- Demonstrate the viability of predictive analytics in clinical settings

---

## 📂 Repository Structure

```
Brain-Stroke-predection/
│
├── Brain_Stroke.ipynb      # Full ML pipeline: EDA → preprocessing → modelling → evaluation
├── Stroke_data.csv         # Anonymised patient health records dataset
└── README.md
```

---

## 📊 Dataset

The dataset contains anonymised patient health records with the following features:

| Feature | Description |
|---|---|
| `age` | Patient age |
| `gender` | Male / Female / Other |
| `hypertension` | 0 = No, 1 = Yes |
| `heart_disease` | 0 = No, 1 = Yes |
| `avg_glucose_level` | Average blood glucose level |
| `bmi` | Body Mass Index |
| `smoking_status` | Never smoked / Formerly smoked / Smokes |
| `work_type` | Employment category |
| `Residence_type` | Urban / Rural |
| `stroke` | **Target variable** — 0 = No Stroke, 1 = Stroke |

---

## 🔬 Methodology

### 1. Data Preprocessing
- Handled missing values (notably in `bmi`)
- Encoded categorical variables using label encoding and one-hot encoding
- Applied feature scaling and normalisation for distance-based algorithms

### 2. Exploratory Data Analysis (EDA)
- Visualised feature distributions and class imbalance
- Analysed correlations between lifestyle factors (e.g. smoking, hypertension) and stroke incidence
- Generated heatmaps, count plots, and box plots to guide feature selection

### 3. Model Development

The following classification algorithms were trained and benchmarked:

| Model | Notes |
|---|---|
| Logistic Regression | Baseline linear classifier |
| Decision Tree | Interpretable rule-based model |
| Random Forest | Ensemble method; robust to overfitting |
| Support Vector Machine (SVM) | Effective in high-dimensional spaces |

### 4. Evaluation

Models were evaluated using:
- **Accuracy** — overall correctness
- **Precision & Recall** — especially important given class imbalance
- **F1 Score** — harmonic mean of precision and recall
- **Confusion Matrix** — breakdown of true/false positives and negatives

---

## 📈 Results

| Metric | Score |
|---|---|
| **Best Model Accuracy** | ~95% |
| Key Risk Indicators | Age, Hypertension, Avg Glucose Level, BMI |

The final model demonstrated strong predictive performance across validation datasets and improved identification of high-risk individuals.

---

## 🛠️ Technologies Used

- **Language:** Python 3
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Environment:** Jupyter Notebook

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/rachitkhn/Brain-Stroke-predection.git
cd Brain-Stroke-predection

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch the notebook
jupyter notebook Brain_Stroke.ipynb
```

---

## 💡 Key Takeaways

- Age, hypertension, and average glucose level are the strongest predictors of stroke risk
- Class imbalance is a critical challenge in medical classification — addressed through evaluation metric selection
- Ensemble methods (Random Forest) outperformed simpler classifiers on this dataset

---

## 👤 Author

**Rachit Khandelwal**
[GitHub](https://github.com/rachitkhn) · [LinkedIn](https://linkedin.com/in/rachitkhn)

---

*This project was developed as part of a data science portfolio focusing on real-world healthcare applications.*
