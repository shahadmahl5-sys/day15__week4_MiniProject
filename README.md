# Data Cleaning Mini Project – Day 15

## Project Description
This project focuses on cleaning a real-world dataset from raw data to an analysis-ready dataset.  
The goal is to apply data cleaning techniques such as handling missing values, treating outliers, cleaning text fields, and processing dates.

The final result is a clean dataset that can be used for data analysis or machine learning.

---

## Dataset Issues
The raw dataset contained several common real-world problems:

- Missing values in numeric columns (age, income)
- Outliers in income values
- Inconsistent text formatting in city names
- Date/time values without proper timezone
- Mixed or incorrect data types

---

## Cleaning Steps

### 1. Data Type Conversion
- Converted age and income to numeric
- Converted signup_time to datetime

Reason:
Ensures correct calculations and analysis.

---

### 2. Handling Missing Values
- Filled missing age with median
- Filled missing income with median
- Created indicator columns for missing values

Reason:
Median is less sensitive to outliers than mean.

---

### 3. Outlier Treatment
- Capped age at 99th percentile
- Applied log transformation to income
- Capped transformed income at 99th percentile

Reason:
Reduces the influence of extreme values while keeping all records.

---

### 4. Text Cleaning
- Trimmed spaces
- Converted city names to lowercase

Reason:
Prevents duplicate categories caused by formatting differences.

---

### 5. Date Cleaning
- Converted signup_time to timezone-aware (UTC)

Reason:
Ensures consistency in time-based analysis.

---

## Trade-offs and Limitations
- Capping may hide some true extreme values
- Median imputation reduces data variability
- Log transformation makes values less interpretable

---

## Impact on Machine Learning
These cleaning steps help:

- Improve model stability
- Reduce noise from outliers
- Improve generalization
- Prevent bias from extreme values
- Ensure consistent feature formatting

---

## Final Output
The cleaned dataset is saved as:

cleaned_dataset.csv

This dataset is ready for analysis or machine learning.

---

## Tools Used
- Python
- Pandas
- NumPy

---

## Author
Shahad Alharbi – Mini Project Week 4
