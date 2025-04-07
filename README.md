# 🏠 Advanced House Price Prediction (Kaggle Competition)

This project is my solution to the [Advanced House Prices - Kaggle Competition](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques). The goal is to predict the final price of residential homes based on various features describing the properties.

---

## 📌 Problem Statement

Predict the sale price of houses using 79 explanatory variables describing nearly every aspect of residential homes in Ames, Iowa.

---

## 🧠 My Approach

### 🧹 Data Preprocessing
- Handled missing values and outliers
- Removed irrelevant columns with little to no value
- Dropped features with high correlation to prevent multicollinearity
- Created new features and fixed skewed distributions

### 📊 Exploratory Data Analysis (EDA)
- Checked feature distributions and relationships with the target variable
- Analyzed correlation matrix and feature importance

### ⚙️ Feature Engineering
- Applied encoding techniques:
  - **Ordinal encoding** for features with inherent order (e.g. quality, condition)
  - **One-hot encoding** for nominal features without order (e.g. neighborhood)
- Handled skewness and applied log transformation where needed
- Used **StandardScaler** to normalize numerical features

### 🧪 Modeling & Evaluation
Trained and evaluated multiple regression models:

- Linear Regression
- Ridge, Lasso, ElasticNet
- K-Nearest Neighbors (KNN)
- Decision Tree (CART)
- Support Vector Regression (SVR)

Then evaluated ensemble models:

- Random Forest
- Extra Trees
- AdaBoost
- Gradient Boosting

Evaluation metric: `negative mean squared error (neg_mean_squared_error)` using cross-validation.

### ✅ Final Model
The **Ridge Regression** model had the **lowest mean squared error**, and was selected as the final model.

---

## 🛠 Tools Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## 📂 Project Structure
The project is organized as follows:
/ (root directory) │ ├── data/ # Folder for storing raw and processed datasets │ ├── notebooks/ # Jupyter Notebooks for Exploratory Data Analysis (EDA) │ ├── src/ # Source code for the project │ ├── init.py │ ├── feature_engineering.py │ ├── data_preprocessing.py │ └── model.py │ ├── models/ # Folder for saving trained models │ ├── README.md # This file ├── requirements.txt # List of Python dependencies └── .gitignore # Git ignore file for unnecessary files
