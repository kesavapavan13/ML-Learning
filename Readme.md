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

