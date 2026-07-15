# Weather Trend Forecasting - Technical Assessment Report

## PM Accelerator Mission

PM Accelerator's mission is to break down financial barriers and achieve educational fairness. With the goal of establishing 200 schools worldwide over the next 20 years, we aim to empower more kids for a better future in their life and career, simultaneously fostering a diverse landscape in the tech industry.

PM Accelerator is dedicated to empowering the next generation of product managers and AI professionals through hands-on experience, mentorship, and real-world projects.

## Executive Summary

WEATHER TREND FORECASTING - TECHNICAL ASSESSMENT SUMMARY

Dataset Overview:
- Total Records: 113,813
- Time Period: 2024-05-16 to 2025-12-22
- Time Span: 585 days
- Countries: 211
- Locations: 255

Data Quality:
- Missing Values: 103,309
- Outliers Handled: 34,699
- Data Cleaning: Complete

Key Findings:
1. Temperature shows strong seasonal patterns with clear annual cycles
2. Precipitation is highly variable with 33.6% of days having precipitation
3. Air quality shows negative correlations with humidity (r = -0.26 to -0.44)
4. Temperature and "feels like" temperature are highly correlated (r = 0.98)

Forecasting Performance:
- Best Model: Ensemble (Weighted)
  * RMSE: 0.40°C
  * MAE: 0.30°C
  * MAPE: 1.53%
  * R²: 0.98

Feature Importance:
- Top Features: feels_like_celsius, humidity, uv_index, pressure_mb
- Spatial patterns: Africa (hottest), North America (coldest)
- Climate variability: High in precipitation, moderate in temperature

Advanced Analyses:
- Anomaly Detection: Implemented (Isolation Forest & LOF)
- Climate Analysis: Long-term trends identified
- Environmental Impact: Air quality correlations analyzed
- Spatial Analysis: 211 countries analyzed


## Methodology

### 1. Data Cleaning & Preprocessing
- Missing values: None found in original dataset
- Outliers: 34,699 extreme outliers capped using IQR method
- Data normalization: Applied StandardScaler, RobustScaler, and MinMaxScaler

### 2. Exploratory Data Analysis
- Temperature and precipitation visualizations
- Correlation analysis
- Seasonal pattern identification
- Air quality analysis

### 3. Forecasting Models
- Basic Models: ARIMA, SARIMA, Moving Average
- Advanced Models: Prophet, XGBoost, Ensemble
- Evaluation Metrics: MAE, RMSE, MAPE, R²

### 4. Advanced Analyses
- Anomaly Detection: Isolation Forest & LOF
- Climate Analysis: Long-term trends and variability
- Environmental Impact: Air quality correlations
- Feature Importance: Random Forest, Correlation, Mutual Information
- Spatial Analysis: Country and continent-level patterns

## Results

### Best Model Performance
- **Model**: Ensemble (Weighted)
- **RMSE**: 0.40°C
- **MAE**: 0.30°C
- **MAPE**: 1.53%
- **R²**: 0.98

### Key Findings

1. FORECASTING MODELS:
   - Ensemble model (Prophet + XGBoost + Moving Average) achieved the best performance
   - Moving Average baseline performed well (RMSE: 0.57°C)
   - ARIMA/SARIMA models showed poor performance and would benefit from parameter tuning

2. TEMPERATURE PATTERNS:
   - Strong seasonal variation (peak in summer, low in winter)
   - Average temperature: 22.23°C (median: 24.30°C)
   - Temperature range: -24.9°C to 49.2°C

3. PRECIPITATION PATTERNS:
   - Highly skewed distribution (most days have no precipitation)
   - Average precipitation: 0.14 mm/day
   - Maximum daily precipitation: 42.24 mm

4. AIR QUALITY:
   - Humidity negatively correlates with most pollutants
   - Ozone increases with temperature (r = 0.28)
   - Wind speed helps disperse pollutants (negative correlations)

5. GEOGRAPHICAL PATTERNS:
   - Africa: Hottest continent (25.45°C average)
   - North America: Coldest continent (10.73°C average)
   - South America: Highest humidity (80.34%)

6. FEATURE IMPORTANCE:
   - "Feels like" temperature is the strongest predictor
   - Humidity and UV index are important features
   - Air quality parameters have moderate importance


## Conclusion

The ensemble forecasting model achieved high accuracy (R² = 0.98) in predicting temperature trends. The analysis identified strong seasonal patterns, geographical variations, and relationships between weather parameters and air quality. These findings demonstrate the effectiveness of combining multiple forecasting approaches and provide insights into global weather patterns.

## Author

Devansh Thakkar
- Email: devanshthakkar1980@gmail.com
- LinkedIn: www.linkedin.com/in/devansh-thakkar-192647284
- GitHub: DevanshThakkar19
