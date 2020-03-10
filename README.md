# python-api-challenge
## Note About Use:
These codes function by looking for config.py file in the same folder as themselves. This file will house the api keys for each respective API (OpenWeather for WeatherPy and GooglePlaces for VacationPy).</br> 
**WeatherPy** looks for api_key = '{Your Key Here}'.</br>
**VacationPy** looks for g_key = '{Your key here}'.</br>
Without these files and formatting the code will not run. They have **NOT** been provided and you will have to create and fill them yourself.
## [/WeatherPy](WeatherPy)
Houses code that performs an analysis and visualizes changes in weather based on an area's latitudinal distance from the equator, as well as the data ouput in csv format and the charts created from the data.
### [WeatherPy](WeatherPy/WeatherPy.ipynb)
Code that performs an analysis and visualizes changes in weather based on an area's latitudinal distance from the equator.
#### *Note:* 
Code calls to OpenWeather API and returns data on a list of cities the code generates at the beginning of the program. This data is then cleaned an saved to a csv file later on which is then read back into the program for data analysis and visualization. This is so if the program is closed before data analysis you don't have to regenerate a new city list and recall the API, you can start from the csv file to analyize data. This means that sample charts provided will also most likely not match exactly the data you will get from running the code as you will be working with a new data set. 
### [/Charts](WeatherPy/Charts)
Charts created by the code in WeatherPy for quick reference rather than having to dig through code. Regression lines are shown for charts depicting weather changes by latitude by hemisphere.
* Charts for the Entire Globe
  * [Temperature by Latitude](WeatherPy/Charts/temp_by_lat.png)
  Scatterplot showing the the maximum temperature in farenheit at a city's given latitude.
  * [Humidity by Latitude](WeatherPy/Charts/humid_by_lat.png)
  Scatterplot showing the the percent humidity at a city's given latitude.
  * [Cloudiness by Latitude](WeatherPy/Charts/cloud_by_lat.png)
  Scatterplot showing the the percent cloudiness at a city's given latitude.
  * [Wind Speed by Latitude](WeatherPy/Charts/wind_by_lat.png)
  Scatterplot showing the the wind speed in miles per hour at a city's given latitude.
* Charts for the Northern Hemisphere
  * [Temperature by Latitude](WeatherPy/Charts/northern_temp_by_lat.png)
  Scatterplot showing the the maximum temperature in farenheit at a city's given latitude, for cities whose latitude is zero (the equator) or greater.
  * [Humidity by Latitude](WeatherPy/Charts/northern_humid_by_lat.png)
  Scatterplot showing the the percent humidity at a city's given latitude, for cities whose latitude is zero (the equator) or greater.
  * [Wind Speed by Latitude](WeatherPy/Charts/northern_wind_by_lat.png)
  Scatterplot showing the the wind speed in miles per hour at a city's given latitude, for cities whose latitude is zero (the equator) or greater.
  * [Cloudiness by Latitude](WeatherPy/Charts/northern_cloud_by_lat.png)
  Scatterplot showing the the percent cloudiness at a city's given latitude, for cities whose latitude is zero (the equator) or greater.
* Charts for the Southern Hemisphere
  * [Temperature by Latitude](WeatherPy/Charts/southern_temp_by_lat.png)
  Scatterplot showing the the maximum temperature in farenheit at a city's given latitude, for cities whose latitude is zero (the equator) or less.
  * [Humidity by Latitude](WeatherPy/Charts/southern_humid_by_lat.png)
  Scatterplot showing the the percent humidity at a city's given latitude, for cities whose latitude is zero (the equator) or less.
  * [Wind Speed by Latitude](WeatherPy/Charts/southern_wind_by_lat.png)
  Scatterplot showing the the wind speed in miles per hour at a city's given latitude, for cities whose latitude is zero (the equator) or less.
  * [Cloudiness by Latitude](WeatherPy/Charts/southern_cloud_by_lat.png)
  Scatterplot showing the the percent cloudiness at a city's given latitude, for cities whose latitude is zero (the equator) or less.
### [/Output Data](WeatherPy/output_data)
Folder for storing data collected from calling the OpenWeather API in csv format for calling on in later analysis.
* [Cities.csv](WeatherPy/output_data/cities.csv)
Data collected by WeatherPy code from OpenWeather API stored in csv format. Allows use of code for data analysis if program is closed and reopened by reading in csv data rather than recalling API.
## [/VacationPy](VacationPy)
Houses code that creates a heatmap of the world based on humidity and finds hotels in cities with the desired weather. ALso houses a static image of the gmaps created for quick reference.
### [VacationPy.ipynb](VacationPy/VacationPy.ipynb)
Code that creates a heatmap of the world based on humidity and finds hotels in cities with the desired weather and marks them on the heatmap. What qualifies as desired weather is as follows:
* Between 65 and 75 degrees Farenheit
* Between 5 and 50 percent cloudiness
* Less than 50 percent humidity
* Wind Speed of less than 10 Miles Per Hour
### [Maps](VacationPy/Maps)
Houses the maps created by VacationPy.
#### *Note:*
These images are static and do not have any functionality associated with using google maps (such as panning and zooming). For these features you must run the code and use the widget that comes up.
* [Humidity Heat Map](VacationPy/Maps/humidity_heat_map.png)
Heat map of the world based on humidity
* [Hotels in Desired Weather Areas](VacationPy/Maps/hotels_in_desired_locations.png)
Above heat map with markers indicating hotels that are in areas of desired weather. 
## Built With
* Python
* Jupyter Notebook
* [OpenWeather API](https://openweathermap.org/current)
* [Google Places API](https://cloud.google.com/maps-platform/places/?utm_source=google&utm_medium=cpc&utm_campaign=FY18-Q2-global-demandgen-paidsearchonnetworkhouseads-cs-maps_contactsal_saf&utm_content=text-ad-none-none-DEV_c-CRE_315916117565-ADGP_Hybrid+%7C+AW+SEM+%7C+BKWS+~+Google+Maps+Places+API-KWID_43700039136946099-kwd-22859391737-userloc_9015305&utm_term=KW_google%20places%20api-ST_google+places+api&gclid=Cj0KCQjw9ZzzBRCKARIsANwXaeLDUMh5TbSiNicSLIGZtCoLDuLdSmJCtow1cc_ozorlD4rxLUsNUtAaAvndEALw_wcB)
## Authors
* Ryan Klueg
