# Final-Year-Project-Time-Series-Forecasting-
**Forecasting Household Electric Power Consumption**

**Dataset Information:**

1. Date: Date in format dd/mm/yyyy
   
2. Time: time in format hh:mm:ss
   
3. Global_active_power: household global mi|nute-averaged active power (in kilowatt)
   Global active power is a term used in electrical engineering to refer to the total active power consumption of a building    or an entire electrical grid. It measures the real power used by electrical devices and is expressed in watts (W).
  
4. Global_reactive_power: household global minute-averaged reactive power (in kilowatt)
   Global reactive power is a term used in electrical engineering to refer to the total reactive power consumption of a  
   building or an entire electrical grid. It is a measure of the amount of electrical power that is flowing back and forth      between the source and the load in an alternating current (AC) electrical system, and it doesn't do any useful work, but     it is necessary to maintain the voltage level in the system. It is expressed in volt-amperes reactive (VAR).
   
5. Voltage: minute-averaged voltage (in volts)
   Voltage, also known as electric potential difference, is a measure of the electrical potential energy per unit charge in     an electrical circuit. It is the force that drives the flow of electric charge in a circuit and is expressed in volts (V).

6. Global_intensity: household global minute-averaged current intensity (in ampere)
   Global intensity refers to the overall or average current flow in an electrical system or network, such as a building or     an entire electrical grid. It is a measure of the amount of electric charge moving through a conductor per unit of time       and is expressed in amperes (A).

7. Sub_metering_1: energy sub-metering No. 1 (in watt-hour of active energy).
   It corresponds to the kitchen, containing mainly a dishwasher, an oven and a microwave (hot plates are not electric but      gas-powered).

8. Sub_metering_2: energy sub-metering No. 2 (in watt-hour of active energy).
   It corresponds to the laundry room, containing a washing machine, a tumble drier, a refrigerator and a light.

9. Sub_metering_3: energy sub-metering No. 3 (in watt-hour of active energy).
   It corresponds to an electric water heater and an air-conditioner.

# Built with
Google Colab

# Libraries used
+ Pandas
+ Numpy
+ itertools
+ Matplotlib
+ Seaborn
+ Scikit-learn
+ statsmodels
+ keras
+ xgboost

# Models used for forecasting of Global Active Power
ARIMA, LSTM, XGBoost

# Flow of implementation
1. Data understanding
   + Data Exploration
   + Data visualisation
3. Data Preparation
   + Data cleaning
   + Feature engineering
   + Data Normalization
   + Train-Test Splits

# Model Implementation
1. ARIMA
   + Check for stationarity of time series data
   + Find value of p,d,q using ACF and PACF plot
   + Find optimal parameters using the grid search technique
2. LSTM
   + Best Input Sequence Selection
   + Best Optimizer Selection
   + Best Learning Rate Selection
   + Data type (Univariate vs Multivariate) Selection
   + Best Batch Size and Epochs Selection
3. XGBoost
   + Data type (multivariate) Selection
   + Fine-tuning the XGBoost model using the grid search technique

# Prediction of Global Active Power
<img width="809" alt="image" src="https://github.com/user-attachments/assets/fc1c4b65-e863-4df5-8a23-67735eb2a1ec">

<img width="788" alt="image" src="https://github.com/user-attachments/assets/76f6b89b-41f9-44e5-a455-8e9d987ec601">

<img width="811" alt="image" src="https://github.com/user-attachments/assets/30986c18-5e6d-4bd1-99b4-6cee15185dc6">

# Performance comparison of ARIMA, LSTM and XGBoost
<img width="544" alt="image" src="https://github.com/user-attachments/assets/ea1b9d09-9a02-4634-944f-350e15f47ae0">

# Conclsion
In this project, I used the IHEPC dataset to predict Global Active Power. Firstly, the IHEPC dataset underwent preprocessing, deploying data exploration and data visualization techniques to address missing values and visualize the data. MICE data imputation techniques enhance the model performance. Afterwards, the time series decomposition and autocorrelation plots were used to confirm the stationary of the data and the best prediction period. For hourly, daily, and monthly resampled data, the optimal prediction periods for all models with reduced RMSE values were 24, 7, and 12, respectively. Lastly, I utilized Min-Max data scaling methods to generate an efficient model for the representation of the input data. The empirical findings indicate that the prediction of Global Active Power with the seasonal ARIMA model with RMSE values of 0.69 and 0.34, respectively, for hourly and daily resampled data. The LSTM model achieves RMSE values of 0.480 and 0.229 for hourly and daily resampled data, respectively, with input data sequences of 24 and 7. Among these two approaches, the XGBoost algorithm provides the lowest RMSE values of 0.249 and 0.111 for hourly and daily resampled data, respectively, when using the Min-Max data scaling technique. In terms of different RSME and MAPE evaluation measures, these findings are better than the state-of-the-art models for predicting electrical power consumption.



