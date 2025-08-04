# python_internship_task1

AI & ML Internship Task 1: Data Cleaning & Preprocessing
This repository contains my submission for Task 1 of the Elevate AI & ML Internship. I selected the House Prices - Advanced Regression Techniques dataset from Kaggle, which provides a comprehensive set of real-world features with significant missing values, categorical variables, and numerical data requiring thorough preprocessing.

Approach
In the Jupyter notebook (preprocessing_notebook.ipynb), I implemented the required steps using Python, Pandas, NumPy, Matplotlib, and Seaborn. Initially, I loaded the train.csv file and conducted exploratory analysis, including dataset shape (1,460 rows, 81 columns), data types (integers, floats, and objects), and missing value counts—columns such as PoolQC exhibited over 99% nulls.

For handling missing values, I applied imputation techniques: median for numerical features to mitigate skewness and mode for categorical features to maintain data integrity. Encoding followed, with LabelEncoder for ordinal variables (e.g., ExterQual, reflecting inherent ordering) and one-hot encoding via get_dummies for nominal variables (e.g., Neighborhood), incorporating a drop_first parameter to prevent multicollinearity.

Feature scaling was achieved through standardization using StandardScaler on numerical columns (excluding the target SalePrice), ensuring zero mean and unit variance for optimal model compatibility. Outlier detection involved generating boxplots for critical features like GrLivArea and SalePrice, followed by removal using the interquartile range (IQR) method to enhance data quality.

Before-and-after visualizations and statistics were included to demonstrate the effectiveness of each transformation, resulting in a fully prepared dataset suitable for machine learning applications such as price prediction.

Repository Contents
preprocessing_notebook.ipynb: Core notebook with code, explanations, and visualizations.

train.csv: Original Kaggle dataset.

cleaned_data.csv: Preprocessed output file.

Execution Instructions
Open preprocessing_notebook.ipynb in Google Colab. Upload train.csv if necessary and execute the cells sequentially. No additional installations are required beyond standard libraries.
