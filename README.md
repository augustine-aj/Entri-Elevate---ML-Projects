# Entri-Elevate---ML-Projects

# Data Preprocessing Project

## Objective
The main objective of this project is to design and implement a robust data preprocessing system that addresses common challenges such as missing values, outliers, inconsistent formatting, and noise. By performing effective data preprocessing, the project aims to enhance the quality, reliability, and usefulness of the data for machine learning.

## Dataset
The dataset used in this project can be accessed here.
https://drive.google.com/file/d/1F3lRf32JM8ejnXq-Cbf9y7fa57zSHGz_/view?usp=sharing

## Key Components

### 1. Data Exploration
- **Loading the Data**: Load the dataset into a pandas DataFrame.
- **Basic Information**: Display basic information such as the number of rows and columns, data types, and memory usage.
- **Unique Values**: List unique values in each feature and their counts.
- **Statistical Analysis**: Perform statistical analysis to understand the distribution of the data.
- **Renaming Columns**: Rename columns for consistency and readability.

### 2. Data Cleaning
- **Missing Values**: Identify missing values and handle them appropriately (e.g., replacing with median values).
- **Duplicate Rows**: Remove all duplicate rows to ensure data integrity.
- **Outliers**: Identify and treat outliers using the IQR method.
- **Specific Value Replacement**: Replace the value 0 in the 'age' column with NaN and handle it.
- **Null Values Treatment**: Treat null values in all columns using suitable measures (e.g., removing rows, or replacing with mean/median/mode).

### 3. Data Analysis
- **Filtering Data**: Filter the data with specific conditions (e.g., age > 40 and salary < 5000).
- **Visualization**: Plot charts to visualize the relationship between features (e.g., age vs salary).
- **Count Representation**: Count the number of people from each place and represent it visually.

### 4. Data Encoding
- **Label Encoding**: Convert categorical variables to numerical representations using label encoding.
- **One-Hot Encoding**: Convert categorical variables to numerical representations using one-hot encoding.

### 5. Feature Scaling (Score: 2)
- **Standard Scaling**: Scale features using StandardScaler to have zero mean and unit variance.
- **Min-Max Scaling**: Scale features using MinMaxScaler to have values between 0 and 1.

## Preprocessing Techniques Explained
- **Handling Missing Values**: Missing values can be filled using various strategies such as mean, median, mode, or even by using prediction models. In this project, we use median for numerical columns.
- **Removing Duplicates**: Duplicate data can cause bias in the analysis. We remove all duplicate rows to maintain data integrity.
- **Encoding Categorical Data**: Machine learning algorithms require numerical input. Categorical data is converted to numerical values using label encoding and one-hot encoding.
- **Feature Scaling**: Scaling is essential for algorithms that rely on distance calculations. We use StandardScaler for standard scaling and MinMaxScaler for scaling features to a range of 0 to 1

## Conclusion
This project provides a comprehensive data preprocessing system that can be applied to enhance the quality and reliability of data for machine learning tasks. By addressing common data challenges, it ensures that the data is well-prepared for subsequent analysis and model development.

# Bangalore House Price Analysis and Outlier Detection

## Project Overview

