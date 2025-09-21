# Kaggle Playground Series Competition Notebooks

Attached to my repository are the Kaggle notebooks I created for various competitions in the Playground Series. These competitions provide an excellent opportunity to refine my data science skills, and I’m excited to share my work here.

Out of the seven competitions I participated in, I achieved top rankings in two classification problems, placing in the **top 4%** and **top 10%** among thousands of competitors. Below is a brief overview of these competitions:

## 1. Early Prediction of At-Risk Students (Academic Success) 

In this competition, the goal was to develop a predictive model that identifies students at risk of underperforming or dropping out. I worked with a dataset of over 80,000 student records, featuring various demographic and academic variables. Here, I achieved an accuracy of **83.76%** using a stacked ensemble model that combined the two models - tuned XGBoost and tuned LightGBM. This placed me in the **top 4% of competitors** (107th out of 2,691).

Key techniques I used in this model include:
  
- I used Stratified 5-fold cross-validation to ensure the model was robust across different demographics, particularly addressing class imbalances and ensuring that the model's performance was generalized (below is the imbalanced distribution of the label classes).
<p align="center">
  <img width="614" height="468" alt="image" src="https://github.com/user-attachments/assets/42765292-c063-4a21-8b3f-a334876810d9" />
</p>


- I also used SHAP values and feature importances to evaluate the contribution of individual models, which helped me decide how best to combine them for improved generalization in the final ensemble.
### LGBM feature importance (The x-axis is supposed to show the name of each feature, not the best graph ever, I apologize)
<p align="center">
  <img width="614" height="468" alt="image" src="https://github.com/user-attachments/assets/c24a58e5-3332-4cce-a642-9359f75d5b1a" />
</p>

### XGB feature importance (same thing here)
<p align="center">
  <img width="614" height="468" alt="image" src="https://github.com/user-attachments/assets/1eabcc1c-e48d-4b83-95c2-aa67eec60fa7" />
</p>


## 2. Identifying Introverts vs. Extroverts

The second competition challenged participants to predict whether individuals were introverts or extroverts based on a dataset of roughly 19,000 samples. I achieved an accuracy of 96.90% using a straightforward LightGBM model augmented with effective feature engineering. This effort earned me a place in the top 10% (473rd out of 4,331 competitors).

Key aspects of this project included:

- Thorough feature engineering to extract meaningful insights from raw data, as well as proper handling of categorical variables. Here, I discovered that certain encodings (e.g., OneHotEncoder) could lead to the misinterpretation of categorical variables, especially when their relationship with other features should be ordinal.

- With a smaller dataset, the risk of overfitting was higher when using Optuna for hyperparameter tuning. To combat this, I implemented a method to check the standard deviation between folds during cross-validation, ensuring the model's accuracy remained stable across splits and helping me select the best model for submission. Below is a screenshot comparing the average accuracy and standard deviation of those accuracies between folds.

<p align="center">
  <img width="704" height="234" alt="image" src="https://github.com/user-attachments/assets/64794ba9-3cf5-4f07-ba5d-8812b5829bf5" />
</p>


## Key Learnings and Skills Developed

- Data Preprocessing & Feature Engineering: I have become experienced at normalizing columns to account for differences in range, encoding categorical variables effectively, and selecting/creating meaningful features through analyzing the distribution of numerical/categorical data, the correlation matrix for multicollinearity, and mutual infos.

- Boosted Models and Ensemble Models: I gained deep experience with popular boosted models like LightGBM, XGBoost, and CatBoost, learning how to combine them effectively through the performance of each model individually and their feature importances.

- Hyperparameter Tuning and Cross-validation: By integrating Optuna for hyperparameter optimization and using cross-validation for robust evaluation, I was able to significantly improve model accuracy without overfitting.

**NOM**
