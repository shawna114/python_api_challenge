# Python API Challenge

## Part I - WeatherPy

In this example, I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, a simple Python library and the OpenWeatherMap API were used to create a representative model of weather across world cities. The goal was to create a series of scatter plots to showcase the following relationships:

1. Temperature (F) vs. Latitude
>This models demonstrates if there is a correlation between Latitude and Max Temperature

2. Humidity (%) vs. Latitude
>This models demonstrates if there is a correlation between Latitude and Humidity

3. Cloudiness (%) vs. Latitude
>This models demonstrates if there is a correlation between Latitude and Cloudiness
![City Latitude Vs. Cloudiness](https://github.com/shawna114/python_api_challenge/blob/main/WeatherPy/City%20Latitude%20vs.%20Cloudiness.png?raw=true)

4. Wind Speed (mph) vs. Latitude
>This models demonstrates if there is a correlation between Latitude and Wind Speed

_Data for this analysis was pulled by performing a weather check on each city, using a series of successive API calls. 500+ unique cities were included in analysis._

### Linear regressions models were run for each relationship. The plots were separated into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

- Northern Hemisphere - Temperature (F) vs. Latitude
>There is a strong, negative linear relationship between latitude and max temperatures in the Northern Hemisphere. In the sample set provided, approximately 77% of the variance in max temperature is explained by latitude. As latitude increases, max temperature decreases.

- Southern Hemisphere - Temperature (F) vs. Latitude
>There is a weak positive linear relationship between latitude and max temperatures in the Southern Hemisphere. In the sample set provided, approximately 38% of the variance in max temperature is explained by latitude. As latitude increases, max temperature increases.

- Northern Hemisphere - Humidity (%) vs. Latitude
>There appears to be a very weak positive relationship between latitude and humidity in the Northern Hemisphere. In the sample set provided, approximately 8% of the variance in humidity is explained by latitude. As latitude increases, max temperature also appears to increase.

- Southern Hemisphere - Humidity (%) vs. Latitude
>There appears to be a very weak positive relationship between latitude and humidity in the Southern Hemisphere. In the sample set provided, approximately 11% of the variance in humidity is explained by latitude. As latitude increases, max temperature also appears to increase.

- Northern Hemisphere - Cloudiness (%) vs. Latitude
>There appears to be a very weak positive relationship between latitude and cloudiness in the Northern Hemisphere on the date data was analyzed. In the sample set provided, approximately 3% of the variance in cloudiness is explained by latitude. As latitude increases, cloudiness also appears to increase.

- Southern Hemisphere - Cloudiness (%) vs. Latitude
>There appears to be a very weak positive relationship between latitude and cloudiness in the Southern Hemisphere on the date data was analyzed. In the sample set provided, approximately 6% of the variance in cloudiness is explained by latitude. As latitude increases, cloudiness also appears to increase.

- Northern Hemisphere - Wind Speed (mph) vs. Latitude
>There appears to be a very weak positive relationship between latitude and wind speed in the Northern Hemisphere on the date data was analyzed. In the sample set provided, approximately 4% of the variance in wind speed is explained by latitude. As latitude increases, wind speed also appears to increase.

- Southern Hemisphere - Wind Speed (mph) vs. Latitude
>There appears to be a very weak negative relationship between latitude and wind speed in the Southern Hemisphere on the date data was analyzed. In the sample set provided, approximately 7% of the variance in wind speed is explained by latitude. As latitude increases, wind speed appears to decrease.

On the date data was analyzed, the strongest relationships were observed between latitude and max temps. The strongest relationship between latitude and max temp was observed in the Northern Hemisphere.

## Part II - VacationPy

In this section, I used jupyter-gmaps and the Google Places API in addition to the data pulled in Part I. Filters were placed based on my personal weather preferences to identify my ideal vacation spots.

### The following criteria was used to filter the data:

- Max Temp between 70 and 90 degrees Fahrenheit
- Wind Speed between 0 and 15 Miles Per Hour
- Cloudiness between 0 and 15%

Once cities with ideal weather were identified. An iteration was used to find the first hotel within 5,000 meters of each city, by passing the latitude and longitude values from the data frame to the Google Places API.

This data was appended to a humidity map with markers to demonstrate the location of cities with ideal weather for vacation, along with the name of a hotel within 5,000 meters of the city.
