# Air Quality in Alaska: PM2.5 Analysis

This project focuses on analyzing the air quality in Alaska by studying PM2.5 (Particulate Matter with a diameter less than 2.5 micrometers) concentration levels over time. The dataset is collected from various monitoring stations across different regions in Alaska and covers the time period from 2018 to 2024.

## Project Structure

- **Data Collection**: PM2.5 concentration levels are collected from several CSV files and merged into a single DataFrame for analysis.
- **Data Preprocessing**: 
  - Dates are formatted correctly and columns are renamed for clarity.
  - Grouped by date to calculate daily mean PM2.5 concentration levels.
  - Missing values handled via forward fill (`ffill`).
  - Anomalies were removed based on Interquartile Range (IQR).

## Key Libraries

The following Python libraries are used in the project:
- `pandas`: Data manipulation and cleaning.
- `matplotlib`, `seaborn`, `plotly`: Data visualization.
- `ARIMA`: Time series forecasting model.
- `statsmodels`: For seasonal decomposition and autocorrelation functions.
- `sklearn`: For performance metrics (Mean Absolute Error, Mean Squared Error).

## Exploratory Data Analysis (EDA)

- **Monthly PM2.5 Concentration**: A bar plot visualizes the average PM2.5 levels by month.
- **Yearly Trend**: A line plot shows the trend of PM2.5 concentration across years.
- **Distribution of PM2.5**: A histogram with a kernel density estimate visualizes the distribution of PM2.5 values.
- **Seasonal Decomposition**: Decomposition of the PM2.5 values into trend, seasonal, and residual components.

## Time Series Forecasting

- **ARIMA Modeling**: Various configurations of ARIMA models were tested to forecast future PM2.5 values:
  - The best-performing model is ARIMA(5, 0, 2).
  - Baseline MAE: 4.31
  - Final Test MAE (Walk Forward Validation): 1.94
  
- **Future Forecast**: The ARIMA model is used to forecast PM2.5 values for the next 3 days.

## Visualizations

- **Yearly Trend of PM2.5**
- **Monthly Distribution of PM2.5**
- **PM2.5 Seasonal Decomposition**
- **Cumulative Distribution Function (CDF) of PM2.5**

## How to Run the Code

1. Clone the repository.
   ```bash
   git clone https://github.com/elsayedghoonaim/air_quality_alaska.git
   cd air_quality_alaska
## Results

The analysis provided several insights into PM2.5 levels in Alaska:

- **Monthly Averages**: PM2.5 levels showed seasonal variation, with certain months having higher average concentrations.
- **Yearly Trend**: Over the years, there was a noticeable fluctuation in PM2.5 levels, with 2020-2021 showing peaks likely influenced by environmental events such as wildfires.
- **Distribution**: The majority of PM2.5 readings were below the hazardous threshold, but there were occasional spikes.
- **Forecasting**: The ARIMA(5, 0, 2) model achieved a **Test MAE** of 1.94, providing a reasonable prediction for future PM2.5 values.

Future forecasts suggest a slight increase in PM2.5 levels for the next three days.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## Author

- **Elsayed Ghonaim**

