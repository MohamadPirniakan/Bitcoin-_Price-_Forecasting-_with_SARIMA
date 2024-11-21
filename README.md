# Bitcoin Price Forecasting with SARIMA

This project applies the **SARIMA (Seasonal ARIMA)** model to forecast Bitcoin prices based on historical data. The model performs data preprocessing, stationarity checks, Box-Cox transformation, ARIMA parameter selection, and provides forecasts with confidence intervals. Visualizations of historical data and forecasted prices are also included.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Model Explanation](#model-explanation)
- [Visualizations](#visualizations)
- [License](#license)

## Installation

To get started with the project, clone this repository to your local machine and install the necessary dependencies.

```bash
https://github.com/MohamadPirniakan/Bitcoin-_Price-_Forecasting-_with_SARIMA.git
cd bitcoin-price-forecasting-sarima
pip install -r requirements.txt
```

## Usage

Once you've installed the dependencies, you can run the forecasting script.

```bash
python forecast_bitcoin.py
```

This will:
- Load and preprocess the Bitcoin data.
- Apply the SARIMA model.
- Output the forecast and visualizations.

Make sure to update the dataset path in the script if necessary.

## Project Structure

```
bitcoin-price-forecasting-sarima/
│
├── data/
│   └── crypto-markets.csv  # Dataset with historical cryptocurrency data
│
├── forecast_bitcoin.py     # Main script to run the forecasting model
├── requirements.txt        # List of dependencies
└── README.md               # Project description and usage
```

## Dependencies

This project uses the following Python libraries:

- `pandas` - for data manipulation and analysis
- `numpy` - for numerical computations
- `matplotlib` - for data visualization
- `seaborn` - for statistical data visualization
- `statsmodels` - for time series analysis (SARIMA model)
- `scipy` - for statistical functions
- `itertools` - for iterating over parameter combinations
- `datetime` - for handling date and time operations

To install the dependencies, run:

```bash
pip install -r requirements.txt
```

## Model Explanation

**SARIMA (Seasonal ARIMA)** is an extension of the ARIMA model that supports univariate time series data with a seasonal component. In this project, the SARIMA model is applied to Bitcoin price data, with the following steps:

1. **Data Preprocessing**: The data is cleaned and resampled to a monthly frequency.
2. **Stationarity Check**: The Dickey-Fuller test is applied to ensure the series is stationary.
3. **Transformation**: A Box-Cox transformation is used to stabilize variance.
4. **Differencing**: The series is differenced to achieve stationarity.
5. **Model Fitting**: The SARIMA model is fitted using various parameter combinations.
6. **Forecasting**: Future Bitcoin prices are predicted for the next 12 months.

## Visualizations

The project generates the following visualizations:

- **ACF and PACF Plots**: To determine the optimal parameters for the SARIMA model.
- **Forecast Plot**: Historical Bitcoin prices and the forecasted prices for the next 12 months.
- **Confidence Interval**: A shaded region representing the uncertainty in the forecast.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```

### Notes:
1. The structure is clear, and key project details are easily accessible.
2. You may need to adjust the paths or the script names based on your actual project structure and file names.
3. Be sure to include a **LICENSE** file if you intend to distribute the project, and adjust the license section as needed.
