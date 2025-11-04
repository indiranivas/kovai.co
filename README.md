# kovai.

1️ Data Understanding and Preparation


2️ Stationarity Check

For accurate forecasting, a time series must be stationary, meaning its average and variance remain constant over time. To verify this, the Augmented Dickey-Fuller (ADF) test was performed. If the p-value was greater than 0.05, it indicated that the data was non-stationary. In such cases, first-order differencing (subtracting each value from its previous one) was applied to make the series stationary.

3️ Model Selection – ARIMA

The ARIMA (Auto-Regressive Integrated Moving Average) model was chosen because it works well for non-seasonal time series data. The model uses three key parameters:

p (Auto-Regressive term): accounts for the influence of past observations.

d (Integrated term): indicates the level of differencing applied to achieve stationarity.

q (Moving Average term): represents the impact of past forecast errors.

After experimenting, an ARIMA(1,1,1) configuration was selected as it provided stable and interpretable results.

4️ Model Training and Forecasting

Separate ARIMA models were trained for each service category — Local Route, Light Rail, Peak Service, Rapid Route, and School. Once fitted, the model generated 7-day forecasts for future passenger counts. Along with the predictions, confidence intervals were also computed to represent the expected range of future values.

5 Insights

6 Result

The final output produced reliable 7-day forecasts for each transport type. These insights can help city transport authorities anticipate changes in passenger flow and plan their services more efficiently.
