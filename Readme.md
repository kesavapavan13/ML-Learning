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

## 3.2 Handling Outliers

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


# 5.📘 Data Preprocessing – Column Transformation Using Functions

This notebook extends the data preprocessing pipeline by implementing **column-wise feature transformations using reusable functions**.  
It follows earlier preprocessing steps such as **missing value handling** and **outlier treatment**, ensuring a clean and structured workflow before model training.

---

## 🔹 Objective

To design a **modular, reusable, and scalable preprocessing approach** by:
- Separating numerical and categorical features
- Applying appropriate transformations using functions
- Integrating all transformations using `ColumnTransformer`
- Producing a fully numerical, model-ready dataset

---

## 🔹 Dataset Preparation (Continuity)

- 📂 Used the cleaned dataset obtained after:
  - Handling missing values  
  - Treating outliers  
- 🔍 Inspected dataset structure, shape, and data types  
- 🧾 Ensured only relevant features were passed for transformation  

---

## 🔹 Feature Categorization

- **Numerical (Continuous) Features**
  - Identified using `select_dtypes(include=np.number)`
  - Scaled to ensure uniform feature contribution

- **Categorical Features**
  - Identified using `select_dtypes(include=object)`
  - Encoded based on feature semantics

---

## 🔹 Functional Preprocessing Design ⭐

To improve code maintainability and reusability, preprocessing logic was implemented using **custom functions**, including:
- Function to identify numerical and categorical columns  
- Function to apply scaling on numerical features  
- Function to apply appropriate encoding on categorical features  
- Function to construct and apply `ColumnTransformer`

This approach aligns with **industry-level ML preprocessing standards**.

---

## 🔹 Encoding Techniques Applied

Different encoding strategies were applied based on the nature of categorical features:

- **Label Encoder**
  - Used for binary or limited nominal categorical features

- **Ordinal Encoder**
  - Used for features with inherent order

- **OneHotEncoder**
  - Used for nominal categorical features
  - `sparse_output=False` to generate dense output

---

## 🔹 Column Transformation

- Combined all preprocessing steps using **`ColumnTransformer`**
- Applied transformations in a single pipeline using `fit_transform()`
- Ensured:
  - No data leakage  
  - Consistent preprocessing  

---

## 🔹 Output

- Transformed data converted into a Pandas DataFrame
- Final dataset becomes:
  - Fully numerical  
  - Scaled and encoded  
  - Clean and consistent  
  - Ready for machine learning models  

---

## 🔹 Libraries Used

- 🐼 **Pandas** – data loading and manipulation  
- 🔢 **NumPy** – numerical operations  
- 🤖 **Scikit-learn**
  - `ColumnTransformer`
  - `StandardScaler`
  - `LabelEncoder`
  - `OrdinalEncoder`
  - `OneHotEncoder`

---

## ✅ Outcome

After completing this step, the preprocessing pipeline becomes:

- Modular and reusable  
- Production-ready  
- Robust against data inconsistencies  
- Suitable for:
  - Exploratory Data Analysis (EDA)
  - Feature Engineering
  - Machine Learning Model Training

---

## 📌 Note

Implementing preprocessing using **functions + ColumnTransformer**:
- Improves code clarity
- Enhances reusability
- Simplifies pipeline integration
- Reflects real-world ML workflow practices

# 6. 📘 Data Preprocessing – Feature Selection (Numerical Features)

This notebook focuses on **selecting the most relevant numerical features** using statistical and information-theoretic methods.  
Feature selection helps improve model performance, reduce dimensionality, and enhance interpretability.

This step is performed **after**:
- Handling missing values  
- Outlier treatment  
- Column transformation  

---

## 🔹 Objective

To identify and retain important numerical features that contribute significantly to the target variable while removing redundant or less informative features.

---

## 🔹 Dataset Preparation

- Used the cleaned and transformed dataset from the preprocessing pipeline  
- Separated independent variables (**X**) and target variable (**y**)  
- Considered only numerical features for selection  

---

## 🔹 Feature Selection Techniques Applied

### 6.1 Correlation Analysis

```python
# Compute correlation matrix
corr_matrix = df.corr()

# Visualize correlations
plt.figure(figsize=(12, 8))
sns.heatmap(corr_matrix, cmap='coolwarm', annot=False)
plt.title("Correlation Heatmap of Numerical Features")
plt.show()


from sklearn.feature_selection import VarianceThreshold

# Apply Variance Threshold
var_thresh = VarianceThreshold(threshold=0)
X_var = var_thresh.fit_transform(X_num)

# Retained features
retained_features = X_num.columns[var_thresh.get_support()]
retained_features

from sklearn.feature_selection import mutual_info_regression

# Calculate Mutual Information scores
mi_scores = mutual_info_regression(X_num, y, random_state=42)

# Create MI score DataFrame
mi_df = pd.DataFrame({
    'Feature': X_num.columns,
    'MI_Score': mi_scores
}).sort_values(by='MI_Score', ascending=False)

mi_df


## ✅ Outcome

After numerical feature selection, the dataset becomes:

- Optimized with informative numerical features  
- Reduced in dimensionality  
- Less redundant and noise-free  
- Ready for efficient machine learning model training  

---

## 📌 Note

Feature selection improves:

- Model generalization  
- Training efficiency  
- Interpretability  

This completes the **feature preparation stage of the preprocessing pipeline**.


