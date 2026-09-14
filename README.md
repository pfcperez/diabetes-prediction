# Diabetes Prediction - Classification Model

[![Python](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Latest-orange.svg)](https://scikit-learn.org/)

## 📝 Overview

Medical data engineering pipeline that loads and transforms patient health data, then applies Random Forest classification to predict diabetes risk.

- **Dataset:** 768 patients × 8 medical features
- **Target:** Diabetes Outcome (Yes/No - Binary)
- **Model Performance:** Accuracy 74% | Recall 74%
- **Clinical Use:** Early diabetes risk identification

---

## 🎯 Key Features

✅ Load Pima Indians diabetes dataset (CSV)  
✅ Medical data analysis (glucose, BMI, blood pressure, etc.)  
✅ Handle class imbalance with resampling  
✅ Feature scaling & normalization  
✅ Random Forest classifier  
✅ Precision/Recall/F1-Score evaluation  
✅ Classification report with risk metrics  

---

## 🛠️ Tech Stack

- **Python 3.11+** | Pandas | NumPy
- **Visualization:** Matplotlib, Seaborn
- **ML:** Scikit-learn, SMOTE (resampling)
- **Development:** Jupyter Notebook

---

## 📦 Installation

```bash
# Clone repo
git clone https://github.com/pfcperez/diabetes-prediction.git
cd diabetes-prediction

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter

---

## 🚀 Usage

```bash
jupyter notebook diabetes_tree.ipynb
```

**Pipeline Steps:**
1. Load patient medical data (768 records × 8 features)
2. Exploratory data analysis (glucose, BMI, age distributions)
3. Handle missing/zero values in medical measurements
4. Detect class imbalance (65% no diabetes, 35% diabetes)
5. Apply SMOTE resampling to balance classes
6. Scale features with StandardScaler
7. Split data 70/30 (train/test)
8. Train Random Forest with balanced class weights
9. Evaluate with Precision, Recall, F1-Score

---

## 📊 Results

| Metric | Diabetes | No Diabetes |
|--------|----------|------------|
| **Precision** | 59% | 85% |
| **Recall** | 74% | 74% |
| **F1-Score** | 0.66 | 0.79 |

| Overall | Value |
|---------|-------|
| **Accuracy** | 74% |
| **Test Records** | 231 |

**Interpretation:** Model correctly identifies 74% of all patients. For diabetes patients specifically, catches 74% of cases but has higher false negatives (~26% missed).

---

## 🔑 Medical Features

- **Pregnancies** - Number of pregnancies
- **Glucose** - Plasma glucose concentration
- **BloodPressure** - Diastolic blood pressure (mmHg)
- **SkinThickness** - Triceps skin fold thickness (mm)
- **Insulin** - Serum insulin (mu U/ml)
- **BMI** - Body Mass Index (weight/height²)
- **DiabetesPedigreeFunction** - Genetic predisposition score
- **Age** - Age in years

---

## 📁 Project Structure

```
diabetes-prediction-pipeline/
├── diabetes_tree.ipynb       # Main notebook
├── README.md
├── requirements.txt
└── data/
    ├── raw/
    │   └── diabetes.csv
   
```

---

## 🔑 Data Transformations

- **Missing Values:** Zero handling in medical measurements
- **Resampling:** SMOTE to balance 65/35 class ratio
- **Feature Scaling:** StandardScaler for all features
- **Train/Test Split:** Stratified 70/30 split

---

## ⚠️ Class Imbalance Challenge

- Original ratio: 65% No Diabetes, 35% Diabetes
- Solution: SMOTE resampling + balanced class weights
- Result: Better recall for minority class (diabetes detection)

---

## 📚 Kaggle Dataset

Source: [Pima Indians Diabetes Database](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

---

**Author:** Ramiro Pérez | [GitHub](https://github.com/pfcperez)  
**Status:** ✅ Complete
