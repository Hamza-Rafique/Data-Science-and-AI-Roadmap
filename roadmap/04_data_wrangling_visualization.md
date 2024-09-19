# 📊 Data Wrangling & Visualization for Data Science

Data wrangling and visualization are critical skills in data science. Data wrangling involves cleaning, transforming, and organizing raw data into a format suitable for analysis, while data visualization provides an intuitive way to explore and understand the patterns in the data.

---

## Table of Contents

1. [Introduction to Data Wrangling](#introduction-to-data-wrangling)
2. [Data Cleaning Techniques](#data-cleaning-techniques)
3. [Data Transformation](#data-transformation)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Data Visualization](#data-visualization)
6. [Popular Libraries for Data Wrangling & Visualization](#popular-libraries-for-data-wrangling-visualization)

---

## Introduction to Data Wrangling

Data wrangling, or data preprocessing, is the process of cleaning and transforming raw data into a structured, usable format. Data scientists spend a significant portion of their time on this process to ensure the data is ready for analysis.

### Common Steps:
- **Handling missing values**
- **Removing duplicates**
- **Dealing with outliers**
- **Standardizing formats (dates, strings, etc.)**
  
Data wrangling is essential because poor data quality leads to inaccurate results and models.

Example in Python (using Pandas):

```python
import pandas as pd

# Loading a sample dataset
data = pd.read_csv('data.csv')

# Dropping rows with missing values
cleaned_data = data.dropna()

# Filling missing values with the mean
data_filled = data.fillna(data.mean())
```
## Data Cleaning Techniques

### 1. Handling Missing Data
Missing data can be handled by:

- **Removing missing data:** Deleting rows or columns that contain missing values.
- **Imputation:** Replacing missing data with statistical measures like mean, median, or mode.
  
Example:
```python
# Filling missing values with the column mean
data['column_name'].fillna(data['column_name'].mean(), inplace=True)
```
### 2. Handling Outliers
**a. Remove Outliers**
**Description:** Identify and remove outliers using methods like the IQR (Interquartile Range) method or Z-score.
**Use Case:** When outliers are due to data entry errors or noise.
**Example:**

# Remove outliers using IQR
```python
Q1 = df['Fare'].quantile(0.25)
Q3 = df['Fare'].quantile(0.75)
IQR = Q3 - Q1
df = df[~((df['Fare'] < (Q1 - 1.5 * IQR)) | (df['Fare'] > (Q3 + 1.5 * IQR)))
```
**b. Cap or Transform Outliers**
**Description:** Cap extreme values to a threshold or transform them using methods like log transformation.
**Use Case:** When outliers can't be removed but should be handled.
**Example:**

```python
# Cap outliers in 'Fare'
df['Fare'] = df['Fare'].apply(lambda x: min(x, 300))
```
### 3. Standardization and Normalization**
**a. Standardization**
**Description:** Scale features so that they have the properties of a standard normal distribution with a mean of 0 and a standard deviation of 1.
**Use Case:** When working with models like linear regression or when the data has different units of measurement.
**Example:**
```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
df[['Age', 'Fare']] = scaler.fit_transform(df[['Age', 'Fare']])
b. Normalization
```
**Description:** Scale values between 0 and 1, useful for algorithms like neural networks.
**Use Case:** When features have different ranges and magnitudes.
**Example:**
```python
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df[['Age', 'Fare']] = scaler.fit_transform(df[['Age', 'Fare']])
```
### 4. Handling Duplicate Data
**a. Remove Duplicates**
**Description:** Identify and remove duplicate rows in the dataset.
**Use Case:** When duplicate rows can cause bias or redundancy.
**Example:**
```python
# Remove duplicate rows
df.drop_duplicates(inplace=True)
```
### 5. Encoding Categorical Data
**a. One-Hot Encoding**
**Description:** Convert categorical variables into a binary matrix.
**Use Case:** When categorical variables need to be represented as numerical features for machine learning.
**Example**:

```python
# One-Hot Encoding
df = pd.get_dummies(df, columns=['Sex', 'Embarked'])
```
**b. Label Encoding**
**Description**: Assign a unique number to each category in the categorical feature.
**Use Case:** For ordinal data where categories have an inherent order.
**Example:**
```python
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['Sex'] = le.fit_transform(df['Sex'])
```

### 6. Fix Structural Errors
**Description:** Correct typos, inconsistencies in naming conventions (e.g., 'USA', 'United States', 'US'), or incorrect data types.
**Use Case:** When data contains inconsistent representations of the same information.
**Example:**
```python
# Replace inconsistent values
df['Country'].replace({'US': 'United States', 'USA': 'United States'}, inplace=True)
```

### 7. Handling Incorrect Data Types
**Description:** Convert data to the correct data types (e.g., converting string numbers to integers).
**Use Case**: When numeric data is stored as strings or vice versa.
**Example:**

```python
# Convert data type to integer
df['Age'] = pd.to_numeric(df['Age'], errors='coerce')
```
### 8. Feature Engineering
**Description:** Create new features or modify existing ones to improve model performance. This can include aggregating, scaling, or combining features.
**Use Case:** When existing features don't capture the full complexity of the data.
**Example:**

```python
# Create a new feature 'FamilySize'
df['FamilySize'] = df['SibSp'] + df['Parch'] + 1
```
### 9. Handling Imbalanced Data
**a. Oversampling**
**Description:** Increase the number of samples in the minority class.
**Use Case:** When dealing with imbalanced classification problems.
**Example:**

```python
from imblearn.over_sampling import SMOTE
smote = SMOTE()
X_res, y_res = smote.fit_resample(X, y)
```
**b. Undersampling**
**Description**: Reduce the number of samples in the majority class.
**Use Case:** When the majority class dominates the dataset.
**Example:**
```python
from imblearn.under_sampling import RandomUnderSampler
rus = RandomUnderSampler()
X_res, y_res = rus.fit_resample(X, y)
```

### 10. Binning or Discretization
**Description:** Group continuous variables into bins or categories.
**Use Case:** When you want to reduce the impact of small variations in continuous variables.
**Example:**
```python
 Binning 'Age' into categories
df['AgeGroup'] = pd.cut(df['Age'], bins=[0, 12, 18, 35, 60, 100], labels=['Child', 'Teen', 'YoungAdult', 'Adult', 'Senior'])
```
**Conclusion**
Data cleaning is an essential process in ensuring that the data you work with is reliable, consistent, and ready for analysis or modeling. By using these techniques, you can significantly improve the quality of your dataset, leading to better results in your machine learning models.


