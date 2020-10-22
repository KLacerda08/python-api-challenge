Weather data from 500+ cities across the world was obtained using the OpenWeatherMap API at 
https://openweathermap.org/api. 

First, 1500 random geocoordinates were identified throughout the world 
(using numpy), spanning the full range of latitude (-90 to 90) and longitude (-180 to 180) possibilities. 
These  coordinates were then fed into citipy to identify 500+ cities in the vicinity of the random coordinates. 
The cities were then passed into the OpenWeatherMap API call to identify various identifiers and weather 
characteritics, including: 
- latitude and longitude (as logged by the weather API)
- temperature (degrees Fahrenheit or "F")
- % humidity
- % cloudiness
- wind speed (miles per hour or mph)
- city id (as logged by the weather API)
- city name (as logged by the weather API), and 
- country (as logged by the weather API)

A time pause was utilized so as not to send more then 60 calls per minute.  The data was saved to a dataframe, and
the following analyses were performed via scatter plot and linear regression: 

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude
* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

Weather Results: 
Based on the data evaluation and charts, the following conclusions can be drawn: 

- Temperature decreased with distance from the equator.  
- Humidity was not likely dependent on latitude for the timepoint analyzed, with a weak correlation coefficient of 0.18. 
- Cloudiness was not dependent on latitude for the timepoint analyzed, with a very weak correlation coefficient of 0.02. 
- Wind Speed was not dependent on latitude for the timepoint analyzed, with a very weak correlation coefficient of 0.05. 
- The relationship between temperatures and latitude in the northern hemisphere had a very strong correlation coefficient 
	of -0.9. Temperature was highly dependent on latitude: temperatures decreased with increasing latitude (with
	increasing distance from the equator). 
- The relationship between temperatures and latitude in the southern hemisphere had a strong correlation coefficient 
	of -0.65. Temperature was dependent on latitude: temperatures increased with increasing latitude (with
	decreasing distance to the equator). 
- Humidity, Cloudiness, and Wind Speed were not strongly correlated to latitude in either the northernor southern 
	hemispheres.  