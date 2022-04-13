# Kaggle Bike-Sharing-Demand

## Problem Statement

In this competition, participants are asked to combine historical usage patterns with weather data in order to forecast bike rental demand in the Capital Bike-share program in Washington, D.C.

## Data Description

The dataset contains weather information (Temperature, Relative Humidity, Windspeed, Snowfall, Rainfall), the time information (Season, Datetime, Holiday, Workingday), and number of bikes rented per hour.

## Attribute Information

    • datetime : hourly date + timestamp
    • season : 1 = spring, 2 = summer, 3 = fall, 4 = winter 
    • holiday : whether the day is considered a holiday
    • workingday : whether the day is neither a weekend nor holiday
    • weather - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
                2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
                3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
                4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
    • temp : temperature in Celsius
    • atemp : "feels like" temperature in Celsius
    • humidity : relative humidity
    • windspeed : wind speed
    • casual : number of non-registered user rentals initiated
    • registered : number of registered user rentals initiated
    • count : number of total rentals

## Modeling Pipeline

1. Exploratory Data Analysis (EDA) : In this part we have done some  EDA on the features to see the trend. 
2. Data Pre-processing : Based on the observations from the previous stage, we first deal with **missing data imputation**.
3. Modeling : Finally, in this part we created the various XGBoost tree models.  These various models are analysed, and we tried to do model selection by **Grid Search** to get the best performing model for our project.

## Observation

● Observation 1: By the Exploratory Data Analysis, we find each hour has its own unique pattern, we consider modeling by each hour.

● Observation 2: The amount of data is not quiet large, so we do not consider building a neural network model.

● Observation 3: We get the best results from XGBoost tree model.

## Conclusion

● Finally, we modeled with xgboost tree, and the model performance reached 0.41, which is about the 90th percentile.

## Reference
1. [kaggle site](https://www.kaggle.com/competitions/bike-sharing-demand/overview)
2. [Generalized Low Rank Models](https://web.stanford.edu/~boyd/papers/pdf/glrm.pdf)

