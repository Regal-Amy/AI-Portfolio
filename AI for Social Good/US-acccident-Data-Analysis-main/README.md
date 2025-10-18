# US Accidents Data Analysis

## Overview

This project analyzes a dataset of accidents in the United States to uncover patterns and insights related to traffic incidents. The dataset contains information on **500,000 rows** of recorded accidents, including variables such as severity, location, weather conditions, and time of day.

## Dataset

The [dataset](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents) used for this analysis is the "US Accidents (March 2023) - Sampled 500K" dataset, which includes the following key columns:

- **ID**: Unique identifier for each accident.
- **Severity**: The severity of the accident, ranging from 1 (low) to 4 (high).
- **Start_Time**: Timestamp when the accident occurred.
- **End_Time**: Timestamp when the accident ended.
- **Start_Lat / Start_Lng**: Latitude and longitude of the accident's starting location.
- **End_Lat / End_Lng**: Latitude and longitude of the accident's ending location.
- **Temperature(F)**: Temperature at the time of the accident.
- **Visibility(mi)**: Visibility conditions during the accident.
- **Precipitation(in)**: Amount of precipitation at the time of the accident.
- **Weather_Condition**: Descriptive weather conditions.
- **Sunrise_Sunset**: Whether the accident occurred during daylight or nighttime.
- **Traffic_Signal**: Whether there was a traffic signal present at the time of the accident.

## Objectives

The primary objectives of this analysis are:

1. To understand the relationship between weather conditions and accident severity.
2. To explore the impact of visibility and temperature on traffic incidents.
3. To identify patterns in accident occurrence based on time of day and geographic location.

## Methodology

The analysis involves the following steps:

1. **Data Cleaning**: Handle missing values, convert state codes to state names, and format timestamps.
2. **Exploratory Data Analysis (EDA)**: Use visualizations to analyze trends and relationships within the data.
3. **Statistical Analysis**: Apply statistical methods to draw insights regarding factors influencing accident severity.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Conclusion

This analysis aims to provide actionable insights that could help improve road safety and inform traffic management strategies. The findings will be valuable for stakeholders in transportation planning and policy-making.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for more details.

