# 📉 Customer Churn Prediction Using Decision Trees & Ensemble Models

This project analyzes a customer churn dataset and builds multiple machine learning models to predict whether a customer is likely to churn. The goal is to identify key factors contributing to churn and evaluate classification models on their ability to generalize.

---

## 🧠 Project Highlights

### 🔍 Exploratory Data Analysis (EDA)
- Dataset loaded and explored using summaries, info, and value distributions.
- Categorical feature frequencies visualized with seaborn and matplotlib.
- Outliers and distributions examined through histograms, box plots, and KDE plots.

### 🧹 Data Preprocessing
- Separated numerical and categorical columns.
- Correlation heatmap plotted to detect multicollinearity.
- Dropped 'Frequency of use' feature due to strong correlation.
- Scaled numerical features with `StandardScaler`.
- Applied one-hot encoding using `pd.get_dummies()` for categorical variables.

### 🤖 Model Training & Evaluation
- Models used:
  - Logistic Regression
  - Decision Tree Classifier (with cross-validation)
  - Random Forest Classifier (optimized using OOB sampling)
  - Gradient Boosting Classifier

- Optimization:
  - Out-of-Bag (OOB) sampling to tune `n_estimators` in Random Forest.
  - `cross_val_score()` for evaluating model stability.

- Evaluation Metrics:
  - Accuracy
  - Classification Report (Precision, Recall, F1-Score)
  - Feature Importance (for Decision Tree)

---

## 📁 Files in This Folder

| File Name                                                                 | Description                             |
|---------------------------------------------------------------------------|-----------------------------------------|
| `DecisionTrees_&_RandomForests_&_GradientBoosting_Using_Customer_Churn_Dataset.ipynb` | Main notebook with full analysis        |
| `Dataset Customer Churn.csv`                                              | Original dataset used for training      |

---

## 📊 Dataset Description

- Binary classification dataset containing:
  - Customer demographics
  - Service usage features
  - Categorical features (e.g., gender, product type, payment method)
  - Target variable: Churn (Yes/No)

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/hasta-8/machine-learning.git
   cd machine-learning/Decision_Trees_&_Random_Forests/Customer_Churn_Dataset
