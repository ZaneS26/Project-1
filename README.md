# Project-1-Air Quality Analysis 
# Project Files
- [Dataset (CSV)](https://github.com/ZaneS26/Project-1/blob/main/Project%20%231/AirQuality_Daily_StudentVersion.csv)
- [Jupyter Notebook](https://github.com/ZaneS26/Project-1/blob/main/Project%20%231/Python%20Code.ipynb)
- [Python Script](https://github.com/ZaneS26/Project-1/blob/main/Project%20%231/raw.py)


# Overview

This project analyzes air quality sensor data to explore patterns in:

-PM 2.5

-PM 10.0

-VOC

-Temperature & humidity categories

-Altitude relationships

-AQI health-risk screening (Unhealthy for Sensitive Groups or worse)

# Dataset Expectations

The analysis loads the CSV into a Pandas DataFrame named air_data.
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

Identifies the dates and sensor locations where the maximum PM2.5, PM10, and VOC values occurred

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

# Step 4 — EPA Health Risk Screening (Simplified Categories)

This step screens for potential air quality health risks using EPA-style category breakpoints applied directly to concentration values.

For PM2.5:

Good: 0.0–12.0

Moderate: 12.1–35.4

Unhealthy for Sensitive Groups: 35.5–55.4

Unhealthy: 55.5–150.4

Very Unhealthy: 150.5–250.4

Hazardous: > 250.4

For PM10:

Good: 0–54

Moderate: 55–154

Unhealthy for Sensitive Groups: 155–254

Unhealthy: 255–354

Very Unhealthy: 355–424

Hazardous: > 424

The code then filters and reports all events where:

“Unhealthy for Sensitive Groups” or worse occurred
and lists when and where those events happened for both PM2.5 and PM10.

# Step 5 — Altitude vs Air Quality

Aggregates to one row per sensor

Computes correlations between altitude and mean pollutant values
