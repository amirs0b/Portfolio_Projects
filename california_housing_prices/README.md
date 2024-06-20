# California Housing Prices Prediction

This repository contains a comprehensive analysis and prediction of housing prices in California using various machine learning models. The project involves data preprocessing, feature engineering, model building, evaluation, and visualization.

## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Handling Outliers](#handling-outliers)
- [Data Normalization](#data-normalization)
- [Model Building and Evaluation](#model-building-and-evaluation)
- [Model Performance Comparison](#model-performance-comparison)
- [Conclusion](#conclusion)

## Introduction

In this project, we use the California Housing Prices dataset to predict housing prices. We train and evaluate the following models:
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Bayesian Ridge Regression

## Data Preprocessing

### Handling Missing Values

We noticed that the `total_bedrooms` column has 207 missing values. We assume these represent houses without any bedrooms, so we fill these missing values with 0.

### Encoding Categorical Variables

The `ocean_proximity` column is a categorical variable. We use one-hot encoding to convert it into a numerical format.

## Feature Engineering

We create new features such as `rooms_per_household`, `bedrooms_per_room`, and `population_per_household` to provide additional information to the model.

## Handling Outliers

Outliers can significantly affect the performance of machine learning models. We cap outliers to a certain percentile to mitigate their impact.

## Data Normalization

After feature engineering, we normalize the numerical features to ensure they are on a similar scale.

### Standardization

We use `StandardScaler` for standardization, which scales the data to have a mean of 0 and a standard deviation of 1.

### Min-Max Normalization

We use `MinMaxScaler` to scale the data between a specific range (e.g., 0 and 1).

## Model Building and Evaluation

We train and evaluate four different models to predict housing prices.

### Linear Regression

- **MAE**: 0.1088
- **MSE**: 0.0211
- **R²**: 0.6098

### Decision Tree Regressor

- **MAE**: 0.1052
- **MSE**: 0.0248
- **R²**: 0.5410

### Random Forest Regressor

- **MAE**: 0.0757
- **MSE**: 0.0126
- **R²**: 0.7678

### Bayesian Ridge Regression

- **MAE**: 0.1088
- **MSE**: 0.0211
- **R²**: 0.6101

## Model Performance Comparison

We visualize the performance of the different models using bar plots.

### Mean Absolute Error (MAE)

![Mean Absolute Error of Models](california_housing_prices/graphs/Plot_MAE.png)

### Mean Squared Error (MSE)

![Mean Squared Error of Models](california_housing_prices/graphs/Plot_MSE.png)

### R² Score

![R² Score of Models](california_housing_prices/graphs/Plot_R2.png)

## Conclusion

Based on our evaluation, the **Random Forest** model performed the best overall, with the lowest MAE and MSE, and the highest R² score. This indicates that **Random Forest** is the most accurate model for predicting housing prices in this dataset. Future work could involve further tuning the hyperparameters of these models and exploring additional feature engineering techniques to improve performance even further.
