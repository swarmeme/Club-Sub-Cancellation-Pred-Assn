# Membership Woes Data Analysis

## Introduction

This Python script analyzes membership data to gain insights into membership cancellations using the pandas, scikit-learn, and seaborn libraries. The analysis includes data preprocessing, visualization, and training a Random Forest Classifier for predicting membership status.

## Usage

### Dependencies

Make sure you have the following libraries installed:

- pandas
- scikit-learn
- seaborn
- matplotlib

You can install them using the following:

``bash
pip install pandas scikit-learn seaborn matplotlib

## Analysis Steps

### 1. Data Loading and Exploration:

- **Objective:** Understand the structure and basic characteristics of the membership data.

- **Steps:**
  - Load the membership data from the CSV file using `pd.read_csv`.
  - Display basic information about the data using `head()` and `info()` functions.
  - Check for null values using `isnull()` and `sum()`.

### 2. Data Preprocessing:

- **Objective:** Prepare the data for analysis and modeling.

- **Steps:**
  - Remove null values from specific columns.
  - Analyze and drop unnecessary columns based on data distribution.

### 3. Exploratory Data Analysis (EDA):

- **Objective:** Gain insights into the data through visualizations.

- **Sub-Sections:**
    1. **Cancellation Status by Marital Status:**
       - Visualize cancellation status distribution by marital status using `seaborn.countplot`.

    2. **Average Annual Income Analysis:**
       - Compare average annual income for cancelled and in-force memberships using `seaborn.barplot`.

    3. **Payment Mode and Membership Status:**
       - Visualize the relationship between payment mode and membership status using `seaborn.countplot`.

    4. **Member Age at Issue Analysis:**
       - Analyze member age at issue for different membership statuses using `seaborn.boxplot`.

    5. **Income-to-Fee Ratio Visualization:**
       - Calculate and visualize income-to-fee ratio by membership status using `seaborn.barplot`.

    6. **Cancelled Members by Gender:**
       - Explore cancelled members distribution by gender using `value_counts()` and visualization.

### 4. Outlier Detection (Optional):

- **Objective:** Identify and examine outliers in the data.

- **Steps:**
  - Calculate z-scores for annual income using `zscore` from `scipy.stats`.
  - Identify and examine outliers based on z-scores.

### 5. Machine Learning Model:

- **Objective:** Train a model to predict membership status.

- **Steps:**
  - Prepare features and target variables.
  - Encode categorical data using `pd.get_dummies`.
  - Split the data into training and testing sets with `train_test_split`.
  - Train a Random Forest Classifier using `RandomForestClassifier`.
  - Evaluate the model's accuracy using `accuracy_score`.

### 6. Confusion Matrix:

- **Objective:** Evaluate the model's performance using a confusion matrix.

- **Steps:**
  - Calculate the confusion matrix using `confusion_matrix` from `sklearn.metrics`.
  - Display the confusion matrix for further analysis.
