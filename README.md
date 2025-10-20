# Weather Forecasting using SARIMA

### Overview
This project focuses on applying time series forecasting techniques to daily temperature data.  
The goal was to **compare and evaluate the performance of Holt–Winters and SARIMA models** in predicting short-term weather patterns, improving forecast accuracy through seasonal decomposition and model tuning.

---

### Objectives
- Analyze historical temperature data to identify trends, seasonality, and residual variance  
- Implement and compare Holt–Winters exponential smoothing and SARIMA models  
- Evaluate model performance using statistical error metrics (RMSE, MAE, MAPE)  
- Visualize forecast accuracy and residual diagnostics  

---

### Tools & Technologies
- **Python:** pandas, NumPy, statsmodels, matplotlib, seaborn  
- **Environment:** Jupyter Notebook  
- **Data Source:** NOAA (National Oceanic and Atmospheric Administration) weather datasets  

---

### Methodology
1. **Data Preprocessing:** Cleaned and formatted daily temperature data for time series analysis  
2. **Exploratory Analysis:** Identified seasonal cycles and trends using decomposition plots  
3. **Model Building:** Fit Holt–Winters and SARIMA models using the statsmodels library  
4. **Model Evaluation:** Compared RMSE, MAE, and AIC to assess predictive accuracy  
5. **Visualization:** Generated time series plots, residual diagnostics, and forecast intervals  

---

### Results
- **SARIMA model outperformed Holt–Winters** with a **15% lower RMSE**  
- Identified strong annual seasonality patterns in temperature variation  
- Produced stable forecasts with minimal residual autocorrelation  
- Built modular and reusable forecasting pipeline in Jupyter Notebook  

---

### Files
- `sarima_forecast.ipynb` – Full notebook including EDA, model fitting, and evaluation  
- `plots/` – Forecast, residual, and seasonal decomposition visuals  
- `summary.pdf` – Project report comparing model accuracy and findings  
