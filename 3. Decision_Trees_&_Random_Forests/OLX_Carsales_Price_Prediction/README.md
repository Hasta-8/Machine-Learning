# 🚗 OLX Used Car Price Prediction with Decision Trees & Ensemble Models

This project presents a full pipeline to predict used car prices using machine learning. It leverages a cleaned dataset of OLX car listings and applies tree-based regression algorithms to build interpretable and high-performing models.

---

## 📊 Dataset Overview

- **Source**: Cleaned OLX car sales data
- **Features**: 
  - Location, Year of Manufacture (converted to Age)
  - Kilometers Driven, Fuel Type, Transmission, Owner Type
  - Mileage, Engine Size, Power, Number of Seats
- **Target Variable**: `Price`

---

## 🧪 Workflow & Techniques Used

### 🔍 Exploratory Data Analysis (EDA)
- Inspected numerical and categorical features
- Created a new feature: **`Age` = Current Year - Manufacturing Year**
- Analyzed distributions and feature types

### 🧹 Preprocessing
- Standardized numerical features using `StandardScaler`
- Applied `pd.get_dummies()` for one-hot encoding of categorical variables
- Split the dataset using `train_test_split` for model evaluation

### 🤖 Models Trained
1. **Linear Regression**
   - Used as a baseline model
   - Applied log transformation to `Price` due to skew
2. **Decision Tree Regressor**
   - Tuned `max_depth` to reduce overfitting
   - Evaluated with cross-validation
3. **Random Forest Regressor**
   - Used 1000 estimators for robust ensemble learning
4. **Gradient Boosting Regressor**
   - Also trained with 1000 estimators for higher accuracy

---

## 📈 Model Evaluation

- **Metrics Used**: R-squared (`R²`) and Root Mean Squared Error (RMSE)
- **Key Insights**:
  - Tree-based ensemble models significantly outperformed Linear Regression
  - Decision Tree overfitting controlled via depth tuning
  - `Power` and `Age` were found to be the most important features

---

## 📁 Files in This Folder

| File Name                                                                   | Description                               |
|------------------------------------------------------------------------------|-------------------------------------------|
| `OLX_Car_Sales_Price_Prediciton_Using_Decision_Trees_and_Random_Forests.ipynb` | Main notebook with end-to-end workflow    |
| `OLX Car Sales Cleaned.csv`                                                 | Cleaned OLX dataset used in the project   |

---

## 🚀 How to Run

1. Clone the repository and move to the project folder:
   ```bash
   git clone https://github.com/hasta-8/machine-learning.git
   cd machine-learning/Decision_Trees_&_Random_Forests/OLX_Carsales_Price_Prediction
