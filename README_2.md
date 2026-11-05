# Air Quality Time Series Forecasting (India)

Forecast the daily Air Quality Index (AQI) of an Indian city using baselines, ARIMA, and machine-learning models.

## Dataset
Kaggle: [Air Quality Data in India](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india)
Download `city_day.csv` and place it in a `data/` folder:

```
air_quality_forcasting_project/
├── air_quality_forecasting.ipynb
├── requirements.txt
└── data/
    └── city_day.csv
```

## Run
```bash
pip install -r requirements.txt
jupyter lab
```
Open `air_quality_forecasting.ipynb` and run all cells. Change `CITY = "Delhi"` to try another city.

## Approach
1. Clean data (missing values, date index, interpolation of short gaps)
2. EDA: city comparison, seasonality, yearly trend, correlations
3. Time series analysis: decomposition, ADF test, ACF/PACF
4. Models: naive / seasonal naive / moving average, ARIMA, Ridge, Random Forest, Gradient Boosting
5. Evaluate on the last 90 days with MAE, RMSE, R2
6. Recursive 7-day forecast

## Results
Fill in after running (example): Gradient Boosting reduced RMSE by 9% vs the naive baseline.

## Tech
Python, Pandas, NumPy, Matplotlib, Seaborn, statsmodels, scikit-learn
