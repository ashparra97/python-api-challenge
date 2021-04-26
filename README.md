# python-api-challenge

###### Disclosure: This assignment was done in collaboration with Jason Wang.

## WeatherPy

### Summary 

Through the use of citypy and the OpenWeatherMap APIa, thie assignment gathered data from various cities across the globe. The following information on these random cities was collected: latitude, longitutde, maximum temperature, humidity, cloudiness, windspeed, country, and date information was pulled.

### Process
The dependencies below were using in this section of the assignment:
* import matplotlib.pyplot as plt
* import pandas as pd
* import numpy as np
* import requests
* import time
* import json
* from scipy.stats import linregress
* import time 
* from citipy import citipy
* from api_keys import weather_api_key

A list of cities was generated, and from there, latitude, longitutde, maximum temperature, humidity, cloudiness, windspeed, country, and date information was collected by iterating through the list of cities. This city data was saved into a csv and as its own dataframe.

After the above information was collected and saved in a dataframe, various scatterplots were created to determine the correlations between various factors. The following were plotted using matplotlib: 
* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

A linear regression model was also calcuated for each hemisphere. 

## VacationPy

### Summary 

This half of the assignment uses the city data csv from the previous section. 

### Process 

The following dependencies were imported:
* import matplotlib.pyplot as plt
* import pandas as pd
* import numpy as np
* import requests
* import gmaps
* import os
* from g_api_keys import g_key

The previous csv file was imported and gmaps was then configured. A heat map regarding humidity was created using gmaps. Three conditions were added to the data, and only the cities that fit these conditions were kept: 
- A max temperature lower than 80 degrees but higher than 70
- Wind speed less than 10 mph.
- Zero cloudiness

Once the data was filtered by these conditions, the hotels that were closet to each of these cities were found and entered into the data frame. These hotels were then added to the previously made heatmap as markers.


