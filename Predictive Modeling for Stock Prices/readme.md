# Stock Price Prediction using ARIMA, LSTM, and Prophet

## Project Overview

This project focuses on predicting stock prices using three different models: ARIMA, LSTM, and Prophet. Each model is evaluated based on standard performance metrics, and the results are compared to determine the best approach for forecasting stock prices.

## Project Structure
├── data/                         # Directory containing the dataset

│   └── stock_price_translated.csv # Stock price data used for model training and testing

├── notebooks/                    # Jupyter notebooks for model training and evaluation

│   ├── ARIMA_Model.ipynb         # Notebook implementing ARIMA model

│   ├── LSTM_Model.ipynb          # Notebook implementing LSTM model
│   └── Prophet_Model.ipynb       # Notebook implementing Prophet model
├── models/                       # Directory to save trained models
│   ├── arima_model.pkl           # Saved ARIMA model
│   └── lstm_model.h5             # Saved LSTM model
├── src/                          # Python scripts for data processing and model building
│   └── utils.py                  # Utility functions used across the project
├── README.md                     # Project README file
└── requirements.txt              # Dependencies required to run the project


## Getting Started
**Prerequisites** 
- To run this project, you will need the following packages installed:

    - Python 3.8 or higher
    - Pandas
    - NumPy
    - TensorFlow
    - fbprophet (Prophet)
    - statsmodels (for ARIMA)
    - Matplotlib
    - Scikit-learn


You can install all dependencies by running the following command:
pip install -r requirements.txt



## Dataset
The dataset used for this project contains stock price data with features such as:

- Date: The date of the stock price entry.
- Opening price: The stock price at market opening.
- Closing price: The stock price at market closing.
- Volume: The total volume of stocks traded each day.
- The dataset is provided in the data/stock_price_translated.csv file.

## Running the Models
**ARIMA Model:**
    To train and evaluate the ARIMA model, navigate to the notebooks/ARIMA_Model.ipynb file. It includes the entire workflow, from data preprocessing to model evaluation.

**LSTM Model:**
    For the LSTM model, use the notebooks/LSTM_Model.ipynb file. The LSTM model is trained on the scaled stock price data, and the results are evaluated on a test set.

**Prophet Model:**
    The Prophet model can be run by accessing the notebooks/Prophet_Model.ipynb file. It handles the seasonality and trend of the stock prices.

## Model Evaluation
Each model is evaluated using the following metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

The evaluation results are summarized in the table below:

        Model	MAE	MSE	RMSE	R²
        ARIMA	10.05	145.63	12.07	-0.34
        LSTM	0.036	0.0022	0.047	0.951
        Prophet	13.64	268.31	16.38	-1.47

## Feature Engineering
Various feature engineering techniques were applied to improve model performance, including:

Lag features (previous day's closing price).
Rolling statistics (moving averages).
Handling missing data and outliers.

## Model Saving
The trained models are saved for future use:

- The ARIMA model is saved as arima_model.pkl in the models/ directory.
- The LSTM model is saved as lstm_model.h5 in the models/ directory.
- The Phrophet model is saved as prophet_model.pkl in the models/ directory.

## Improvements and Future Work
To improve model accuracy, the following approaches could be explored:

**Hyperparameter tuning:** Further optimization of model parameters.
**Ensemble learning:** Combining multiple models to improve prediction accuracy.
**External features:** Incorporating external factors such as market trends and economic indicators.

## Contributing
If you would like to contribute to this project, feel free to fork the repository and submit a pull request with your changes.
