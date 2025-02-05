**OVERVIEW**
This project explores a dataset from Kaggle. The original dataset contained information on 3 million used cars. The provided dataset contains information on 426K cars to ensure speed of processing.  
The goal is to understand what factors make a car more or less expensive.  As a result of your analysis, you should provide clear recommendations to your client -- a used car dealership -- as to what consumers value in a used car.
### CRISP-DM Framework
To frame the task, throughout our practical applications, we will refer back to a standard process in industry for data projects called CRISP-DM.  This process provides a framework for working through a data problem. 
The first step in this application will be to read through a brief overview of CRISP-DM.
CRISP-DM starts with understanding a business problem:
## Business Understanding
From a business perspective, we are tasked with identifying key drivers for used car prices.  
The objective is to build a predictive model that estimates the price of used cars based on multiple features 
(such as the year of manufacture, region, condition, fuel,size and others). 
We will use historical data on used car sales, where the price is the target variable (dependent variable), and the car attributes (e.g., year, region, condition or other) are the features (independent variables). 
The model aims to identify the relationship between these features and the target variable (price) and predict the price of unseen cars based on these characteristics. 
We will apply techniques such as data preprocessing, feature engineering, and regression algorithms, 
evaluating the model's performance through metrics like Mean Squared Error (MSE), R-squared, and Root Mean Squared Error (RMSE).
### Data Understanding
After considering the business understanding, we want to get familiar with our data.  Write down some steps that you would take to get to know the dataset and identify any quality issues within.  
Take time to get to know the dataset and explore what information it contains and how this could be used to inform your business understanding.
In order to understand data, the below sequential steps will be followed:
1. Load data
2. check and remove duplicate rows
3. Analyze data for missing values and outliers
4. Visualize data for exploratory analysis of relationship between features contributong to the price
## Data Preparation
After our initial exploration and fine-tuning of the business understanding, it is time to construct our final dataset prior to modeling.  Here, we want to make sure to handle any integrity issues and cleaning, 
the engineering of new features, any transformations that we believe should happen (scaling, logarithms, normalization, etc.), and general preparation for modeling with `sklearn`. 
Part of this step, is to split data into train and test set,encode,fit and transform data that can be used for the machine learning model.
### Modeling
With your near to final dataset in hand, it is now time to build some models.  
Here, data is first feature scaled and modelled useding LinearRegression, this is a basic model for predictive analysis. 
Using LinearRegression the model evaluation metrics such as Mean absolute error,Mean Squared error and R-squared error are evaluated.
According to this for the car price prediction, the values determined are
Model Evaluation:
Mean Absolute Error (MAE): 8089.921633536004
Mean Squared Error (MSE): 115934567.77538289
R-squared (R²): 0.32823662329297976
This is followed by determining coefficients that indicates the features contributing to the used car sales price.
Feature scaled regression score:0.32823662329297987
**Evaluation**
To evaluate the root mean squared error is determined 
Root Mean Squared Error (RMSE): 10767.29157102114
RMSE is a measure of the average magnitude of error between the model's predictions and the actual values. In this case,
RMSE of 10767.29, indicates model is off by $10767 of the predicted used car price.
**Cross-Validation**
GridSearchCV is used for cross-validating the model 
Model Evaluation:
Mean Absolute Error (MAE): 8089.921633536006
Mean Squared Error (MSE): 115934567.77538288
R-squared (R²): 0.32823662329297987
Ridge Regression and Lasso Regression are other mutiple regression models that were used to model as well.
**Conclusion**
Given that the RMSE is a bit high and the R² is only 0.32, the model is not perfect, but it already offers clear insights into which factors are driving used car prices. 
Based on further fine tuning other aspects of preprocessing the data such as improved feature extraction by creating new features from existing ones
Processing textual data: Converting text into word embeddings (TFIDF, GloVe, Word2Vec, BERT) or n-grams, we would be able to provide more accurate insights on the model and sales price of used cars.
To conclude , according to the linearRegression model used the features that predict the used car price are:
*Transmission
*Year
*cylinders
*condition
*paint_color
*type
*model
