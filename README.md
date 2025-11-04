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

  Weekly Passenger Journeys by Service Type:
  The weekly trend analysis shows fluctuations in passenger journeys across different service types, highlighting variations in travel demand throughout the week.
  
  Anomalous Spike in Peak Service:
  A sudden spike was observed in the ‘Peak Service’ on 10 November 2023, followed by a sharp drop over the next two days, even reaching zero. This indicates an isolated surge in peak-hour travel demand, possibly due to a specific event or data anomaly.
  
  High Average in Rapid Route:
  The Rapid Route service records the highest average daily passenger count compared to other service types, suggesting it is the most preferred or efficient route among commuters.
  
  Comparison: Rapid Route vs Local Route:
  When comparing Rapid Route and Local Route, the Rapid Route consistently shows higher passenger volumes and more stable patterns, whereas the Local Route experiences more fluctuations, indicating varying local travel behavior.

6 Result

The final output produced reliable 7-day forecasts for each transport type. These insights can help city transport authorities anticipate changes in passenger flow and plan their services more efficiently.
