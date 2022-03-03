
# Flight Price Prediction

Create a tool that predict Flight price to users look for best prices when booking flight tickets.
Created a tool that estimates Flight Prices to help users look for best prices when booking flight tickets.
Engineered features from the Departure Time, Date of Journey, to quantify the data and make it more understandable.
Optimized multiple Regression models using RandomSearchCV to reach the best model.
Built a client facing API using flask.




## Code and Resources used
>-Python Version: 3.9
-Packages: pandas, numpy, sklearn, matplotlib, seaborn, flask, json, pickle
For Web Framework 
>-Requirements: pip install -r requirements.txt
-Dataset: https://www.kaggle.com/nikhilmittal/flight-fare-prediction-mh
## Cleaning the data and EDA
I needed to clean it up so that it was usable for our model. I made the following changes and created the following variables:

-Made Columns for Day and Month out of Date of Journey
-Calculated the total flight duration
-Removed the null values
-Removed the outliers
## Model Building
First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.

I used Random Forest model and evaluated using R-square. I got R-square value 79%, after using the Hyper-parameter tuning method r-sqaure value was increase by 79% to 81%.  
## Productionization
In this step, I built a flask API endpoint that was hosted on a local webserver. The API endpoint takes in a request with a list of values from a flight and returns an estimated price.