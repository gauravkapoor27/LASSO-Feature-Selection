# Project Description

## Aim

This project is a simple exercise to demonstrate feature selection using LASSO for time-series data. I attempt to select relevant features for daily electricity spot prices in New Zealand using several exogeneous variables (see data description section below). I use a time-series cross-validation scheme for robust estimation and to avoid overfitting.

## Methodology

- Transforming and scaling data using Yeo-Johnson power transformation.
- Building feature set using lags of all variables
- Building a time-series cross-validation scheme for robust LASSO estimation.
- Identifying and visualizing selected features using LASSO.

## Data Description

**Target Variable**:

- Price ($/MWh) - Daily average electricity spot price in New Zealand.

**Features**:

- Demand (MWh) - Daily average demand for electricity in New Zealand.
- Generation (MWh) - Daily average generation of electricity in New Zealand, separated into generation by fuel type (coal, diesel, gas, geothermal, hydro, wind, and wood).

- Weather Variables

  - Wind Speed (kph) - Daily average wind speed measured across New Zealand.
  - Wind Direction (degrees) - Daily average direction of wind across New Zealand.
  - Precipitation (mm) - Daily average precipitation across several regions in New Zealand.
  - Precipitation Coverage (%) - Daily average proportion of time for which measurable precipitation was recorded.
  - Temperature (C) - Daily average temperature across New Zealand.
  - Dew (C) - Daily average dew point across New Zealand.
  - Humidity (%) - Daily average humidity across New Zealand.
  - Cloud Cover (%) - Daily average proportion of sky covered by clouds across New Zealand.
  - Solar Energy (MJ/m<sup>2</sup>) - Daily average energy from the sun across New Zealand.

Price, demand, and generation data are easily accessible from the Electricity Authority website, see <https://www.emi.ea.govt.nz>.  
Weather data was acquired through a paid subscription service.
