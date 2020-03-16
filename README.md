# Python-API-challenge

### Background
Let's take the knowledge on Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"


## Part I - WeatherPy
In this project, I will be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I will be utilizing a simple Python library, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities.
My first objective is to build a series of scatter plots to showcase the following relationships:

Temperature (F) vs. Latitude
Humidity (%) vs. Latitude
Cloudiness (%) vs. Latitude
Wind Speed (mph) vs. Latitude

After each plotI will add a sentence or two explaining the graph.
My next objective will be to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Northern Hemisphere - Temperature (F) vs. Latitude
Southern Hemisphere - Temperature (F) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (mph) vs. Latitude
Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots I will explain what the linear regression is modelling such as any relationships noticed and any other analysis.

## Part II - VacationPy
For this project, I will use jupyter-gmaps and the Google Places API for this part of the assignment.

I will create a heat map that displays the humidity for every city from the part I of the project.

I will narrow down the DataFrame to find my ideal weather condition. For example:

- A max temperature lower than 80 degrees but higher than 70.

- Wind speed less than 10 mph.

- Zero cloudiness.

I will drop any rows that don't contain all three conditions. You want to be sure the weather is ideal. I will then use Google Places API to find the first hotel for each city located within 5000 meters of your coordinates. I will plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.



