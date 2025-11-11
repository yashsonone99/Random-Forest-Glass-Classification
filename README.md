# Random-Forest-Glass-Classification
“Predicting glass types using Random Forest — from data cleaning, EDA, to ensemble learning and hyperparameter tuning 🌲📊”
# 🌲 Random Forest Classification on Glass Dataset  

This project implements a **Random Forest Classifier** to predict the **type of glass** based on its chemical composition.  
It covers the entire pipeline — from **data cleaning and EDA** to **model training, tuning, and ensemble comparison** — providing a hands-on understanding of classification and ensemble learning techniques in machine learning.  

---

## 🎯 Objectives  
- Perform detailed **data cleaning** and handle missing or inconsistent data  
- Conduct **Exploratory Data Analysis (EDA)** using histograms, boxplots, and correlation heatmaps  
- Build and evaluate a **Random Forest Classifier** for multi-class prediction  
- Perform **hyperparameter tuning** using GridSearchCV  
- Compare performance with **Bagging**, **AdaBoost**, and **Gradient Boosting** models  
- Save the **best performing model** for deployment  

---

## ⚙️ Technologies Used  
- **Python** 🐍  
- **Pandas**, **NumPy** — Data manipulation and preprocessing  
- **Matplotlib**, **Seaborn** — Data visualization  
- **Scikit-learn** — Model building, tuning, and evaluation  
- **Joblib** — Model saving  

---

## 📁 Files Included  
| File Name | Description |
|------------|-------------|
| `Random_forest.ipynb` | Complete notebook containing code and visualizations |
| `glass.csv` | Input dataset containing chemical composition of glass samples |
| `best_random_forest_glass.pkl` | Saved model after hyperparameter tuning |
| `README.md` | Project documentation |

---

## ⚙️ Steps Involved  

### 1️⃣ Data Loading & Cleaning  
- Loaded `glass.csv` dataset  
- Removed missing values and duplicates  
- Ensured all numeric features were correctly typed  

### 2️⃣ Exploratory Data Analysis (EDA)  
- Visualized data distributions using histograms and boxplots  
- Created a **correlation heatmap** for feature relationships  
- Checked **target variable balance** (Glass Type)

### 3️⃣ Data Preprocessing  
- Scaled features using **StandardScaler**  
- Split data into training and testing sets (75:25 ratio)

### 4️⃣ Model Building  
- Built a **baseline Random Forest model**  
- Evaluated using:
  - Accuracy  
  - Precision  
  - Recall  
  - F1-Score  
  - Confusion Matrix  

### 5️⃣ Hyperparameter Tuning  
- Applied **GridSearchCV** to optimize:
  - `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`  
- Selected best performing model and re-evaluated on test data  

### 6️⃣ Ensemble Learning Comparison  
Compared Random Forest with:
- **Bagging Classifier** (with Random Forest base)  
- **AdaBoost Classifier**  
- **Gradient Boosting Classifier**  

Displayed comparative performance with accuracy metrics and confusion matrices.

### 7️⃣ Model Saving  
- Exported the tuned Random Forest model as  
  ```python
  joblib.dump(best_rf, "best_random_forest_glass.pkl")
