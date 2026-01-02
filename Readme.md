# 📘 Data Preprocessing Pipeline

This repository contains a complete **data preprocessing workflow** designed to prepare raw data for **exploratory data analysis (EDA)** and **machine learning model development**.  
The pipeline focuses on improving data quality, consistency, and reliability through structured preprocessing steps.

---

## 🔹 1. Handling Missing Values

This step identifies and handles missing values present in the dataset to ensure completeness and consistency.

### Key Steps
- Loaded the dataset and inspected its structure and data types  
- Identified missing values in numerical and categorical features  
- Analyzed the distribution and proportion of missing data  
- Visualized missing values using heatmaps  
- Applied appropriate handling techniques:
  - Dropped rows or columns with excessive missing values  
  - Imputed missing **numerical values using the median**  
  - Imputed missing **categorical values using the mode**  
- Verified the dataset after preprocessing  

### Libraries Used
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

## 🔹 2. Handling Outliers

This step focuses on detecting and treating extreme values that may negatively impact analysis or model performance.

### Key Steps
- Used the cleaned dataset after missing value handling  
- Selected continuous numerical features for outlier detection  
- Excluded the target variable from outlier analysis  
- Detected outliers using **boxplots and the IQR method**  
- Capped extreme values within acceptable bounds  
- Verified data stability after outlier treatment  

### Libraries Used
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

## 🔹 3. Column Transformation

This step prepares the dataset for machine learning by applying suitable transformations to numerical and categorical features.

### Key Steps
- Identified numerical and categorical features based on data types  
- Applied **ColumnTransformer** to handle different feature types simultaneously  
- Used:
  - **StandardScaler / MinMaxScaler / RobustScaler** for numerical features  
  - **OneHotEncoder / LabelEncoder / OrdinalEncoder** for categorical features  
- Converted the transformed output into a model-ready DataFrame  

### Libraries Used
- Pandas  
- NumPy  
- Scikit-learn  

---

## 🔹 4. Column Transformation Using Functions

This step improves code reusability and scalability by implementing preprocessing logic using functions.

### Key Steps
- Created reusable functions for:
  - Identifying numerical and categorical columns  
  - Scaling numerical features  
  - Encoding categorical features  
  - Applying transformations using ColumnTransformer  
- Ensured consistent and leakage-free preprocessing  

---

## 🔹 5. Feature Selection – Numerical Features

This step identifies the most informative numerical features contributing to the target variable.

### Techniques Used
- Correlation analysis  
- Variance Threshold  
- Mutual Information Regression  

### Outcome
- Reduced redundancy  
- Retained important numerical features  
- Improved model efficiency and interpretability  

---

## 🔹 6. Feature Selection – Categorical Features

This step evaluates categorical features based on their relationship with the target variable.

### Techniques Used
- Chi-Square Test  
- Mutual Information  

### Outcome
- Selected informative categorical features  
- Reduced noise and irrelevant variables  

---

## ✅ Final Outcome

After completing the preprocessing pipeline, the dataset is:

- Clean and consistent  
- Free from missing values  
- Robust to outliers  
- Fully numerical, scaled, and encoded  
- Ready for:
  - Exploratory Data Analysis (EDA)  
  - Feature Engineering  
  - Machine Learning Model Training  

---

## 📌 Key Highlights

- Median imputation ensures robustness against outliers  
- ColumnTransformer enables clean and scalable preprocessing  
- Feature selection improves model performance and interpretability  
- Workflow follows **industry-standard machine learning practices**
