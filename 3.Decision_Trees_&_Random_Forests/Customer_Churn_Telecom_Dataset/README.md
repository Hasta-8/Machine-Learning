# ☎️ Telecom Churn Prediction on Imbalanced Data with SMOTE & Decision Trees

This project analyzes a telecom customer churn dataset with significant class imbalance. It applies advanced resampling techniques like **SMOTE** and **SMOTENC** to improve the classification performance of models like **Logistic Regression** and **Decision Tree Classifier**.

---

## 📊 Dataset Overview

- Features: Account details, call charges (day, evening, night, international), number of customer service calls
- Target: `Churn` (1 if the customer churned, 0 otherwise)
- Nature: Highly imbalanced — very few customers have actually churned

---

## 🧪 Workflow & Techniques Used

### 🔍 Data Exploration
- Loaded the dataset and inspected distributions
- Identified class imbalance
- Categorical feature encoding using one-hot

### 🧹 Preprocessing
- Feature selection
- SMOTE and SMOTENC used to balance the minority class

### 🤖 Model Training & Evaluation
- Models used:
  - Logistic Regression
  - Decision Tree Classifier
- Techniques:
  - Applied SMOTE for synthetic data balancing
  - Used cross-validation to assess model generalization
  - Visualized Decision Tree
  - Extracted and interpreted decision rules

---

## 📝 Key Findings

- Logistic Regression struggled on the imbalanced dataset, especially for minority class prediction.
- Applying **SMOTE/SMOTENC** significantly improved recall and F1-score for the churn class.
- Decision Tree overfitted on training data but gave better generalization via cross-validation.
- Tree rules provided valuable insights into churn-driving patterns (e.g., high international call charges + frequent customer service calls).

---

## 📁 Files in This Folder

| File Name                                                           | Description                            |
|---------------------------------------------------------------------|----------------------------------------|
| `DecisionTrees_&_RandomForests_Classifier_for_Telecom_Churn_Dataset.ipynb` | Main notebook for the full analysis    |
| `Telecom_Churn_For_SMOTE.csv`                                      | Modified dataset prepared for SMOTE    |

---

## 🚀 How to Run

1. Clone the repo and navigate:
   ```bash
   git clone https://github.com/hasta-8/machine-learning.git
   cd machine-learning/Decision_Trees_&_Random_Forests/Customer_Churn_Telecom_Dataset
