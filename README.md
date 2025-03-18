# EPA Air Quality AQI Analysis

This project analyzes air quality data collected by the U.S. Environmental Protection Agency (EPA) to assess air pollution levels across different states and counties. The analysis leverages Python libraries such as pandas, NumPy, and statistics to clean, manipulate, and analyze large datasets efficiently. The primary goal is to extract meaningful insights from the AQI (Air Quality Index) data, allowing for improved decision-making regarding public health and environmental policies.

Additionally, a deeper analysis of AQI based on carbon monoxide levels has been conducted in a dedicated project:
🔗 [EPA Carbon Monoxide AQI Analysis](https://github.com/Cyberoctane29/EPA-Carbon-Monoxide-AQI-Analysis) : https://github.com/Cyberoctane29/EPA-Carbon-Monoxide-AQI-Analysis

## Project Overview

The EPA Air Quality AQI Analysis project aims to:

- Analyze AQI data from multiple U.S. states.
- Explore trends in air quality across different regions.
- Perform statistical analysis on AQI data to extract key metrics.
- Provide actionable insights for improving air quality and public health.

The analysis is based on three datasets:

- **c2_epa_air_quality**: Contains AQI records for various U.S. states.
- **epa_ca_tx_pa**: Contains AQI records for California, Texas, and Pennsylvania.
- **epa_others**: Contains AQI records for states other than California, Texas, and Pennsylvania.

## Dataset Structure

The datasets contain the following fields:

- **state_code**: A numerical or string representation of the state code.
- **state_name**: The full name of the state.
- **county_code**: A numerical or string representation of the county code.
- **county_name**: The name of the county.
- **aqi**: A numerical value representing the AQI for that county.

## Data Processing Steps

The data processing steps include:

1. **Loading and Structuring Data**: The AQI data is first loaded into a pandas DataFrame, cleaned, and structured into a list of tuples. Each tuple contains the state, county, and AQI value.

2. **Creating a Dictionary for Fast Lookup**: The tuples are converted into a dictionary where states act as keys, and values are lists of AQI data for each county within the state. This facilitates quick lookups.

3. **Statistical Analysis**: Various statistical measures are calculated, such as the mean AQI per state, the maximum and minimum AQI values, and the percentage of readings with low AQI values (indicating clean air).

4. **County-Specific Analysis**: The data is further analyzed by county, revealing patterns in air quality distribution and highlighting areas with higher pollution levels.

5. **Vectorized Operations with NumPy**: For large-scale numerical operations, NumPy is utilized to perform efficient calculations such as determining summary statistics (mean, median, max, etc.) and identifying regions with the cleanest air.

6. **Data Exploration with Pandas**: The analysis is extended by exploring AQI trends across different states and counties. The dataset is also filtered for specific AQI ranges (e.g., "Moderate" AQI).

## Project Insights

The project provides key insights into air quality patterns:

- **High AQI Regions**: Certain areas, particularly in states like California, exhibit consistently high AQI values, indicating poor air quality.
- **County-Specific Trends**: Counties with high population density, such as Los Angeles, show varying AQI trends compared to rural areas.
- **Clean Air Areas**: A significant portion of the data contains AQI readings that indicate clean air (AQI ≤ 5).
- **AQI Distribution**: Analyzing AQI distribution by state and county can inform public health campaigns and air quality improvement measures.

## Project Highlights

- **Data Loading & Cleaning**: Efficiently loads and cleans large datasets using pandas and NumPy.
- **Statistical Analysis**: Computes key summary statistics such as mean, median, max, and standard deviation for AQI values.
- **Data Exploration**: Filters and analyzes data based on state, county, and AQI ranges.
- **Visualization Support**: Can be extended with visualizations (e.g., heatmaps, bar plots) to further illustrate AQI patterns.

## Future Work

- **Predictive Models**: Explore predictive models to forecast AQI based on historical data and environmental factors.
- **Data Expansion**: Incorporate additional datasets with environmental parameters such as temperature, traffic density, and industrial activity to improve the analysis.
- **Visualization**: Add interactive visualizations to better understand AQI distribution and trends across states and counties.
