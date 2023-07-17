# Linear regression
This repository holds the final project for the **IBM Linear regression** course, with a colab notebook going through the steps of cleaning the dataset and traning multiple models and comparing the results with each other to find the optimal model to that dataset.

# Dataset
I choose a Housing price in Beijing dataset
- https://www.kaggle.com/datasets/ruiqurm/lianjia

# EDA
It was performed a lot of cleaning on this dataset, there were some features with records holding values with wrong data types, there were values that could not be decoded because were written in chinese alphabet, other than that no outliers were found.

## Feature Scaling
There were some features on different magnitudes of scaling, so it was used StandardScaling() to bring them to same scale.

## Polynomial Features
It was used PolynomialFeatures with degree = 2.

# Linear, Lasso and Ridge
Those three models where trained using the same train test split, and at the end i compared the r2_score of all of them to find the optimal model.

## Alphas
On lasso and ridge i created multiple alphas to find the best one that had the best results on that dataset.
- Ridge
```
ridge_alphas = np.geomspace(0.06, 6.0, 20)
```
- Lasso
```
lasso_alphas = np.geomspace(1e-9, 1e0, num=10)
```

## Regularization
Based on the results, regularization and feature selection didn't had much of a impact on the final results.