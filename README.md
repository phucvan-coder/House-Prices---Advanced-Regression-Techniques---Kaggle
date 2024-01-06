# House Prices - Advanced Regression Techniques
In this notebook, I will try to predict the sales house prices and practice with feature engineering.

## 1. Loading Dataset
The first stage is loading dataset and we can do it by using pandas library.

We have training dataset (1460 rows and 81 columns) and testing dataset (1459 rows and 80 columns).

## 2. Data Visualization
The next stage is data visualization, we can draw the histogram and boxplot to check the skew and outliers of each feature.

There are many outliers in the dataset, we will keep them because we do not want to lose the important information. 
In order to handle outliers, we can use cross-validation technique. 

## 3. Merge Train and Test
Next stage, we will merge training dataset and testing dataset for data preprocessing, then we will split the data before building model.

## 4. Handling Missing Values
- Handling missing values of numerical features (we will change missing values by mean values of each feature).

- Handling missing values of categorical features (we will change missing values of the features that have the keywords 
'Qual' OR 'Cond' OR 'Qu' OR 'QC', and categorical features that have NA as a correct value into the string "Missing".
The rest of categorical features, we will change missing values into the mode values).

## 5. Feature Engineering
- Drop the id column because we do not need it to train the model.

- Encoding categorical features (we will encode the categorical features where ranking can be applied and the remaining
categorical features will be encode by using pandas.get_dummies() function).

## 6. Train-Test Splitting
Splitting the merged data into training dataset (shape of training data: 1460) and testing dataset (shape of testing data: 1459).

## 7. Feature Scaling
We will scale the training data by using MinMaxScaler.

## 8. Training Model
- we will use Ridge Regression Model which is applied regularization technique to reduce overfitting.

- In order to choose alpha parameter for Ridge Regression model and apply cross-validation technique, we will use GridSearchCV.

## 9. Evaluate The Model
we will use R-squared and Root-Mean-Squared-Error (RMSE) between the logarithm of the predicted value and the logarithm of the 
observed sales price (Taking logs means that errors in predicting expensive houses and cheap houses will affect the result equally).

## 10. Predictions On Testing Data
Finally, we will predict on testing data and export the predicted result into csv file to submit.
