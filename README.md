# Wearable Device Data Analysis: Predicting and Detecting Anomalies in Sleep Performance

## Introduction

This project aims to analyze sleep patterns using data from wearable devices. By leveraging machine learning techniques, we seek to predict sleep performance and detect anomalies. The data used in this analysis includes sleep cycles and physiological data collected over several months. Understanding and predicting sleep patterns can help in improving sleep quality and overall health.

## Table of Contents
- [Introduction](#introduction)
- [Data Description](#data-description)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Future Work](#future-work)
- [References](#references)

## Data Description

The data for this project was obtained from Whoop, a wearable device that tracks various physiological metrics. The main datasets include:
- **sleeps.csv**: Contains sleep performance data.
- **physiological_cycles.csv**: Contains physiological cycle data.

### Columns in sleeps.csv:
- `Cycle start time`: Start time of the sleep cycle.
- `Cycle end time`: End time of the sleep cycle.
- `Sleep performance %`: Sleep performance percentage.
- `Asleep duration (min)`: Total duration of sleep in minutes.
- `Light sleep duration (min)`: Duration of light sleep in minutes.
- `Deep (SWS) duration (min)`: Duration of deep sleep (slow-wave sleep) in minutes.
- `REM duration (min)`: Duration of REM sleep in minutes.

### Columns in physiological_cycles.csv:
- Various physiological metrics tracked over time.

## Project Structure

The project is structured as follows:
```
wearable-device-data-analysis/
│
├── data/
│ ├── sleeps.csv
│ ├── physiological_cycles.csv
│
├── notebooks/
│ ├── wearableDeviceDataAnalysis.ipynb
│
├── results/
│ ├── analysis_results.html
│
├── README.md
└── requirements.txt
```

## Installation

To run the analysis, you need to have Python 3.x installed along with the necessary libraries. You can install the required libraries using the following command:

```sh
pip install -r requirements.txt
```

## Usage
1. Data Import and Preprocessing:

- Load the data and handle missing values.
- Convert relevant columns to datetime objects.

2. Exploratory Data Analysis (EDA):

- Visualize sleep performance over time.
- Calculate descriptive statistics.

3. Feature Engineering:

- Create rolling averages and differences between consecutive days for sleep duration.

4. Predictive Modeling:

- Use a RandomForestRegressor to predict sleep performance.
- Evaluate the model using Mean Squared Error (MSE).

5. Anomaly Detection:

- Use the Isolation Forest algorithm to detect anomalies in sleep performance data.

6. Visualize the anomalies.

## Results
- The Mean Squared Error (MSE) of the prediction model is 828.18, which translates to an average prediction error of 28.79 percentage points.
- Anomalies in sleep performance were identified using the Isolation Forest algorithm, highlighting unusual sleep patterns.

## Future Work
- Feature Importance Analysis: Exploring feature importance to understand which factors contribute most to sleep performance prediction.
- Advanced Modeling Techniques: Implementing more advanced machine learning models, such as Gradient Boosting Machines (GBM) or Neural Networks.
- Data Augmentation: Including additional relevant features, such as activity levels, diet, and environmental factors, may improve the model's ability to predict sleep performance.
- Parameter Tuning: Experimenting with different contamination rates and other parameters to optimize the performance of the Isolation Forest algorithm.

## References

Data Source:
- Whoop Data. Learn more about Whoop at: https://www.whoop.com/us/en/the-data/

Libraries and tools used:

- Pandas: Data manipulation and analysis library for Python. Available at: https://pandas.pydata.org/
- Matplotlib: Python plotting library. Available at: https://matplotlib.org/
- Seaborn: Statistical data visualization library for Python. Available at: https://seaborn.pydata.org/
- Scikit-learn: Machine learning library for Python. Available at: https://scikit-learn.org/stable/
