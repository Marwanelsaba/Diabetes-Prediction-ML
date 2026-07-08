# 🩺 Diabetes Prediction Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-blue)
![License](https://img.shields.io/badge/License-MIT-success)

---

## 📖 Project Overview

This project presents an **end-to-end Machine Learning pipeline** for predicting diabetes using patient medical records.

The project demonstrates the complete machine learning workflow, including:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Preprocessing
- Outlier Detection
- Hyperparameter Optimization
- Cross Validation
- Model Evaluation
- Model Comparison

Six different machine learning algorithms were implemented and compared to determine the best-performing classifier for diabetes prediction.

---

# 🎯 Objectives

- Predict whether a patient is:
  - Normal
  - Prediabetic
  - Diabetic

- Compare multiple machine learning algorithms.

- Analyze the influence of medical features on diabetes prediction.

- Optimize model performance using GridSearchCV.

---

# 📂 Dataset

The dataset contains **1000 patient records** collected from medical examinations.

### Features

| Feature | Description |
|----------|-------------|
| Gender | Patient Gender |
| AGE | Age |
| Urea | Blood Urea |
| Cr | Creatinine |
| HbA1c | Average Blood Sugar |
| Chol | Cholesterol |
| TG | Triglycerides |
| HDL | Good Cholesterol |
| LDL | Bad Cholesterol |
| VLDL | Very Low Density Lipoprotein |
| BMI | Body Mass Index |
| CLASS | Target Variable |

Target Classes

- N → Normal
- P → Prediabetes
- Y → Diabetes

---

# 🏗 Project Workflow

```text
                Dataset
                    │
                    ▼
          Data Cleaning & Preprocessing
                    │
                    ▼
        Exploratory Data Analysis (EDA)
                    │
                    ▼
          Feature Engineering
                    │
                    ▼
          Train/Test Split (85/15)
                    │
                    ▼
     Hyperparameter Optimization
                    │
                    ▼
      Train Machine Learning Models
                    │
                    ▼
         Performance Evaluation
                    │
                    ▼
        Compare Model Performance
```

---

# 🔍 Exploratory Data Analysis

Several visualization techniques were used to better understand the dataset.

✔ Histograms

✔ Boxplots

✔ Violin Plots

✔ Correlation Heatmaps

✔ Pairplots

✔ Regression Plots

✔ Class Distribution

---

## 📷 Dataset Overview

<img src="images/dataset_preview.png" width="900">

---

## 📷 Class Distribution

<p align="center">
<img src="images/class_distribution.png" width="750">
</p>

---

## 📷 Correlation Heatmap

<p align="center">
<img src="images/correlation_heatmap.png" width="850">
</p>

---

## 📷 Feature Relationships

<p align="center">
<img src="images/pairplot.png" width="900">
</p>

---

## 📷 Boxplots & Violin Plots

<p align="center">
<img src="figures/hba1c_class.png" width="800">
</p>

---

# ⚙ Data Preprocessing

The following preprocessing techniques were applied:

- Missing Value Checking
- Duplicate Detection
- Label Encoding
- One-Hot Encoding
- Standard Scaling
- Min-Max Scaling
- KBins Discretization
- SMOTE Oversampling
- Stratified Train/Test Split

---

# 🤖 Machine Learning Models

The following algorithms were implemented.

| Model | Hyperparameter Tuning |
|--------|----------------------|
| Decision Tree | ✅ |
| Logistic Regression | ✅ |
| Random Forest | ✅ |
| Support Vector Machine | ✅ |
| K-Nearest Neighbors | ✅ |
| Gaussian Naive Bayes | Cross Validation |

---

# 🔧 Hyperparameter Optimization

GridSearchCV was used for model optimization.

Example:

```
5-fold Cross Validation

↓

72 Parameter Combinations

↓

360 Model Fits

↓

Best Model Selected
```

---

# 📈 Model Evaluation Metrics

Each model was evaluated using

- Accuracy

- Precision

- Recall

- F1 Score

- Confusion Matrix

- Cross Validation

---

# 📷 Confusion Matrix Example

<p align="center">
<img src="images/confusion_matrix.png" width="650">
</p>

---

# 📊 Feature Importance

Decision Tree and Logistic Regression were used to analyze feature importance.

<p align="center">
<img src="images/feature_importance.png" width="800">
</p>

---

# 📋 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn
- Jupyter Notebook

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/Marwanelsaba/Diabetes-Prediction-ML.git
```

Move into the project

```bash
cd Diabetes-Prediction-ML
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook diabetes_prediction.ipynb
```

---

# 📁 Project Structure

```
Diabetes-Prediction-ML
│
├── figures/
│
├── data/
│   └── Diabetes.csv
│
├── diabetes_prediction.ipynb
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 Future Improvements

- Deep Learning Models
- XGBoost
- LightGBM
- CatBoost
- SHAP Explainability
- Streamlit Deployment
- Flask REST API
- Feature Selection
- Automated ML Pipeline

---

# 📌 Results

After comparing six machine learning algorithms, the optimized models demonstrated strong predictive performance for diabetes classification.

Hyperparameter tuning and cross-validation significantly improved the overall performance and robustness of the classifiers.

---
