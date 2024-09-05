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
