# Time Series Analysis
using ARIMA and fbProphet
# ARIMA
ARIMA models are, in theory, the most general class of models for forecasting a time series which can be made to be “stationary” by differencing (if necessary), perhaps in conjunction with nonlinear transformations such as logging or deflating (if necessary). A random variable that is a time series is stationary if its statistical properties are all constant over time.  A stationary series has no trend, its variations around its mean have a constant amplitude, and it wiggles in a consistent fashion, i.e., its short-term random time patterns always look the same in a statistical sense.  The latter condition means that its autocorrelations (correlations with its own prior deviations from the mean) remain constant over time, or equivalently, that its power spectrum remains constant over time.  A random variable of this form can be viewed (as usual) as a combination of signal and noise, and the signal (if one is apparent) could be a pattern of fast or slow mean reversion, or sinusoidal oscillation, or rapid alternation in sign, and it could also have a seasonal component.  An ARIMA model can be viewed as a “filter” that tries to separate the signal from the noise, and the signal is then extrapolated into the future to obtain forecasts.

* p is the number of autoregressive terms, 
* d is the number of nonseasonal differences needed for stationarity, and 
* q is the number of lagged forecast errors in the prediction equation. 

#### This repository demonstrates how to make Time Series Analysis on a single feature, or comparing between multiple features: forecasting and insights


### Data
Some basic TSA datasets to analyze:
* [LINK](https://github.com/jonykoren/Time_Series_Analysis/tree/master/data)

