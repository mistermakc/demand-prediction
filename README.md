# Demand Prediction

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Objective

The objective of this project is to build a model to predict demand based on promotions and calculate baselines for predicting revenue uplift in a specific category.

## Table of Contents

- [1. Data Collection](#1-data-collection)
- [2. Data Preparation](#2-data-preparation)
- [3. Data Cleaning & Feature Engineering](#3-data-cleaning--feature-engineering)
- [4. Data Modeling](#4-data-modeling)
- [5. Interpretation](#5-interpretation)

## 1. Data Collection

The data collection section involves importing necessary libraries and reading data from multiple files. The following libraries are imported:

- pandas
- numpy
- matplotlib
- seaborn
- scipy.stats
- xlrd
- matplotlib.dates
- sklearn

The data is read from various files using the `read_fwf` and `read_excel` functions from pandas.

## 2. Data Preparation

In the data preparation section, the code performs merging and concatenation of dataframes. The following operations are performed:

- Merging stores and groceries dataframe.
- Merging main and product dataframes.
- Creating a new column for UPC creation.
- Merging the main dataframe with the product attributes dataframe.
- Checking the length of the dataset and verifying the concatenation.
- Dropping unnecessary columns from the merged dataframe.

## 3. Data Cleaning & Feature Engineering

The data cleaning and feature engineering section involve cleaning the data and creating new features. The following operations are performed:

- Creating an average price variable.
- Visualizing the correlation matrix heatmap.
- Filtering data for baseline and promotion.
- Applying rolling max function to calculate maximum average price.
- Filling missing values and creating discount column.

## 4. Data Modeling

The data modeling section involves training and evaluating machine learning models. The following operations are performed:

- Dropping unnecessary columns.
- Computing quarters and cyclical features for month and day.
- Defining a function for Mean Absolute Percentage Error (MAPE).
- Defining a preprocessor and models.
- Setting up GridSearchCV for hyperparameter tuning.
- Splitting the data into train and test sets.
- Training and evaluating models using GridSearchCV.

## 5. Interpretation

The Lasso Lars model performed well in our evaluation, explaining approximately 86.35% of the variance in the target variable (explained variance score of 0.8635) and achieving an R2 score of 0.8629. However, there is room for improvement as indicated by the Mean Absolute Error (MAE) of 141, Mean Squared Error (MSE) of 76,910, and Mean Absolute Percentage Error (MAPE) of 40.82%. While the model shows a strong positive linear correlation (Pearson coefficient of 0.9306) with actual values, it occasionally generates predictions significantly deviating from the actual values. Further enhancements are required to reduce prediction errors.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
