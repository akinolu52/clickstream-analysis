# E-commerce Traffic Predictor

A Python-based machine learning system for analyzing and forecasting e-commerce website traffic using clickstream data. The project implements multiple forecasting models and provides comprehensive visualization tools for traffic pattern analysis.

## Features

- **Data Preprocessing**
  - Timestamp conversion and feature engineering
  - Missing value handling
  - Holiday detection using US Federal calendar
  - Hourly traffic aggregation

- **Traffic Analysis**
  - Hourly and daily traffic pattern visualization
  - Purchase behavior analysis
  - Event type distribution
  - View-to-purchase conversion tracking

- **Multiple Forecasting Models**
  - XGBoost
  - Random Forest
  - SARIMA (Seasonal ARIMA)
  - Facebook Prophet

- **Model Optimization**
  - Hyperparameter tuning using GridSearchCV
  - Model performance comparison
  - Automatic best model selection

- **Forecasting Capabilities**
  - Multi-hour ahead predictions
  - Confidence intervals for applicable models
  - Peak traffic detection
  - Interactive visualizations

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/ecommerce-traffic-predictor.git

# Install required packages
```pip install -r requirements.txt``` 
I will add the requirements.txt file later

from predictor import ECommerceTrafficPredictor

# Initialize predictor with data
predictor = ECommerceTrafficPredictor('./data/ecommerce_clickstream_transactions.csv')

# Preprocess data
predictor.preprocess_data()

# Train models
predictor.train_xgboost_model()
predictor.train_random_forest_model()
predictor.train_sarima_model()
predictor.train_prophet_model()

# Compare model performance
metrics = predictor.compare_models()

# Generate forecasts
forecast = predictor.forecast_future_traffic(hours=72)

# Visualize results
predictor.plot_forecasts()

