# 🍷 Wine Quality Classification Based on Chemical Properties

This project applies data analysis and machine learning techniques to **predict wine quality (rated from 0 to 10)** based on various chemical parameters.

---

## 📁 Repository Contents

- `wine_analysis.ipynb`: Main Jupyter Notebook with data exploration, preprocessing, model training, and evaluation.
- `/images`: Folder containing generated plots and visualizations.

---

## 📊 Dataset Description

The dataset includes multiple wine samples, each described by several physicochemical features such as:

- Fixed acidity  
- Volatile acidity  
- Citric acid  
- Residual sugar  
- Chlorides  
- Free sulfur dioxide  
- Total sulfur dioxide  
- Density  
- pH  
- Sulphates  
- Alcohol  

The target variable is the **quality score**, an integer ranging from 0 to 10.

---

## 🔍 Data Analysis

The notebook includes:

- **Data cleaning** and handling of missing values  
- **Descriptive statistics** and summary of the dataset  
- **Exploratory Data Analysis (EDA)** using histograms, box plots, and correlation heatmaps  
- **Feature selection** based on correlation and distribution  

Correlation heatmap:

![Correlation Heatmap](./images/Correlation_Matrix.png)

---

## 🤖 Machine Learning

We trained a classification model to predict wine quality. The steps include:

- Data splitting (training/test sets)
- Feature scaling (except for Random Forest)
- Model selection (Logistic Regression, SVC, Random Forest, Gradient Boosting)
- Cross Validation tests
- Hyperparameter tuning (Using GridSearchCV and RandomizedSearchCV)
- Performance evaluation (accuracy, f1, confusion matrix)

---

## 📈 Results

Random Forest and Gradient Boosting are the models with more accuracy. The problem of this two models is that they have high overfitting. Considering low overfitting, the best model should be the SVC.

- **Accuracy of SVC**: 0.5885
- **f1 of SVC**: 0.5640

![Confusion Matrix SVC](./images/ConfusionMatrix_SVC.png)

The Feature Importance using SHAP showed that acohol, density and volatile acidity were the most important features related with the quality of the wine.

![Feature Importance using SHAP](./images/SHAP_RandomForest.png)

---
