# Air-Quality-Index-AQI-Prediction
This project aims to build a regression model to predict the Air Quality Index (AQI) of Indian cities based on various environmental parameters. It also provides visual insights into regional pollution levels across different years.

Dataset

The dataset used is city_day.csv, which contains daily air quality data for Indian cities. It includes features such as:

PM2.5

PM10

NO, NO2, NOx

NH3

CO

SO2

O3

Benzene, Toluene, Xylene

AQI (Target variable)

Objectives

Clean and preprocess the data.

Train a regression model (Random Forest) to predict AQI.

Visualize pollution trends across cities and time.

Identify the most influential features contributing to AQI.

Provide a prediction interface for custom inputs.

Steps Performed

1. Data Preprocessing

Handled missing values with median/mode imputation.

Extracted temporal features (year, month).

Encoded categorical data (City).

2. Feature Engineering

Selected features highly correlated with AQI.

Applied label encoding to city names.

3. Model Training & Evaluation

Used RandomForestRegressor with train/test split.

Evaluated performance using RMSE and R² score.

4. Visualizations

AQI distribution by city and over time.

Feature importance plot.

Regional AQI trend plots for top polluted cities.

5. AQI Prediction

Created a function predict_aqi(input_features) to make predictions for custom input values.

Trained model is saved as aqi_model.pkl for reuse.

Example Prediction

custom_input = {
    'PM2.5': 120, 'PM10': 250, 'NO': 40, 'NO2': 50, 'NOx': 80,
    'NH3': 20, 'CO': 1.0, 'SO2': 10, 'O3': 15, 'Benzene': 2.5,
    'Toluene': 3.0, 'Xylene': 0.5, 'City_encoded': le.transform(['Delhi'])[0]
}
predicted_aqi = predict_aqi(custom_input)

Requirements

Python 3.x

pandas, numpy, seaborn, matplotlib

scikit-learn

joblib

Future Enhancements

Real-time AQI prediction with API integration.

Web-based dashboard using Streamlit or Flask.

Integration with maps to show pollution geospatially.
