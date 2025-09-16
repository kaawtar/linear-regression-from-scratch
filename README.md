# 🩺 Predicting Medical Insurance Charges with Regression Models

This project explores the prediction of **medical insurance charges** using regression models.  
We start by building a **Linear Regression model from scratch** and then extend the work with advanced regression techniques including **Ridge Regression, Lasso Regression, and Random Forest Regression**.  

The project not only demonstrates implementation but also provides **interpretation of results** for each model.

---

## 📂 Dataset

We used the **[Medical Insurance Dataset (insurance.csv)](https://www.kaggle.com/mirichoi0218/insurance)**.  
It contains demographic, lifestyle, and health-related factors:

- **age**: Patient’s age (years)  
- **sex**: Biological sex (male/female)  
- **bmi**: Body Mass Index (kg/m²) – a measure of obesity  
- **children**: Number of dependents covered by insurance  
- **smoker**: Smoking status (yes/no)  
- **region**: Patient’s residential region in the US  
- **charges**: Final medical cost billed by insurance (**target variable**)  

---

## 🎯 Project Objective

The goal is to predict **medical charges** (`charges`) using patient characteristics.  

We focus on the following features for building regression models:
- **age**: Older age → higher health risks & costs  
- **bmi**: Higher BMI → obesity-related diseases → higher costs  
- **children**: More dependents → higher insurance usage  
- **smoker**: Smoking strongly increases medical costs  

---

## 🛠️ Data Preprocessing

Before building models, we prepared the dataset by:
1. **Feature Selection**: Chose biologically & statistically relevant features.  
2. **Encoding Categorical Variables**: Converted `sex`, `smoker`, and `region` into numerical format.  
3. **Scaling (Optional)**: Applied scaling to speed up convergence of gradient descent.  
4. **Train-Test Split**: Split dataset into training and testing subsets.  

---

## 🤖 Models Implemented

### **1. Linear Regression (from scratch)**
- Implemented using **NumPy** without scikit-learn.  
- Gradient descent optimization.  
- Compared with scikit-learn implementation.  
- ✅ Interpretation of coefficients (effect of age, BMI, smoking, etc.).

---

### **2. Ridge Regression**
- Adds **L2 regularization** to handle multicollinearity.  
- Controls overfitting by penalizing large coefficients.  
- ✅ Interpretation of shrinkage effect on coefficients.

---

### **3. Lasso Regression**
- Adds **L1 regularization** for **feature selection**.  
- Some coefficients shrink to zero → selects only the most impactful predictors.  
- ✅ Interpretation of which features remain significant.  

---

### **4. Random Forest Regression**
- Non-linear, ensemble-based model.  
- Captures complex feature interactions beyond linear assumptions.  
- ✅ Feature importance ranking provided.  

---

## 📊 Results & Insights

- **Linear Regression**: Captures baseline relationships between patient features and costs.  
- **Ridge**: Reduces variance; improves generalization.  
- **Lasso**: Identifies smoking & BMI as dominant predictors.  
- **Random Forest**: Achieves the best predictive performance but at the cost of interpretability.  

Key finding:  
➡️ **Smoking** and **BMI** are the strongest predictors of insurance charges.  
➡️ Age also plays an important role, but less than smoking.  


