# Bike Sharing Demand Prediction
## Project Overview
Urban cities are increasingly offering bike-sharing services to reduce congestion and promote eco-friendly transportation. However, ensuring a consistent supply of bikes at the right time and location is crucial for efficient service delivery. This project focuses on predicting the demand for rental bikes based on various factors like weather conditions, time, and seasonality. By predicting bike demand, the aim is to minimize resource wastage while maximizing customer satisfaction.

## Problem Statement
The goal is to predict the number of bikes required at a given hour to meet the demand of a bike-sharing program in Seoul. A consistent supply is essential to reduce customer wait times and avoid resource wastage due to an oversupply of bikes.

## Motivation
Bike-sharing systems have gained popularity in metropolitan cities like San Francisco, New York, and Chicago. For these systems to operate efficiently, it is vital to predict demand accurately.

Excess bikes can lead to wasted resources in terms of bike maintenance and parking space.
Fewer bikes lead to lost revenue and potential long-term customer dissatisfaction.
Accurate demand prediction can lead to optimal resource allocation and better user experience.

## Dataset
The dataset includes data from Seoul's bike-sharing system and includes features such as:

Date & Time: Year, month, day, and hour.
Weather: Temperature, humidity, wind speed, visibility, etc.
Season: Spring, summer, autumn, winter.
Holiday & Functioning Days: Holidays and working days.
The target variable is the Rented Bike Count, representing the number of bikes rented at a specific time.

## Libraries Used
pandas
numpy
seaborn
matplotlib
scikit-learn
xgboost
statsmodels
Data Preprocessing

## Exploratory Data Analysis (EDA)
### Some key observations from EDA:

**Season:** The demand for bikes is lower during the winter season.

**Holiday:**  Bike demand is lower on holidays but higher on non-holidays, as people likely use bikes for commuting to work.

**Functioning Day:** No bike demand is observed on non-functioning days.

**Days of the Week:** The demand patterns differ between weekdays and weekends. On weekends, demand spikes in the afternoon, while on weekdays, the demand is high during office hours.

**Month:** Demand is low in the winter months of December, January, and February.

**Year:** Bike demand increased significantly in 2018 compared to 2017, likely due to increased awareness of the bike-sharing program.

## Data Skewness
Right Skewed Columns: Rented Bike Count, Wind speed, Solar Radiation, Rainfall, Snowfall
Left Skewed Columns: Visibility, Dew point temperature
The skewness of these features was accounted for while applying machine learning algorithms.

##  Modeling
Several regression algorithms were applied to predict bike demand:

Linear Regression: Basic approach, but may not capture complex relationships.
RandomForest Regression: Ensemble method that improves accuracy by reducing overfitting and capturing nonlinear relationships.
XGBoost Regression: Gradient boosting technique, which usually delivers superior performance by optimizing for accuracy and handling skewed data.

## Evaluation Metrics
The models were evaluated using:

Mean Absolute Error (MAE): To measure the average magnitude of the errors in predictions.
Mean Squared Error (MSE): To penalize larger errors more significantly.
R-squared (R²): To measure how well the model explains the variance of the data.

## Results
Linear Regression: Provided a baseline model but struggled with complex relationships in the data.
RandomForest Regression: Improved accuracy by better handling nonlinear patterns in the data.
XGBoost Regression: Delivered the best performance among all models due to its capability to optimize and handle large-scale data efficiently.

## Conclusion
By analyzing historical data and identifying patterns based on weather, time, and holidays, the project successfully predicted bike demand with reasonable accuracy. The models, especially XGBoost, can be used to ensure optimal resource allocation for the bike-sharing system, thereby improving service efficiency and user satisfaction.
