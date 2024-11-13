# **Cameroon Air Quality Prediction - AutoGluon**

## Introduction

This study focuses on predicting air quality in Cameroon, specifically the concentration of particulate matter (**PM2.5**), using various machine learning techniques. The dataset includes weather and air quality features collected from different cities across Cameroon.

## Leaderboard Achievement

Here’s a snapshot of my position on the leaderboard during the **Cameroon Air Quality Prediction** competition:

## Methodology

The analysis began with an exploration of the dataset, where **data inconsistencies** were addressed. Features with a **single value**, such as **'sunrise'**, **'sunset'**, and **'snowfall_sum'**, were removed. Redundant variables, including **city**, **longitude**, and **latitude**, were also eliminated to reduce unnecessary complexity in the models.

### Feature Engineering

To enhance predictive power, we analyzed the distribution of **PM2.5** concentrations across different cities. This led to the creation of a new feature:  
- **Distance of each city from Bafoussam** (the city with the highest PM2.5 levels).

## Models

Several machine learning models were initially employed to predict **PM2.5** levels, including:

- **CatBoost**
- **LightGBM (LGBM)**
- **XGBoost (XGB)**
- **GradientBoostingRegressor**
- **ExtraTreesRegressor**
- **RandomForestRegressor**
- **AdaBoostRegressor**
- **MLPRegressor**

These models were evaluated using a **9-split RepeatedKFold cross-validation** strategy to ensure reliable results.

However, after initial testing, **AutoGluon** was introduced and ultimately provided the best performance, surpassing all other models in predictive accuracy.

## Results

Among all models tested, **CatBoost** performed well, achieving a **root mean squared error (RMSE)** of **3.11078**. However, **AutoGluon** outperformed every other model, achieving the **lowest RMSE of 2.97008**.

### Key Result Comparison

| Model                     | RMSE      |
| -------------------------- | --------- |
| **CatBoost**               | 3.11078   |
| **AutoGluon**              | **2.97008** |

This result demonstrates a **significant improvement** over the other models, indicating the superior predictive capabilities of **AutoGluon** for this particular task.

While other models, such as **CatBoost** and **ExtraTrees**, provided competitive results, **AutoGluon’s automatic model selection and hyperparameter tuning** led to the best performance, further validating its effectiveness as an **AutoML tool** for air quality prediction.

## Conclusion

This study highlights the critical role of **feature engineering** in improving model performance, as well as the superiority of **AutoGluon** over other machine learning models for the task of predicting **PM2.5** concentrations. AutoGluon’s automated approach to model selection and optimization resulted in a more accurate prediction, achieving the best RMSE score and outperforming traditional models like **CatBoost** and **XGBoost**.
