# Hackathon-Notebook
This is my first Kaggle competition


In the Kaggle competition, my approach was as follows:

Initial Data Exploration:
I started by examining the training data, which consisted of 3132 rows and 9 columns.
The columns were named A, B, C, D, E, F, G, H, and Target.
Column A was a categorical variable with three categories: M, F, and I.
Columns B, C, D, E, F, G, H, and Target were continuous numeric values.
There were no missing values in any column.

Feature Engineering:
Since the only task was to featurize column A, I used one-hot encoding to convert it into three new columns: A_F, A_I, and A_M.
Since the presence of any two columns among A_F, A_I, and A_M represents the third category, I dropped one column (A_I).

Model Selection:
Before applying any models, I defined a function called rmse(model) to calculate the root mean squared error (RMSE) for a given model.
I split the training data into two parts: 80% for training and 20% for validation.

Model Evaluation:
I applied several models and calculated their respective RMSE values on the validation data:
Ridge (RMSE = 2.441)
KNN (RMSE = 2.165)
GaussianNB (RMSE = 2.986)
SVR (RMSE = 2.147)
DT (RMSE = 2.313)
RF (RMSE = 2.094)
Adaboost (RMSE = 2.291)
XGBoost (RMSE = 2.154)
GBoostingDT (RMSE = 2.145)
Stacking (RMSE = 2.153) - Stacking using the best four models (RF, GB, SVR, XGB) as base models and a meta-model of RandomForest.

Hyperparameter Tuning:
Before applying any model to the test data, I performed hyperparameter tuning for each model using 80% of the training data.
After obtaining the best parameters, I applied each model with the best parameters to the remaining 20% of the training data for validation.

Model Selection and Prediction:
The best result I obtained was with the Random Forest model, which had an RMSE value of 2.094 on the validation data.
I used this model to predict the target variable for the test data.
Overall, this was my first hackathon organized by the AI and Robotics Club as part of their ML.ai course, and I thoroughly enjoyed applying various techniques and concepts that I learned from the course.
