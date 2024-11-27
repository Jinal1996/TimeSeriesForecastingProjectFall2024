# TimeSeriesForecastingProjectFall2024
A comprehensive time series analysis and forecasting project focusing on production patterns of various goods. Includes exploratory data analysis, correlation analysis, and predictions using methods like Moving Average, Exponential Smoothing, and Facebook Prophet. Interactive visualizations and insights included.
## Overview
This project analyzes and forecasts the production patterns of various goods using time series techniques. It explores similarities between goods, handles missing values, and predicts production values for the next six months using multiple forecasting methods.

## Objectives
1. Identify production trends and similarities between goods.
2. Handle missing values to ensure data consistency.
3. Forecast production for the next six months using:
   - Moving Average
   - Exponential Smoothing
   - Facebook Prophet

## Repository Structure

TimeSeriesForecastingProjectFall2024/
├── Beans (dry).csv                              # Data files
├── Cassava.csv
├── Chili (red).csv
├── Maize.csv
├── Oranges (big size).csv
├── Peas (fresh).csv
├── Potatoes (Irish).csv
├── Sorghum.csv
├── Tomatoes.csv
├── Combined_Production_Data.csv                # Combined dataset
├── Jinal_Fall 2024_TimeSeriesForecastingProject.ipynb  # Jupyter Notebook
├── Jinal_Fall 2024_TimeSeriesForecastingProject.py     # Python script
├── README.md                                   # Documentation
├── Visualizations/
│   ├── Combined_Forecasts_for_Tomatoes_Using_Plotly.png
│   ├── Combined_Forecasts_for_Tomatoes_Using_Seaborne.png
│   ├── Correlation_Heatmap.png
│   ├── Exponential_Smoothing_Forecast_for_Tomatoes_Using_Plotly.png
│   ├── Facebook_Prophet_Forecast_for_Tomatoes.png
│   ├── Forecast_Comparison_for_Tomatoes_Using_Pyplot.png
│   ├── Moving_Average_Forecasting_for_Tomatoes.png
│   ├── Overlay_of_Time_Series_for_All_Goods.png
│   ├── Time_Series_Visualization.png

## Methods Used
### 1. Data Preprocessing
- **Handling Missing Values:** Linear interpolation to preserve trends.
- **Similarity Analysis:** Correlation matrix and heatmap visualization.

### 2. Forecasting Techniques
- **Moving Average:** Forecast based on a 3-month and 6-month moving average.
- **Exponential Smoothing:** Trend-adjusted smoothing to predict future production.
- **Facebook Prophet:** Advanced model accounting for trends and seasonality.

## Results
### 1. Handling Missing Values:
- To fill or interpolate missing values Linear Interpolation was used.
- **Justification for Linear Interpolation**
  * Given the nature of the data (monthly production values for goods), linear Interpolation is the best choice because:
    * Preservation of Trends: Monthly production values typically follow trends over time. Interpolation maintains these trends better than forward-fill or backward-fill.
    * Continuity: Linear interpolation provides a smooth transition between data points, avoiding abrupt jumps in values.
    * Symmetry: Unlike ffill or bfill, interpolation considers both past and future data, ensuring a balanced estimation for missing values.
    * Applicability to Time Series: Time series data often requires methods that preserve continuity and trends, making interpolation ideal.
  * Linear Interpolation is used for this dataset because:
     * The data likely follows consistent trends.
     * It ensures smooth, trend-preserving estimations without introducing significant biases.
### 2. Correlation Analysis
- **Most Similar Pair of Goods:**
  - Peas (fresh) and Potatoes (Irish) with a correlation of 0.74
- **Why Use Correlation as a Metric?**
  * **Quantitative Measure of Similarity:** Correlation quantifies how two goods' production values change together over time. A high correlation (close to +1) indicates similar production patterns, while a low or negative correlation suggests dissimilarity.
  * **Handles Linear Relationships:** Correlation is well-suited for time series data where trends and seasonal variations are expected.
  * **Interpretability:** Correlation values provide a clear and interpretable metric to compare production patterns.
### 3. Forecasting
- **Moving Average Forecast for Next 6 Months:**
  ```plaintext
  [383.09, 383.09, 383.09, 383.09, 383.09, 383.09]
- **Exponential Smoothing Forecast for Next 6 Months:**
   ```plaintext
  2016-01-01    368.30
  2016-02-01    368.80
  2016-03-01    369.30
  2016-04-01    369.80
  2016-05-01    370.30
  2016-06-01    370.80
- **Prophet Forecast for Next 6 Months:**
  ```plaintext
  2015-12-31    388.28
  2016-01-31    495.98
  2016-02-29    400.67
  2016-03-31    434.92
  2016-04-30    431.21
  2016-05-31    417.23
## Requirements
- Python 3.8+, Google Colab
- Libraries:
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `statsmodels`
  - `prophet`
  - `plotly`
    
## How to Run
**Run the Analysis:**
To run the Jupyter Notebook:
* Clone the repository.
* Navigate to the project directory:
  ```bash
  cd TimeSeriesForecastingProjectFall2024
* Launch the notebook:
   * Jupyter Notebook:
     ```bash
     jupyter notebook: Jinal_Fall 2024_TimeSeriesForecastingProject.ipynb
   * Python Script:
     ```bash
     python scripts: Jinal_Fall 2024_TimeSeriesForecastingProject.py

## Visualizations
### Time Series of Monthly Production Values of Each Good
![Time Series](/Overlay_of_Time_Series_for_All_Goods.png)

### Correlation Heatmap
![Correlation Heatmap](/Correlation_Heatmap.png)

### Moving Averages Forecast
![Moving Average Forecasting for Tomatoes](/Moving_Average_Forecasting_for_Tomatoes.png)

### Exponential Smoothing Forecast for Tomatoes Using Plotly
![Exponential Smoothing Forecast for Tomatoes Using Plotly](/Exponential_Smoothing_Forecast_for_Tomatoes_Using_Plotly.png)

### Facebook Prophet Forecast for Tomatoes
![Facebook Prophet Forecast for Tomatoes](/Facebook_Prophet_Forecast_for_Tomatoes.png)

### Combined Forecasts for Tomatoes Using Pyplot
![Forecast Comparison for Tomatoes Using Pyplot](/Forecast_Comparison_for_Tomatoes_Using_Pyplot.png)

### Combined Forecasts for Tomatoes Using Plotly
![Combined Forecasts for Tomatoes Using Plotly](/Combined_Forecasts_for_Tomatoes_Using_Plotly.png)

### Combined Forecasts for Tomatoes Using Seaborn
![Combined Forecasts for Tomatoes Using Seaborn](/Combined_Forecasts_for_Tomatoes_Using_Seaborne.png)
## License
This project is licensed under the MIT License.

## Contact
For questions or contributions, feel free to reach out:
* Name: Jinal Patel
* Email: jinalpat06@gmail.com
* GitHub: Jinal1996
