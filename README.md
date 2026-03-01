# highnote

This repository contains a comprehensive machine learning workflow (R Markdown) designed to identify high-value users for HighNote, a digital music service. The primary objective is to predict which "free" users are most likely to convert to "premium" subscribers.

Data Privacy
Please note that the dataset used in this analysis is private and subject to non-disclosure agreements. As such, the raw data files are not included in this repository. The .Rmd file serves as a demonstration of the analytical framework and coding standards.

Project Overview
HighNote faces the classic freemium challenge: identifying the right users to target for conversion without wasting marketing spend. This project utilizes an anonymized dataset to build a predictive pipeline that ranks users by their conversion probability.

Key Objectives:
Predictive Modeling: Identify the top 1,000 free users most likely to upgrade.
Class Imbalance Handling: Address the naturally low conversion rate using SMOTE (Synthetic Minority Over-sampling Technique).
Profit Optimization: Move beyond simple accuracy to focus on business-centric metrics like precision and expected profit.

Technical Stack
Language: R
Libraries: tidyverse, caret, randomForest, xgboost, ROSE (for SMOTE), pROC.
Models Evaluated: * Logistic Regression (Baseline)
Random Forest
XGBoost (Extreme Gradient Boosting)

Methodology & Features
The analysis follows a standard data science lifecycle:
Exploratory Data Analysis (EDA): Visualizing user demographics and activity patterns (e.g., playlists created, friends on the platform).
Feature Engineering: Treatment of skewed activity data and categorical encoding.
Resampling: Implementing SMOTE to ensure the models effectively learn the characteristics of the minority "converter" class.
Evaluation: Models were compared based on AUC-ROC and their ability to maximize the conversion rate within the top decile of predicted users.

Results
The final model (XGBoost/Random Forest) successfully identified a target segment with a significantly higher conversion lift compared to a random baseline, providing a data-driven foundation for HighNote's marketing strategy.
