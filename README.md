# Logistic Regression - Bank Marketing Dataset  

## Overview  
This project applies **Logistic Regression** to predict whether a customer will subscribe to a term deposit based on their **demographics, financial status, and previous interactions** in a bank marketing campaign. The dataset contains **41,000+ records** with **20+ features**, including **age, job type, balance, contact history, and campaign details**.  

## Dataset  
📂 **File:** `bank-additional-full.csv`  
📊 **Rows:** 41,000+  
🔢 **Columns:** 20+  

### **Key Features:**  
- **age** – Client’s age  
- **job** – Job type (e.g., admin, technician)  
- **marital** – Marital status (single/married/divorced)  
- **education** – Education level  
- **default** – Credit in default (yes/no)  
- **balance** – Account balance (in euros)  
- **housing** – Has a housing loan (yes/no)  
- **loan** – Has a personal loan (yes/no)  
- **contact** – Contact communication type (cellular/telephone)  
- **campaign** – Number of contacts made during this campaign  
- **pdays** – Days since last contact (-1 means never contacted)  
- **previous** – Number of times contacted before this campaign  
- **y** (Target) – Subscribed to a term deposit? (1 = Yes, 0 = No)  

---

## **Project Workflow**  

### **1️⃣ Data Preprocessing**  
- Loads the dataset and handles **missing values**  
- Removes **duplicate entries** to avoid bias  
- Detects and removes **outliers** in numerical features (`age`, `duration`, `campaign`, etc.)  
- Encodes categorical variables using **Label Encoding**  

### **2️⃣ Feature Selection & Multicollinearity Handling**  
- Uses **Recursive Feature Elimination (RFE)** to identify the most important features  
- Applies **Variance Inflation Factor (VIF)** to remove highly correlated variables (`pdays`, `previous`, `poutcome`)  

### **3️⃣ Model Training - Logistic Regression**  
- Splits the dataset into **70% training** and **30% testing** sets  
- Trains a **Logistic Regression** model using `sklearn`  
- Predicts customer responses on the test set  

### **4️⃣ Model Evaluation**  
- Computes **accuracy score** for model performance  
- Analyzes **confusion matrix** to assess false positives & false negatives  
- Visualizes the **Sigmoid function** to understand classification probability  

---

## **Technologies Used**  
🚀 **Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn**  

## **Results & Insights**  
- **Feature selection and VIF-based removal improved model performance**  
- **Logistic Regression effectively classifies customer responses** using probability-based predictions  
- **Outlier removal and categorical encoding enhanced prediction accuracy**  

---

## **Future Improvements**  
🔹 Implement **Random Forest** or **XGBoost** for better classification accuracy  
🔹 Apply **SMOTE** to handle class imbalance in the dataset  
🔹 Optimize hyperparameters using **GridSearchCV**  
🔹 Use **AUC-ROC curves** to evaluate model performance  

