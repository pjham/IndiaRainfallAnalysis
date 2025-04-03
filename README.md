# Social Impact Report: Analyzing Rainfall Trends in India (1901-2017)

## Introduction
India's monsoon-dependent economy, agricultural sustainability, and water resource management are deeply influenced by historical and future rainfall trends. This study utilizes rainfall data (1901-2017) to conduct Exploratory Data Analysis (EDA) and develop predictive models, ensuring that climate-related risks are understood and mitigated effectively. The analysis incorporates statistical methods, visualization techniques, and machine learning models to explore seasonal trends, spatial patterns, and forecasting.

---

## Setup Instructions
1. The `.ipynb` file can be run in a **Kaggle notebook environment** where the data will be loaded automatically.
2. If not using Kaggle, manually read the data and store it in a variable `df` in the first cell—the code will still work properly.

---

## Key Findings from Data Analysis

### Long-Term Rainfall Trends
- **Stable Rainfall Patterns**: Most Indian states have experienced stable month-wise rainfall over the past century, except Arunachal Pradesh and the Naga-Mani-Mizo-Tripura region, where noticeable shifts are observed.
- **Monsoon Dependency**: Rainfall is heavily concentrated in the monsoon months (June-September), making water resource planning crucial for the remaining dry months.

### Seasonality & Stationarity in Time Series
- A statistically significant p-value indicates that the time series is stationary, making traditional forecasting models like SARIMA appropriate.
- Autocorrelation (ACF) and Partial Autocorrelation (PACF) plots reveal seasonal dependencies, guiding the selection of SARIMA parameters (1,0,0) X (1,1,1,12) for improved predictions.

### Spatial Variability in Rainfall
- Certain states exhibit highly different rainfall patterns compared to the national average.
- Incorporating spatial information into machine learning models like XGBoost significantly improves prediction accuracy.

---

## Predictive Modeling & Implications

### Time Series Forecasting with SARIMA
- Using the (1,0,0) X (1,1,1,12) SARIMA model, we can predict annual and seasonal rainfall trends.
- **RMSE**: 112.41
- **R²**: 0.61
- **Application**: Governments can use this model for drought preparedness, flood warnings, and agricultural advisories.
- **Limitation**: The model assumes past trends will continue, making it sensitive to climate change-induced anomalies.

### Incorporating ML and Spatial Features
- **RMSE**: 83.31
- **R²**: 0.71 (Clear improvement from subdivision-wise time series model)
- **XGBoost Model with Spatial Data** enhances predictions by capturing geographical dependencies in rainfall.
- **Application**: More precise regional climate models for policymakers in sectors like irrigation, disaster response, and urban planning.

---

## Social & Economic Impact

### Agriculture & Food Security
- 70% of Indian farmers depend on monsoons, making erratic rainfall a threat to food security.
- Using predictive models, crop planning can be optimized by recommending drought-resistant crops in low-rainfall zones.

### Flood & Drought Management
- States like Assam and Bihar suffer from excessive monsoon rainfall, while regions like Rajasthan face recurrent droughts.
- AI-driven flood warning systems can help reduce human and economic losses.

### Climate Change Adaptation
- Long-term rainfall changes indicate possible climate shifts affecting water cycles, biodiversity, and human health.
- **Actionable Insights**: Data-driven policies for river basin management, afforestation, and sustainable irrigation strategies.

---

## Tools & Technologies Used
**Python** – Main programming language  
**Pandas** – Data manipulation & preprocessing  
**NumPy** – Numerical operations  
**Matplotlib** – Data visualization  
**Seaborn** – Advanced plotting (heatmaps, boxplots)  
**Statsmodels** – Time series analysis (Dickey-Fuller test, ACF/PACF, SARIMA)  
**Scikit-learn** – Machine learning utilities (train-test split, evaluation)  
**XGBoost** – Machine learning model for rainfall prediction  


---

## Conclusion
This study provides a data-driven approach to understanding India’s rainfall patterns and forecasting future trends. By leveraging statistical time-series models and machine learning, we can equip policymakers, farmers, and disaster management teams with crucial insights for climate resilience and sustainable development.


---



