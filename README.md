🚖 Taxi Fare Prediction with PySpark ML
This project demonstrates how to build a machine learning pipeline using PySpark to predict taxi fare prices based on various features like passenger count, trip distance, and more. The project includes data preprocessing, feature scaling, encoding categorical variables, and applying machine learning models to predict fare amounts.

📋 Project Overview
The goal of this project is to predict the fare amount of taxi rides using a dataset containing information about:

Pickup times
Number of passengers
Distance traveled (calculated from latitude and longitude)
Time of day (day or night)
Weekday (weekend or weekday)
We used PySpark's MLlib to preprocess the data, train machine learning models, and evaluate their performance.

🚀 Features
Data Preprocessing
Extract year, month, day of the week, and hour from the pickup time
Create new features: day_or_night and weekend
Remove outliers based on distance, passenger count, and fare amount
Handle missing values
Encode categorical variables: day of the week, day or night
Feature Scaling
Normalize numerical features using StandardScaler
Distance Calculation
Compute the distance between pickup and drop-off locations using the Haversine formula
Train-Test Split
Split the data into training and test sets (70/30)
Machine Learning Modeling
Train and evaluate a Linear Regression model using PySpark MLlib
Evaluate the model using RMSE and R²
📊 Dataset
The dataset used in this project contains the following key columns:

fare_amount: Target variable, the amount of fare for the taxi ride.
passenger_count: The number of passengers in the taxi.
year, month, day_of_week, hour, minute: Time-related features extracted from the pickup datetime.
distance_km: The distance between the pickup and drop-off locations (calculated using latitude and longitude).
weekend: Binary variable indicating whether the ride was on a weekend or a weekday.
day_or_night: Binary variable indicating whether the ride occurred during the day or night.

📈 Model Training & Evaluation
The model pipeline involves the following steps:

Feature Engineering:

Extract time-related features like year, month, day of the week, and hour.
Calculate distance using latitude and longitude.
Encode categorical variables (e.g., day_of_week, day_or_night).
Train-Test Split:

We split the dataset into 70% training and 30% testing data.
Modeling:

We used Linear Regression to predict the taxi fare.
We scaled the numerical features using PySpark's StandardScaler.
Evaluation:

The model was evaluated using Root Mean Squared Error (RMSE) and R².
