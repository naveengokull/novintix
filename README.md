# Household Power Consumption Analysis

A complete end-to-end data science project focused on understanding and forecasting household electricity usage using the *Individual Household Electric Power Consumption* dataset. The project includes Exploratory Data Analysis (EDA), supervised forecasting models, unsupervised anomaly detection, usage-based clustering, and a simple rule-based AI module.


## Dataset

Source: UCI Machine Learning Repository
Link: [https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)

### Columns Used

* Date
* Time
* Global_active_power
* Global_reactive_power
* Voltage
* Global_intensity
* Sub_metering_1
* Sub_metering_2
* Sub_metering_3


# Task 1 — Exploratory Data Analysis (EDA)

### Work Completed

* Combined separate Date and Time columns into a unified timestamp.
* Plotted the time-series behavior of Global_active_power.
* Identified missing values, abnormal readings, and unusual spikes.
* Examined daily and hourly power-usage patterns to understand load behavior.

### Visual Analysis

* Time-series trend plots
* Distribution and boxplots
* Daily and hourly pattern analysis (heatmaps and line trends)



# Task 2 — Supervised Learning

### Time-Series Forecasting (Next-Hour Global Active Power)

### Steps Implemented

* Prepared cleaned timestamped data and generated windowed time-series sequences.
* Built and trained forecasting models (such as Linear Regression, Random Forest, or LSTM).
* Evaluated each model using time-series metrics including MAE, RMSE, and MAPE.
* Compared predicted vs actual Global_active_power through visualization.



# Task 3 — Unsupervised Learning

### Anomaly Detection and Daily Usage Clustering

### Components

#### 1. Anomaly Detection

Techniques used include Isolation Forest and statistical thresholding (Z-score or IQR).
Objective: identify unusual consumption behaviors or sudden spikes/drops.

#### 2. Clustering

* Aggregated usage data at a daily level.
* Applied clustering algorithms such as K-Means or DBSCAN.
* Visualized clustered groups to understand behavior trends.

### Cluster Interpretation Examples

* Days with consistently low usage
* Days with moderate or normal consumption
* High-usage or outlier days due to abnormal load patterns



# Task 4 — Rule-Based AI

### Consumption Category Generator

A simple rule-based AI module classifies predicted next-hour power consumption into meaningful categories:

| Category     | Range (kW) | Description                                                |
| ------------ | ---------- | ---------------------------------------------------------- |
| Low Usage    | < 2.0      | Light household load, minimal appliance activity           |
| Medium Usage | 2.0 – 4.5  | Normal operation with mixed appliance use                  |
| High Usage   | > 4.5      | Heavy consumption, potentially multiple appliances running |

### Suggestion Examples

* Low Usage: “Good efficiency. Consider shifting heavy appliances to off-peak hours if needed.”
* Medium Usage: “Moderate load. Check if unused appliances can be turned off.”
* High Usage: “High consumption detected. Avoid running multiple heavy appliances at the same time.”

### Example Output


Predicted Global Active Power: 4.89 kW
Category: High Usage
Suggestion: High consumption detected. Avoid running heavy appliances simultaneously.



