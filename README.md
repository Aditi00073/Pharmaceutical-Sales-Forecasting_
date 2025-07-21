Here’s a **concise, paraphrased summary** of your Pharma-Sales-Analysis-and-Forecasting case study, incorporating recent research practices and keeping technical context intact:

# Pharma-Sales-Analysis-and-Forecasting

## Project Summary

Pharmaceutical sales forecasting is crucial for inventory and strategic business planning. Traditionally, large-scale pharmaceutical forecasts use simple models like the Naïve approach—projecting future sales as the previous period's numbers, adjusted by growth factors tailored for different regions or product categories. While this is reliable at scale, it becomes less accurate for smaller entities (like a single distributor or pharmacy) due to higher uncertainty and noise in the data. Therefore, there is a need for more advanced modeling at the local or short-term level.

This project examines whether modern time-series forecasting methods—ARIMA/SARIMA, Facebook Prophet, and LSTM-based deep learning—can outperform basic approaches (Naïve, Seasonal Naïve, Average) in forecasting pharmaceutical product sales at the pharmacy level. The analysis uses six years of sales data from a single pharmacy, aggregated by drug category and time period.

## Time Series Forecasting Techniques

- **Naïve, Seasonal Naïve, and Average methods** serve as the baseline, offering simple projections based on recent or seasonal values.
- **ARIMA and SARIMA** models capture trends, seasonality, and autocorrelation in stationary (or transformed) data, with hyperparameters tuned by autocorrelation patterns and grid search.
- **Facebook Prophet** is well-suited for capturing complex trends, outliers, and business seasonality, and supports customization through holiday/event markers.
- **LSTM Neural Networks** (including vanilla, stacked, and bidirectional architectures) are leveraged for their ability to model nonlinear and long-term dependencies within the time series.

## Methodology

1. **Feature Engineering:**  
   Raw transactional records (date, time, drug, quantity) are aggregated into designated drug categories, following pharmacist guidance and mapped to standard codes (ATC). Data is resampled to hourly and then weekly intervals for analysis.
2. **Exploratory Analysis:**  
   The time series is analyzed for level, trend, seasonality, and noise. Stationarity is tested (rolling statistics, ADF/KPSS tests), and series are transformed as needed for modeling.
3. **Forecasting:**  
   Both rolling (short-term) and long-term forecasts are produced. For validation, the last year of data is reserved as a test set, and performance is measured via Mean Squared Error (MSE), with Mean Absolute Percentage Error (MAPE) given for context.

## Key Results

- **LSTM models** consistently achieved higher accuracy than traditional approaches like ARIMA and Naïve methods, especially in scenarios with complex, nonlinear patterns.
- Accurate modeling guides real-world business decisions: resource allocation, procurement, sales campaigns, and strategic planning.
- Seasonal and trend analysis revealed optimal periods for marketing actions and highlighted drug categories with irregular or unpredictable demand.

## Credits: 
This project draws significant inspiration from the work of milanzdravkovic on Kaggle—specifically the notebook titled "Pharma Sales Data Analysis and Forecasting." The referenced notebook served as a key resource for the methodology, exploration of forecasting techniques, and presentation of analysis. 
link - "https://www.kaggle.com/code/milanzdravkovic/pharma-sales-data-analysis-and-forecasting/notebook"
