# Forecasting Maximum Daily Temperature in the LR Area (1960)

### Overview
This project analyzes and forecasts maximum daily temperatures for the Little Rock (LR) area, using historical data from **1940–1959**.  
The goal was to develop statistical time series models to predict the maximum daily temperature for 1960, comparing model performance using error metrics and visual forecasts.

---

### Repository Contents
| File | Description |
|------|--------------|
| **`3_LRArea.xlsx`** | Dataset containing historical daily temperature data for the LR area (1940–1959). |
| **`STAT TEST.Rmd`** | R Markdown source file with all preprocessing, modeling, and visualization code. |
| **`Forecasting_Final_Project_Report.pdf`** | Final written report summarizing methodology, model selection, results, and conclusions. |

---

### Methods

#### 1. **Data Preparation**
- The dataset was formatted as a time series of maximum daily temperatures.  
- Each year was treated as one season (`m = 365`).  
- Data from 1959 was reserved as the validation set.

#### 2. **Models Applied**

##### **Holt-Winter’s Additive Smoothing**
- Decomposes data into level, trend, and seasonal components.  
- Parameters (`α`, `β`, `γ`) were optimized to minimize RMSE.  
- Best-fit parameters:  
  - α = 0.6297  
  - β = 0  
  - γ = 0.4822  

##### **SARIMA Modeling**
- Seasonal ARIMA models capture autocorrelation and seasonality directly.  
- The best model selected via AIC was SARIMA(1, 0, 4) × (0, 1, 0)<sub>365</sub>.  
- Seasonal differencing was applied once to achieve stationarity.

---

### Results

| Model | MAD | MASE | RMSE | MAPE |
|--------|------|------|------|------|
| **Holt-Winter’s** | 15.484 | 1.604 | 18.013 | 21.842 |
| **SARIMA(1,0,4)×(0,1,0)** | 9.085 | 0.941 | 12.13 | 14.055 |

**SARIMA** demonstrated superior accuracy across all error metrics, effectively capturing the variability of temperature trends for 1960.

---

### Visualization
- Both models produced 1960 forecasts plotted alongside historical data.  
- SARIMA’s forecasts (in red) aligned more closely with observed patterns than Holt-Winter’s (in blue).

---

### Conclusion
The SARIMA(1,0,4)×(0,1,0) model provided the most reliable forecast for 1960 maximum daily temperatures in the LR area.  
Future improvements could involve:
- Applying rolling validation for adaptive model tuning, and  
- Incorporating external climate variables (e.g., precipitation, pressure).

---

### Tools & Libraries
- **Language:** R  
- **Packages:** `forecast`, `tseries`, `ggplot2`, `readxl`  
- **Environment:** RStudio

