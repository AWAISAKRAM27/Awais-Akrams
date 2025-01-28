# Data Cleaning Process for `apple_sales_2024.csv`

## Introduction
This document provides a comprehensive overview of the data cleaning process performed on the `apple_sales_2024.csv` dataset. The goal of this process is to ensure that the dataset is accurate, consistent, and ready for analysis. The steps outlined below describe the methods and techniques used to inspect, clean, and prepare the data.

## Overview
This document outlines the data cleaning process performed on the dataset `apple_sales_2024.csv` using Python. The purpose of this process is to ensure the dataset is clean, consistent, and ready for analysis.

## Steps in the Cleaning Process

### 1. Importing Libraries
To handle data manipulation and analysis, the Pandas library was imported:
```python
import pandas as pd
```

### 2. Loading the Dataset
The dataset was loaded from a CSV file named `apple_sales_2024.csv`:
```python
data = pd.read_csv("apple_sales_2024.csv")
```

### 3. Inspecting the Data
The structure and basic properties of the dataset were examined using the following methods:
- **Columns in the dataset:**
  ```python
  data.columns
  ```
- **First few rows:**
  ```python
  data.head()
  ```
- **Last few rows:**
  ```python
  data.tail()
  ```
- **Random sample of rows:**
  ```python
  data.sample()
  ```
- **Dataset information:**
  ```python
  data.info()
  ```
- **Statistical summary:**
  ```python
  data.describe()
  ```

### 4. Detailed Statistical Analysis
A detailed statistical summary, including categorical data, was generated using:
```python
y = data.describe(include="all")
```
Further insights were extracted using:
- **Top and max values:**
  ```python
  y.loc[["top", "max"]]
  ```
- **Specific rows of summary statistics (example indices):**
  ```python
  y.iloc[[0, 4, 8]]
  ```

### 5. Handling Missing Values
Missing values in each column were identified using:
```python
data.isnull().sum()
```

### 6. Analyzing Categorical Columns
- **Value counts for the `Region` column:**
  ```python
  data["Region"].value_counts()
  ```
- **Value counts for the `State` column:**
  ```python
  data["State"].value_counts()
  ```

### 7. Visualizing Data
- **Bar plot for `State` column:**
  ```python
  data["State"].value_counts().plot(kind="bar", title="State", color="purple")
  ```
- **Pie chart for `Region` column:**
  ```python
  data["Region"].value_counts().plot(kind="pie", title="Region", color="red")
  ```

### 8. Saving the Cleaned Dataset
The cleaned dataset was saved to a new CSV file named `data(new).csv`:
```python
data.to_csv("data(new).csv")
```

## Summary
The cleaning process included inspecting, analyzing, and visualizing the dataset, along with handling missing values. The cleaned data is now saved in `data(new).csv` and is ready for further analysis or modeling.

## Feedback
If you have any feedback or suggestions regarding the data cleaning process or this document, please feel free to share.

---
**Author:** Awais Akram
