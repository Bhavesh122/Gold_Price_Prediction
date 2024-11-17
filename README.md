# Gold Price Prediction

This project uses machine learning models to predict the price of gold based on various economic indicators such as Silver, Crude Oil, S&P500, Dollar Index, etc. The models utilized for prediction include Linear Regression, Decision Tree Regressor, Random Forest Regressor, Gradient Boosting Regressor, and Support Vector Regressor.

## Features

- Data is fetched from Yahoo Finance for different economic indicators and their historical data.
- Preprocessing includes merging and cleaning the data before training.
- Multiple machine learning models are trained and compared for performance.
- A function to predict gold prices based on input data is implemented.

## Installation

To set up the project and install the necessary dependencies, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/gold-price-prediction.git
    cd gold-price-prediction
    ```

2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

    If `requirements.txt` is not already present, you can install dependencies manually:
    ```bash
    pip install pandas matplotlib scikit-learn yahoofinancials
    ```

## Dataset

The project fetches historical price data for multiple tickers from Yahoo Finance. A sample `Ticker List.xlsx` containing tickers and descriptions is used for this project.

## Usage

1. **Load and Fetch Data**: The project fetches data from Yahoo Finance using the tickers in the `Ticker List.xlsx` file.
2. **Train Models**: The following models are used to predict the gold price:
    - Linear Regression
    - Decision Tree Regressor
    - Random Forest Regressor
    - Gradient Boosting Regressor
    - Support Vector Regressor
3. **Plotting**: The script plots actual vs predicted gold prices for the best-performing model.
4. **Predict Gold Price**: Use the `predict_gold_price` function to predict gold prices based on input data.

Example:
```python
input_data = {
    'Date': '2000-10-02',
    'Silver': 31.2,
    'Crude Oil': 68.2,
    'S&P500': 5762.5,
    'Russel 2000 Index': 2230.0,
    '10 Yr US T-Note futures': 114.3,
    '2 Yr US T-Note Futures': 104.0,
    'Platinum': 979.0,
    'Copper': 4.5,
    'Dollar Index': 100.5,
    'Volatility Index': 16.7,
    'Soybean': 45.9,
    'MSCI EM ETF': 1.1,
    'Euro USD': 1484.7,
    'Euronext100': 18189.2
}

predicted_price = predict_gold_price(input_data)
print(f"Predicted Gold Price on {input_data['Date']}: {predicted_price}")