This project involves analyzing property prices in the city of Bangalore with a focus on the `price_per_sqft` column. The objective is to perform exploratory data analysis (EDA), detect and remove outliers using various methods, check the normality of the data, and investigate the relationships between different variables.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Objectives](#objectives)
4. [Project Workflow](#project-workflow)
    - [1. Basic EDA](#1-basic-eda)
    - [2. Outlier Detection and Removal](#2-outlier-detection-and-removal)
    - [3. Box Plot for Outlier Detection Methods](#3-box-plot-for-outlier-detection-methods)
    - [4. Normality Check and Data Transformation](#4-normality-check-and-data-transformation)
    - [5. Correlation Analysis](#5-correlation-analysis)
    - [6. Scatter Plot Analysis](#6-scatter-plot-analysis)
5. [Results and Observations](#results-and-observations)
6. [Conclusion](#conclusion)
7. [Requirements](#requirements)
8. [Usage](#usage)
9. [Timely Submission](#timely-submission)

## Introduction

Real estate prices in Bangalore vary significantly across different locations and property types. This project aims to understand these variations by analyzing the `price_per_sqft` of properties. The analysis will involve detecting outliers, checking data normality, and investigating the correlations between different variables.

## Dataset

- **File Name**: `house_price.csv`
- **Source**: [Google Drive Link](https://drive.google.com/file/d/1UlWRYU0UglE2ex3iFse0J6eCLEU8g98P/view?usp=sharing)
- **Description**: The dataset contains information on property prices in Bangalore, including features such as location, size, total square footage, number of bathrooms, price, and more.

## Objectives

1. Perform basic exploratory data analysis (EDA).
2. Detect and remove outliers using different statistical methods.
3. Visualize and compare the effectiveness of different outlier removal methods using box plots.
4. Check the normality of the `price_per_sqft` column and perform data transformations if needed.
5. Analyze the correlations between numerical variables using a heatmap.
6. Use scatter plots to further investigate relationships between variables.

## Project Workflow

### 1. Basic EDA

- **Load the Dataset**:
  - Inspect the first few rows of the dataset to understand its structure.
  
- **Check for Missing Values and Data Types**:
  - Identify any missing values in the dataset.
  - Review the data types of each column to ensure they are appropriate for analysis.
  
- **Generate Summary Statistics**:
  - Calculate summary statistics for all numerical columns, including measures such as mean, median, and standard deviation.
  
- **Explore the Distribution of `price_per_sqft`**:
  - Analyze the distribution of the `price_per_sqft` column using visualizations like histograms and KDE plots.

### 2. Outlier Detection and Removal

- **a) Mean and Standard Deviation**:
  - Calculate the mean and standard deviation.
  - Identify outliers as values outside a certain range based on these statistics.
  
- **b) Percentile Method**:
  - Use percentiles (e.g., 1st and 99th) to define outliers.
  
- **c) IQR (Interquartile Range) Method**:
  - Calculate the IQR and define outliers as values beyond 1.5 * IQR from the quartiles.
  
- **d) Z-Score Method**:
  - Calculate the Z-score for each value.
  - Identify outliers as those with a high absolute Z-score.

### 3. Box Plot for Outlier Detection Methods

- **Objective**: Compare the effectiveness of different outlier removal methods.
- **Tasks**:
  - Create box plots for `price_per_sqft` after applying each outlier removal method.
  - Analyze which method provides the best balance between removing outliers and retaining meaningful data.

### 4. Normality Check and Data Transformation

- **Objective**: Check whether the `price_per_sqft` column follows a normal distribution and apply transformations if necessary.
- **Tasks**:
  - Draw a histogram and kernel density estimate (KDE) plot for the `price_per_sqft` column.
  - Calculate skewness and kurtosis before and after transformation.
  - Apply transformations like logarithmic or Box-Cox if the data is highly skewed.

### 5. Correlation Analysis

- **Objective**: Investigate the relationships between numerical variables in the dataset.
- **Tasks**:
  - Calculate the correlation matrix for all numerical columns.
  - Visualize the correlation matrix using a heatmap.

### 6. Scatter Plot Analysis

- **Objective**: Visualize the relationships between pairs of numerical variables using scatter plots.
- **Tasks**:
  - Create scatter plots between pairs of numerical variables (e.g., `total_sqft` vs. `price`).
  - Analyze the patterns and correlations between different variables.

## Results and Observations

- Detailed results and observations will be documented here after performing the analysis.

## Conclusion

- Summarize the findings of the project, including the most effective outlier removal method, the normality of the data, and any significant correlations between variables.

## Requirements

- **Python 3.x**
- **Libraries**:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scipy

## Usage

1. Clone the repository or download the project files.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run the Jupyter Notebook or Python script provided in the repository.
4. Follow the code and explanations to perform the analysis.


