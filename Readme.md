# 1.📘 Data Preprocessing – Handling Missing Values

This notebook focuses on cleaning the dataset by identifying and handling missing values, which is a crucial step before performing analysis or building machine learning models.

---

## 🔹 Key Steps Performed

- 📂 Loaded the dataset and examined its structure and data types  
- 🔍 Identified missing values across numerical and categorical features  
- 📊 Analyzed the proportion and distribution of missing data  
- 📈 Visualized missing values and data patterns using plots  
- 🛠️ Applied appropriate handling techniques:
  - ❌ Dropping rows or columns with excessive missing values  
  - 🧮 Imputing missing values using **mean**, **median**, or **mode** based on feature type  
- ✅ Verified the dataset after preprocessing to ensure completeness and consistency  

---

## 🔹 Libraries Used

- 🐼 **Pandas** – data loading, manipulation, and missing value handling  
- 🔢 **NumPy** – numerical computations and imputation support  
- 📉 **Matplotlib** – basic data visualization  
- 🌊 **Seaborn** – statistical and missing value visualizations  

---

This preprocessing step ensures a **clean and reliable dataset**, forming a strong foundation for further analysis and machine learning workflows.


# 2. 📘 Data Preprocessing – Handling Outliers

This notebook continues the data preprocessing process by focusing on identifying and handling outliers, which can significantly affect data analysis and machine learning model performance if left untreated.

---

## 🔹 Key Steps Performed

- 📂 Used the cleaned dataset obtained after missing value handling  
- 🔢 Identified continuous numerical features suitable for outlier analysis  
- 🚫 Excluded the binary target variable from outlier detection  
- 📊 Detected outliers using boxplots based on the Interquartile Range (IQR)  
- 🧮 Calculated lower and upper bounds using the IQR method  
- 🛠️ Handled extreme values by capping them within acceptable limits  
- ✅ Verified the dataset after outlier treatment to ensure stability and consistency  

---

## 🔹 Libraries Used

- 🐼 **Pandas** – data manipulation and outlier handling  
- 🔢 **NumPy** – numerical computations  
- 📉 **Matplotlib** – visualization of boxplots  
- 🌊 **Seaborn** – statistical data visualizations  

---

This preprocessing step helps minimize the impact of extreme values, resulting in a **cleaner and more reliable dataset** for further analysis and machine learning modeling.

# 3.📘 Data Preprocessing

This repository contains notebooks focused on **data preprocessing**, an essential step before performing exploratory data analysis or building machine learning models.  
The preprocessing pipeline includes **handling missing values** and **outlier treatment** to ensure data quality and reliability.

---

## 3.1 Handling Missing Values

This notebook focuses on identifying and handling missing values present in the dataset.

### 🔹 Key Steps Performed

- Loaded the dataset and inspected its structure and data types  
- Identified missing values in numerical and categorical features  
- Analyzed the proportion and distribution of missing data  
- Visualized missing values using appropriate plots  
- Applied suitable handling techniques:
  - Dropped rows or columns with excessive missing values  
  - Imputed missing values using **mean**, **median**, or **mode** based on feature type  
- Verified the dataset to ensure completeness and consistency after preprocessing  

### 🔹 Libraries Used

- **Pandas** – data loading, manipulation, and missing value handling  
- **NumPy** – numerical computations and imputation support  
- **Matplotlib** – basic data visualization  
- **Seaborn** – statistical and missing value visualizations  

---

## 2️3.2 Handling Outliers

This notebook continues the preprocessing pipeline by focusing on identifying and handling outliers that may negatively impact model performance.

### 🔹 Key Steps Performed

- Used the cleaned dataset obtained after missing value handling  
- Selected continuous numerical features for outlier detection  
- Excluded the binary target variable from outlier analysis  
- Detected outliers using boxplots based on the **Interquartile Range (IQR)** method  
- Calculated lower and upper bounds using IQR  
- Handled extreme values by capping them within acceptable limits  
- Verified dataset stability and consistency after outlier treatment  

### 🔹 Libraries Used

- **Pandas** – data manipulation and outlier handling  
- **NumPy** – numerical computations  
- **Matplotlib** – boxplot visualization  
- **Seaborn** – statistical visualizations
- **Sk-Learn** - Feature Scaling

---

## ✅ Outcome

After completing these preprocessing steps, the dataset becomes:

- Clean and consistent  
- Free from missing values  
- Robust against extreme outliers  

This prepares the data for **exploratory data analysis**, **feature engineering**, and **machine learning model development**.

# 4. 📘 Data Preprocessing – Column Transformation

This notebook focuses on **column-wise data preprocessing** using `ColumnTransformer`, which is a crucial step before building machine learning models.  
It ensures that **numerical and categorical features are transformed appropriately and consistently**.

---

## 🔹 Objective

To prepare the dataset for machine learning by:
- Separating numerical and categorical features
- Applying suitable transformations to each feature type
- Producing a clean, model-ready dataset

This notebook is a continuation of the preprocessing pipeline after:
- Handling missing values  
- Treating outliers  

---

## 🔹 Dataset Handling

- 📂 Loaded the cleaned dataset after missing value and outlier treatment  
- 🔍 Inspected dataset structure and data types  
- 🧾 Identified feature categories based on data types  

---

## 🔹 Feature Categorization

- **Numerical Features**
  - Identified using `select_dtypes(include=np.number)`
  - These features are continuous and require scaling

- **Categorical Features**
  - Identified using `select_dtypes(include=object)`
  - These features require encoding before model training

---

## 🔹 Column Transformation Steps

- Applied **`ColumnTransformer`** to handle different feature types simultaneously
- Transformations used:
  - 🔢 **StandardScaler**
    - Applied to numerical (continuous) features
    - Ensures features have zero mean and unit variance
  - 🧩 **OneHotEncoder**
    - Applied to categorical features
    - Converts categorical values into numerical format
    - `sparse_output=False` used to obtain a dense output

---

## 🔹 Output

- Combined transformed numerical and categorical features
- Converted the transformed output into a new Pandas DataFrame
- Generated a **fully transformed, model-ready dataset**

---

## 🔹 Libraries Used

- 🐼 **Pandas** – data loading and manipulation  
- 🔢 **NumPy** – numerical operations  
- 🤖 **Scikit-learn**
  - `ColumnTransformer` – column-wise preprocessing
  - `StandardScaler`,`Min-Max Scalar`,`Robust Scalar` – feature scaling (Numerical feature Scaling)
  - `OneHotEncoder`,`Label Encoder`,`Ordinal Encoder`,`frequency/ Count Encoder` – categorical encoding
 

---

## ✅ Outcome

After column transformation, the dataset becomes:

- Fully numerical  
- Scaled and encoded  
- Consistent across feature types  
- Ready for:
  - Exploratory Data Analysis (EDA)
  - Feature Engineering
  - Machine Learning Model Training

---

## 📌 Note

Using `ColumnTransformer` ensures:
- Clean preprocessing logic
- No data leakage
- Easy integration into machine learning pipelines

This makes the preprocessing workflow **robust, reproducible, and production-ready**.

