## Project Name - Bike Sharing Demand Prediction


## Project Description
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.
### Attributes
 **Date : year-month-day**
*   **Rented Bike count - Count of bikes rented at each hour**
*   **Hour - Hour of the day**
*   **Temperature-Temperature in Celsius**
*   **Humidity - %**
*   **Windspeed - m/s**
*   **Visibility - 10m**
*   **Dew point temperature - Celsius**
*   **Solar radiation - MJ/m2**
*   **Rainfall - mm**
*   **Snowfall - cm**
*   **Seasons - Winter, Spring, Summer, Autumn**
*   **Holiday - Holiday/No holiday**
*   **Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

## Project Summary
The bike sharing demand prediction project aims to develop a predictive model to forecast the demand for bike rentals in a specific city or region. The project will leverage historical data on bike usage, weather conditions, and other relevant factors to train a predictive model that can accurately forecast the number of bike rentals for futre time periods.

The project will involve data inspection, exploratory data analysis, feature engineering/data preprocessing and model training and evaluation. Various machine learning algorithims, such as regression, decision tree, and Random forest, will be tested and evaluated to determine the best-performing model.

The ultimate goal of the project is to provide bike-sharing service providers and city officials with accurate demand forecasts that can help them optimize bike availability, allocate resources efficiently, and improve the overall user experience.

## Preprocessing
The dataset requires some preprocessing before it can be used for training and testing a machine learning model. The preprocessing steps include:

*  Dropping those rows containg zero bike counts or No functioning day and and then also drop Functionig day column due to its not usefullness.
*  Converting the datetime column to separate columns for year, month and day
*  Dropping the dew point temperature column to prevent from multicollinearity problem as temperature and dew point temperature are highly correlated(0.91).
*  Label encoding the categorical columns (Seasons, Holiday).
*  Appling different transformation techniques (cbrt transformation, sqrt transformation) to our target variable 'Rented Bike Count' and feature 'Wind speed'.
*  Scaling the train and test data using MinMaxScaler.


## Model
Various machine learning algorithims, such as Linear regression, Lasso Regression, Ridge Regression,  Decision Tree, Extra Decesion Trees and Random Forest regressor, will be tested and evaluated to determine the best-performing model. The models are trained on 80% of the data and evaluated on the remaining 20%. Extra Trees Regression model is the best performing model with the highest R2-score (0.874) achieved.


##  Conclussion
We used R2-score to understand which model fit our data better, and the scores are as follows:
1. Linear Regression - 0.551500
2. Lasso (L1) Regression - 0.549425
3. Ridge (L2) Regression - 0.551497
4. Elastic-Net Regression - 0.550229
5. Decision Tree Regressor - 0.783009
6. Random Forest Regressor - 0.861200
7. Extra Trees Regressor - 0.873917

From the above, we can say that the Extra Trees Regression model is the best performing model with the highest R2-score (0.874) achieved.







