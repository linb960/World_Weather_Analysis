# World Weather Analysis

## Overview
The challenge was to have beta testers use input statements to filter out data for their weather preferences based on temperature, which will then identify potential travel destinations and nearby hotels. A map of these destinations with a marker layer map is created using Google Maps.   Finally from this list of destinations the beta testers can then choose four cities and map a travel itenerary using Google Maps Directions and also show a marker layer map of the destinations weather conditions, max temp, longitude, latitude and city name.

## Details
The first part of the challenge required the generation of a set of random numbers that would become longitude and latitude pairs.  These longitudes and latitudes were then used to identify a least 500 cities using the citipy module.  

Step two involved creating a DataFrame using OpenWeatherMap API and with the Latitude and Longitude of the cities get the max temp in farhenheit, percent humidity, percent cloudiness, wind speed and weather description.  

The next step involved asking a user to input their preferred minimum and maximum tempertures.  By importing the information collected in step two, a new City DataFrame based on the users input was created to hold the names of the cities with the weather preferences.  This information was saved to use in the final steps.

Using Google API a search was performed, based on the longitude and latitude of the City DataFrame, to find a hotel in each city and create a new Hotel DataFrame.

This information was then used to create a marker layer map that looks like this: <br>
<img src="https://github.com/linb960/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png" width="800" height="300" />

In the final steps the information of the users preferred cities was honed down to just four cities.  These four cities longitudes and latitudes were used with Google API for directions to show on a map the route here: <br>
<img src="https://github.com/linb960/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map.png" width="800" height="300" />

And a final marker map of the 4 places chosen by the user: <br>
<img src="https://github.com/linb960/World_Weather_Analysis/blob/main/Vacation_Itinerary/WeatherPy_travel_map_markers.png" width="1000" height="500" />

