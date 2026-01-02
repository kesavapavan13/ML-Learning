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

---

## 🔹 7. Image Preprocessing

This notebook demonstrates essential **image preprocessing techniques** required before applying computer vision or image-based machine learning models.  
These steps ensure images are correctly formatted, consistent, and model-ready.

---

### 🔹 Key Operations

- **Color Space Conversion (BGR → RGB)**  
  Ensures accurate image visualization when using OpenCV and Matplotlib.

- **Image Resizing**  
  Standardizes image dimensions and reduces computational overhead.

- **Image Rotation**  
  Adjusts image orientation and supports basic data augmentation.

- **Image Cropping (Zooming)**  
  Focuses on important regions of interest within an image.

- **Drawing Shapes on Images**  
  Highlights objects or regions for visual inspection and localization.

---

### 🔹 Libraries Used

- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

#### Outcome

After preprocessing, images are:

- Correctly formatted and aligned  
- Consistent in size and structure  
- Focused on relevant regions  
- Ready for visualization and machine learning tasks  

---

---

## 🔹 8. Image & Video Data Preprocessing

This notebook covers **fundamental preprocessing techniques for both images and videos**, which are essential for computer vision and deep learning applications.  
The objective is to convert raw visual data into a clean, consistent, and usable format.

---

### 🔹 Key Operations

#### Image Preprocessing
- Color space conversion for correct visualization  
- Image resizing to maintain uniform dimensions  
- Basic transformations such as rotation and cropping  
- Drawing shapes to highlight regions of interest  

#### Video Preprocessing
- Loaded video files and extracted frames  
- Read videos frame-by-frame using OpenCV  
- Applied image preprocessing techniques to video frames  
- Displayed and analyzed processed frames  

---

### 🔹 Libraries Used

- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

#### Outcome

After preprocessing, image and video data are:

- Properly formatted and standardized  
- Frame-wise accessible for analysis  
- Suitable for computer vision and deep learning models  
- Ready for tasks such as:
  - Video analysis  
  - Object detection  
  - Action recognition  

---



## ✅ Final Outcome

After completing the complete preprocessing pipeline, the project delivers **clean, consistent, and model-ready data** across multiple data types.

### Tabular Data
- Cleaned and consistent dataset  
- Missing values handled using **median (numerical)** and **mode (categorical)**  
- Robust outlier treatment using IQR-based capping  
- Fully numerical, scaled, and encoded features  
- Optimized feature set through numerical and categorical feature selection  

### Image & Video Data
- Correct color space representation (BGR → RGB)  
- Standardized image resizing and transformations  
- Region-focused preprocessing through cropping and annotations  
- Video data converted into frame-wise, analyzable format  

---

## 🚀 Ready For

- Exploratory Data Analysis (EDA)  
- Feature Engineering  
- Machine Learning & Deep Learning Model Training  
- Computer Vision tasks (Image & Video-based)  

---

## 📌 Key Highlights

- Median imputation ensures robustness against outliers  
- IQR-based outlier handling preserves real-world data patterns  
- ColumnTransformer enables scalable and leakage-free preprocessing  
- Feature selection improves model efficiency and interpretability  
- Image and video preprocessing follow standard computer vision practices  
- Workflow aligns with **industry-standard, production-ready ML pipelines**


