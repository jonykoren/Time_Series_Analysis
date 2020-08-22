# Time Series Analysis
using ARIMA and fbProphet

## Time Series Forecast
Time-series forecast itself is one of the methods to create a model for predicting future values based on current and historical time series data. There are four components of time-series:
1. <strong>Trend:</strong> An increase or decrease of data; could be linear or nonlinear (logistics growth)
2. <strong>Seasonality:</strong> Characteristic of time-series data when it experiences regular and predictable movement after a fixed period of time
3. <strong>Cyclic:</strong> Cyclic pattern exists when the data experience rises or falls (regular or periodic fluctuation in data)
4. <strong>Irregularity:</strong> The residual of time series after the trend-cycle and seasonal component are removed


## ARIMA
ARIMA models are, in theory, the most general class of models for forecasting a time series which can be made to be “stationary” by differencing (if necessary), perhaps in conjunction with nonlinear transformations such as logging or deflating (if necessary). A random variable that is a time series is stationary if its statistical properties are all constant over time.  A stationary series has no trend, its variations around its mean have a constant amplitude, and it wiggles in a consistent fashion, i.e., its short-term random time patterns always look the same in a statistical sense.  The latter condition means that its autocorrelations (correlations with its own prior deviations from the mean) remain constant over time, or equivalently, that its power spectrum remains constant over time.  A random variable of this form can be viewed (as usual) as a combination of signal and noise, and the signal (if one is apparent) could be a pattern of fast or slow mean reversion, or sinusoidal oscillation, or rapid alternation in sign, and it could also have a seasonal component.  An ARIMA model can be viewed as a “filter” that tries to separate the signal from the noise, and the signal is then extrapolated into the future to obtain forecasts.

* p is the number of autoregressive terms, 
* d is the number of nonseasonal differences needed for stationarity, and 
* q is the number of lagged forecast errors in the prediction equation. 

#### This repository demonstrates how to make Time Series Analysis on a single feature, or comparing between multiple features: forecasting and insights
* ARIMA(1,0,0) = first-order autoregressive model:
if the series is stationary and autocorrelated, perhaps it can be predicted as a multiple of its own previous value, plus a constant.
* ARIMA(0,1,0) = random walk:
If the series Y is not stationary, the simplest possible model for it is a random walk model, which can be considered as a limiting case of an AR(1) model in which the autoregressive coefficient is equal to 1, i.e., a series with infinitely slow mean reversion.
* ARIMA(1,1,0) = differenced first-order autoregressive model:
If the errors of a random walk model are autocorrelated, perhaps the problem can be fixed by adding one lag of the dependent variable to the prediction equation--i.e., by regressing the first difference of Y on itself lagged by one period.
* ARIMA(0,1,1) without constant = simple exponential smoothing:
Another strategy for correcting autocorrelated errors in a random walk model is suggested by the simple exponential smoothing model. Recall that for some nonstationary time series (e.g., ones that exhibit noisy fluctuations around a slowly-varying mean), the random walk model does not perform as well as a moving average of past values. In other words, rather than taking the most recent observation as the forecast of the next observation, it is better to use an average of the last few observations in order to filter out the noise and more accurately estimate the local mean. The simple exponential smoothing model uses an exponentially weighted moving average of past values to achieve this effect.

## fbProphet
fbProphet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.

## Notebooks
* [Single Feature Example](https://github.com/jonykoren/Time_Series_Analysis/blob/master/Minimum_Daily_Temperatures.ipynb)
* [Mutltiple Features Example](https://github.com/jonykoren/Time_Series_Analysis/blob/master/Superstore.ipynb)

## Data
Some basic TSA datasets to analyze:
* [LINK](https://github.com/jonykoren/Time_Series_Analysis/tree/master/data)

