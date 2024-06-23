# CODETECH-TASK1-Data-processing
NAME: ABHINAV KAUSHIK
COMPANY: CODTECH IT SOLUTION
ID: CT08SP1029
DOMAIN: ARTIFICIAL INTELLIGENCE

## Overview of the project

This project focuses on data preprocessing, a crucial step in preparing a dataset for machine learning model training. The specific steps demonstrated in this project include handling missing values, encoding categorical variables, splitting the data into training and testing sets, and scaling features. Here’s an overview of each step:

1. Data Handling and Creation
A sample DataFrame is created to simulate a dataset that contains missing values and categorical data. The DataFrame includes three columns:

age: Numerical values with some missing entries.
salary: Numerical values with some missing entries.
department: Categorical values with some missing entries.
2. Handling Missing Values
To address missing values, different strategies are applied:

Numerical columns (age and salary) are imputed using the mean value of each column. This is done using the SimpleImputer from sklearn with the strategy set to 'mean'.
The categorical column (department) is imputed using the mode (the most frequent value) of the column.
3. Encoding Categorical Variables
Categorical variables need to be converted into a numerical format suitable for machine learning algorithms. This is done using one-hot encoding:

The pd.get_dummies function is used to transform the department column into binary columns, dropping the first category to avoid the dummy variable trap.
4. Splitting Data into Features and Target Variable
The dataset is split into:

Features (X): All columns except the target variable (salary).
Target variable (y): The salary column.
5. Splitting the Dataset into Training and Testing Sets
The data is divided into training and testing sets using train_test_split from sklearn:

80% of the data is used for training (X_train and y_train).
20% of the data is used for testing (X_test and y_test).
6. Feature Scaling
Feature scaling is crucial to ensure that numerical features contribute equally to the model. This is done using StandardScaler from sklearn:

The scaler is fitted on the training data and then used to transform both the training and testing data to ensure that the model does not have access to the testing data during training.
Output and Results
The script prints the features before and after scaling for both the training and testing sets to demonstrate the effect of feature scaling.

##Summary
This project showcases a fundamental process in data preprocessing, ensuring that the data is clean, well-formatted, and appropriately scaled for machine learning models. Each step in the process is crucial for building robust and accurate models.
