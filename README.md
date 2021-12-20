# Predict the electrical energy output of a Combined Cycle Power Plant 🌱

* Final project from Duke University course "Machine Learning Foundations for Product Managers".
* Created a tool that estimates the output of a power plant (MAPE > 1%).
* Used almost 10k rows dataset and 4 features.
* Explored data to find pattern in order to better feature engineer when modeling. Found helpful correlation via visualization.
* Optimized Linear, Decision tree Regressors to reach the best model. 
* Built a client facing API using flask 

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn 
**For Web Framework Requirements:**  ```pip install -r requirements.txt```  
**Kaggle Notebook:** https://www.kaggle.com/ulyssebot/power-plan-prediciton
**Dataset:** https://archive.ics.uci.edu/ml/datasets/combined+cycle+power+plant


## Data Cleaning
After scraping the data, I needed to clean it up so that it was usable for our model. 


## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 


## Model Building 
First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.   

I tried three different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.   

I tried two different models:
*	**Linear Regression** – Baseline for the model
*	**Decision tree regression** – Turns out to be a good idea. 

## Model performance
The DTR model far outperformed the other approaches on the test and validation sets. 
*	**Linear Regression** : MAPE = 0,6%
*	**Decision tree regression**: MAPE = 0,9%

## Productionization 
I'm planning to design a super simple prototype using streamlit, in order to ask for a city, and using the OpenWeatherMap API it will find the temperature and predict the output in this day and city, using the LR model.



