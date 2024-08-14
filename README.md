# Weather and vacation Data Analysis

## Code Source:
This assignment was completed with the help of Justin Moore from tutoring sessions, Brian Perry TA, Google and Chat GPT.

## Overview

This repository contains two Jupyter Notebooks, WeatherPy and VacationPy, which together form a comprehensive analysis of global weather patterns and provide practical insights for selecting vacation destinations based on favorable weather conditions. The analysis leverages data from the OpenWeatherMap API to explore the relationships between various weather parameters and geographical latitude, and uses this information to identify ideal vacation spots.

## WeatherPy Notebook

WeatherPy is focused on analyzing how different weather parameters change with latitude across the globe. The notebook utilizes data collected from the OpenWeatherMap API and performs the following key tasks:

### Data Collection:

- Random City Selection: A set of random geographic coordinates is generated, and the nearest cities are identified using the citipy library.
- API Requests: Weather data for these cities is retrieved using the OpenWeatherMap API, including metrics such as temperature, humidity, cloudiness, and wind speed.

### Data Analysis:

1. **Temperature vs. Latitude**: Investigates how maximum temperature varies with latitude, typically finding that temperatures decrease as one moves away from the equator.
2. **Humidity vs. Latitude**: Analyzes the relationship between humidity levels and latitude, observing how humidity does not show a strong linear relationship with latitude.
3. **Cloudiness vs. Latitude**: Explores cloud cover distribution across different latitudes, finding weak correlations.
4. **Wind Speed vs. Latitude**: Examines how wind speed varies with latitude, generally showing minimal correlation.

### Visualization:

- Scatter Plots: For each weather parameter, scatter plots are generated to visually inspect the relationships.
- Linear Regression: A linear regression model is fitted to each scatter plot to quantify the relationship between latitude and the weather parameter. The strength of these relationships is evaluated using the r^2 value.
- Hemispherical Analysis: The data is split into Northern and Southern Hemispheres to observe differences in weather patterns.

### Key Findings:

- Temperature: A clear relationship exists between latitude and temperature, with higher latitudes generally experiencing cooler temperatures.
- Other Parameters: Humidity, cloudiness, and wind speed show weaker correlations with latitude, indicating that other factors are likely more influential.

## VacationPy Notebook

VacationPy builds on the insights from WeatherPy to help users identify ideal vacation destinations based on specific weather criteria. This notebook leverages the geographical and weather data to suggest potential travel locations and provides additional tools for planning.

### Criteria-Based Filtering:

- Users can define ideal vacation conditions, such as:
**Temperature Range**: Specifying a comfortable temperature range.
**Humidity Levels**: Filtering out locations with high humidity.
**Cloudiness**: Preferring clear or partly cloudy skies.
**Wind Speed**: Avoiding locations with high wind speeds.
- Filtering: The dataset is filtered based on these criteria to identify cities that meet the desired weather conditions.

### Mapping and Visualization:

- Plotting Vacation Spots: The selected cities are plotted on a map using the Google Maps API, providing a clear visual representation of potential vacation destinations.
- Hotel Identification: For each vacation spot, nearby hotels are identified using the Google Places API, helping users plan their accommodations.

### Use Cases:

- Vacation Planning: Ideal for users looking to plan a vacation with specific weather conditions in mind.
- Travel Agency Tools: Can be used by travel agencies to suggest destinations based on client preferences.

## Dependencies

Both notebooks require the following dependencies:
- Python Libraries: pandas, numpy, matplotlib, requests, scipy, citipy.
- APIs:
     - OpenWeatherMap API: For retrieving weather data.
     - Google Maps API: For visualizing vacation spots and identifying nearby hotels.

## How to Use
- Clone the Repository: Download or clone the repository to your local machine.
- API Key Setup: Insert your API keys for OpenWeatherMap and Google Maps in the relevant cells within the notebooks.
- Run the Notebooks: Execute the notebooks in sequence:
- Start with WeatherPy to analyze global weather patterns.
- Then use VacationPy to find and visualize ideal vacation spots.
- Customization: Modify the weather criteria in VacationPy according to your preferences to find your perfect vacation destination.

## Conclusion
This project provides a powerful tool for analyzing global weather patterns and identifying vacation destinations based on user-defined criteria. By combining real-time weather data with geographic analysis, these notebooks offer valuable insights for travelers and anyone interested in understanding how weather varies with latitude around the world.


