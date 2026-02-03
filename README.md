# Project-1-Air Quality Analysis 
# Project Files
 - [Jupyter](notebooks/PythonCode.ipynb)
- [Raw Python script](src/raw.py)
- [Dataset](data/AirQuality_Daily_StudentVersioncsv)

# Overview

This project analyzes air quality sensor data to explore patterns in:

-PM 2.5

-PM 10.0

-VOC

-Temperature & humidity categories

-Altitude relationships

-AQI health-risk screening (Unhealthy for Sensitive Groups or worse)

# Dataset Expectations

The analysis loads the CSV into a Pandas DataFrame (typically named air_data).
Key columns used:

date (formatted like mm/dd/yy)

sensor.name

pm2.5_atm

pm10.0_atm

voc

temperature

humidity

sensor.altitude 

# Analysis Summary
# 1) Summary Statistics & Top Locations

Groups data by sensor.name

Calculates mean/median for PM2.5, PM10, and VOC

Finds top 5 locations by mean pollutant values

# 2) Max Values: When and Where?

Identifies the date(s) and sensor location(s) where the maximum PM2.5, PM10, and VOC values occurred

# 3) Temperature & Humidity Categorization

Creates categories based on assignment bins:

Humidity

Low: < 50%

High: 50–80%

Very High: > 80%

Temperature (°F)

Below Freezing: < 32

Cool: 32–50

Warm: 51–70

Hot: > 70

# 4) Altitude Impact

Aggregates to one row per sensor location

Computes Pearson and Spearman correlations between altitude and PM/VOC values

Also performs a trimmed (outlier-reduced) correlation check

# 5) AQI Health Risk Screening (PM2.5 and PM10)



