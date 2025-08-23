# Price prediction for AirBnB properties in Paris


## Project Overview

This project explores the development of a pricing recommendation tool for Airbnb hosts in Paris, leveraging both traditional linear regression and 
spatial regression techniques. The goal is to assess how geographical factors, such as proximity to amenities, tourist attractions, 
and neighborhood characteristics, affect Airbnb property prices, and to evaluate whether incorporating spatial features improves predictive accuracy.

## Data
The study is based on a dataset of 84,000 Airbnb listings in Paris, France from InsideAirbnb


## Methodology

### Data Preprocessing
- Handling missing values
- Encoding categorical variables
- Outlier removal 

### Exploratory Data Analysis (EDA & SEDA)
- Price distribution across neighborhoods
- Spatial clustering of listings and prices
- Correlation analysis of features

### Modeling
- Baseline: Ordinary Least Squares (OLS) regression without spatial features
- Extended Models: Gradual integration of spatial features:
  - Distance to amenities (restaurants, cafés, bars, nightclubs, art centers)
  - Kernel Density Estimation (KDE) of amenities
  - Distance to Points of Interest (Eiffel Tower, Louvre, Notre-Dame, Champs-Élysées, Sacré-Cœur, City Center)
  - SLX model (spatial lags of selected predictors)

### Evaluation
- Metrics: RMSE, MAE, Adjusted R²
- Validation: K-fold cross-validation



## Key Results

### Performance Improvements with Spatial Features:
- RMSE: 73.33 → 68.16
- MAE: 53.77 → 48.86
- Adjusted R²: 36.14% → 44.50%

### Main Price Drivers:
- Positive impact: Closer distance to Notre-Dame, Eiffel Tower, Sacré-Cœur; higher accommodates/bedrooms; higher review scores; higher density of cafés & nightclubs
- Negative impact: Proximity to Louvre & Champs-Élysées; higher density of art centers

### Conclusion
Incorporating spatial features significantly improves model accuracy and provides actionable insights for Airbnb hosts to set more competitive prices.


## Tools & Libraries
- Python: pandas, numpy, matplotlib, seaborn
- Modeling: scikit-learn, statsmodels
- Spatial Analysis: osmnx, geopandas, libpysal, geopy
- Visualization: matplotlib, seaborn
