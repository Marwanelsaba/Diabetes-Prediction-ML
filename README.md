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

## 📑 Table of Contents

- [Objectives](#-objectives)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Data Preprocessing](#-data-preprocessing)
- [Machine Learning Models](#-machine-learning-models)
- [Hyperparameter Optimization](#-hyperparameter-optimization)
- [Evaluation Metrics](#-model-evaluation-metrics)
- [Results](#-results)
- [Technologies Used](#-technologies-used)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Future Improvements](#-future-improvements)

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

### Target Classes

- **N** → Normal
- **P** → Prediabetic
- **Y** → Diabetic

---

## 📋 Dataset Feature Definitions

The dataset contains demographic information together with clinical and laboratory measurements commonly used to assess diabetes and related metabolic conditions.

| Feature | Type | Description | Importance |
|---------|------|-------------|------------|
| **Gender** | Categorical | Patient's biological sex | Influences metabolism and diabetes risk |
| **AGE** | Numerical | Patient age (years) | Diabetes risk generally increases with age |
| **Urea** | Numerical | Blood urea concentration | Reflects kidney function |
| **Cr** | Numerical | Blood creatinine level | Important indicator of kidney health |
| **HbA1c** | Numerical | Average blood glucose over the previous 2–3 months | Primary clinical indicator for diabetes diagnosis |
| **Chol** | Numerical | Total cholesterol level | Associated with cardiovascular complications |
| **TG** | Numerical | Triglyceride concentration | Elevated values are linked to metabolic syndrome |
| **HDL** | Numerical | High-density lipoprotein ("good" cholesterol) | Lower levels increase cardiovascular risk |
| **LDL** | Numerical | Low-density lipoprotein ("bad" cholesterol) | Higher levels contribute to heart disease risk |
| **VLDL** | Numerical | Very-low-density lipoprotein | Associated with lipid metabolism disorders |
| **BMI** | Numerical | Body Mass Index (kg/m²) | Strong indicator of obesity and diabetes risk |
| **CLASS** | Target | Diabetes classification (N, P, Y) | Variable predicted by the machine learning models |

---

### 📊 Dataset Summary

| Property | Value |
|----------|------:|
| Number of Samples | **1000** |
| Predictive Features | **11** |
| Target Classes | **3** |
| Numerical Features | **10** |
| Categorical Features | **1** |
| Missing Values | **0** |
| Duplicate Records | **0** |

---

## 🏗️ Project Workflow

```mermaid
flowchart TD

    A["📄 Diabetes.csv"] --> B["🔍 Data Inspection<br/>Missing Values, Duplicates,<br/>Data Types"]

    B --> C["🧹 Data Cleaning<br/>Normalize CLASS & Gender<br/>Remove Invalid Values"]

    C --> D["📊 Exploratory Data Analysis (EDA)<br/>Histograms, Boxplots,<br/>Correlation Heatmap,<br/>Regression & Pair Plots"]

    D --> E["⚙️ Feature Engineering<br/>Encoding<br/>Scaling<br/>Discretization"]

    E --> F["✂️ Stratified Train/Test Split<br/>85% Train • 15% Test"]

    F --> G["⚖️ Handle Class Imbalance<br/>SMOTE Oversampling"]

    G --> H["🤖 Machine Learning Models<br/>Decision Tree<br/>Logistic Regression<br/>Random Forest<br/>SVM<br/>KNN<br/>Naive Bayes"]

    H --> I["🔧 Hyperparameter Optimization<br/>GridSearchCV<br/>5-Fold Cross Validation"]

    I --> J["📈 Model Evaluation<br/>Accuracy<br/>Precision<br/>Recall<br/>F1 Score<br/>Confusion Matrix"]

    J --> K["📊 Feature Importance<br/>Decision Tree<br/>Logistic Regression"]

    K --> L["🏆 Performance Comparison<br/>Select Best Model"]

    style A fill:#E3F2FD,stroke:#1565C0
    style D fill:#FFF3E0,stroke:#EF6C00
    style F fill:#E8F5E9,stroke:#2E7D32
    style G fill:#FFF8E1,stroke:#F9A825
    style H fill:#EDE7F6,stroke:#5E35B1
    style I fill:#FCE4EC,stroke:#AD1457
    style J fill:#E0F7FA,stroke:#00838F
    style L fill:#C8E6C9,stroke:#1B5E20
```
# 🔍 Exploratory Data Analysis

Several visualization techniques were used to better understand the dataset.

### Exploratory Analysis Included

- 📊 Histograms
- 📦 Boxplots
- 🎻 Violin Plots
- 🔥 Correlation Heatmap
- 🔗 Pairplots
- 📈 Regression Plots
- 📉 Class Distribution
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

The following regression plots illustrate relationships between key medical features associated with diabetes.

<p align="center">
  <img src="images/pairplot1.png" width="45%">
  <img src="images/pairplot2.png" width="45%">
</p>

<p align="center">
  <img src="images/pairplot3.png" width="45%">
  <img src="images/pairplot4.png" width="45%">
</p>

<p align="center">
  <img src="images/pairplot5.png" width="45%">
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

Decision Tree        GridSearchCV
Random Forest        GridSearchCV
Logistic Regression  GridSearchCV
SVM                  GridSearchCV
KNN                  GridSearchCV
Gaussian NB          Stratified 5-Fold CV

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

| Category | Libraries |
|----------|-----------|
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-Learn |
| Imbalanced Learning | Imbalanced-Learn |
| Development Environment | Jupyter Notebook |

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

# 📊 Model Performance Comparison

The performance of each machine learning model was evaluated using **Accuracy**, **Precision**, **Recall**, and **F1 Score** on the test dataset.

| Model | Accuracy | Precision | Recall | F1 Score |
|:------|---------:|----------:|--------:|---------:|
| 🌳 Decision Tree | **99.33%** | **99.34%** | **99.33%** | **99.31%** |
| 📈 Logistic Regression | 94.67% | 93.68% | 94.67% | 93.64% |
| 🌲 Random Forest | **99.33%** | **99.34%** | **99.33%** | **99.31%** |
| ⚙️ Support Vector Machine (SVM) | 95.33% | 94.81% | 95.33% | 94.72% |
| 👥 K-Nearest Neighbors (KNN) | 88.23% | 84.72% | 83.53% | 82.69% |
| 🧠 Gaussian Naive Bayes* | 92.50% | 80.12% | 88.67% | 83.49% |

---

## 📌 Conclusion

This project demonstrates an end-to-end machine learning pipeline for diabetes prediction, covering data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter optimization, and performance evaluation.

Among the evaluated algorithms, the best-performing model achieved the highest predictive performance after hyperparameter tuning using GridSearchCV. The results highlight the effectiveness of combining proper preprocessing, balanced data handling, and model optimization for healthcare classification tasks.

---
