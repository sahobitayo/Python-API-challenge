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


## Observations and Insights
From part one (WeatherPy), here are some observations and insights that can be made from the data:

- There is a strong, negative correlation between a city's latitude and maximum temperature in the northern hemisphere. That is, as you go farther away from the equator (latitude increases), a city's maximum temperature will generally be lower than cities closer to the equator in the northern hemisphere. This is what I expected to see - for example, it's a lot colder in Minnesota (farther north) than it is in Mexico.

- There is a very weak, positive correlation between cloudiness and a city's latitude for both the northern and southern hemispheres. This is represented in the scatter plots in this notebook for those two factors as the data points being scattered across the graph. As a result, we can conclude that a city's latitude has little to no influence on how cloudy a city is.

- There is a very weak, positive correlation for the northern hemisphere between a city's latitude and wind speed (mph), and there is a very weak, negative correlation for the southern hemisphere for those same two factors. I think the fact that the southern hemisphere has a negative correlation and the northern hemisphere has a positive correlation has to have something to do with the northern hemisphere and southern hemisphere being in opposite seasons from each other. Overall, for both hemispheres, latitude has a small influence on wind speed but not very much. However, it is important to note that the correlation between these two factors for the southern hemisphere is stronger than the correlation between these two factors for the northern hemisphere.

## API Keys
To run these jupyter notebooks locally, you will need to obtain API keys.

For part one, you will need to obtain an API key for the OpenWeatherMap API.

After you have the OpenWeatherMap API key, create a file called config.py in the WeatherPy folder and add the API key to that file:

`weather_api_key="API_KEY_HERE"`

For part two, you wll need to obtain a Google API key from the Google Cloud Platform at https://cloud.google.com and enable the Places API.

After you have the Google API key, create a file called config.py in the VacationPy folder and add the API key to that file:

`g_key="API_KEY_HERE"`

### Jupyter Notebook
For this project, I used jupyter notebook to render and display the results of this analysis. There are two notebook files. One for part one (WeatherPy) and another for part two (VacationPy) of this project.

- [WeatherPy](https://github.com/sahobitayo/Python-API-challenge/blob/master/WeatherPy/Weather.ipynb)
- [VacationPy](https://github.com/sahobitayo/Python-API-challenge/blob/master/VacationPy/Vacation.ipynb)

### Images
Static images of the different visualizations I created can be found [here](https://github.com/sahobitayo/Python-API-challenge/tree/master/Output).


### Tools Used
- **Python**
- **Pandas library**
- **Jupyter Notebook**
- **Matplotlib library**
- **Citipy (will need to be installed in your anaconda environment)**
- **OpenWeatherMap API**
- **Google Places API**
- **jupyter-gmaps**
