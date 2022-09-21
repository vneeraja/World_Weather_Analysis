# World_Weather_Analysis

## Overview of the Project

PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
Our task is to collect and analyze weather data across cities worldwide.
We have been asked to add the weather description to the weather data retrieved. 
Then, we will have the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, we will create a travel route between the four cities as well as a marker layer map.

## Analysis and Visualization 

First, we create a Pandas DataFrame with 2000 of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data.
Our analysis of the data will be split into three main parts, or stages.

1. Collection of the Data: 

We do the following steps:

* Use the NumPy module to generate 2000 random latitudes and longitudes.
* Use the citipy module to list the nearest city to the latitudes and longitudes.
* Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
* Parse the JSON data from the API request.
* Collect the following data from the JSON file and add it to a DataFrame:

City,
country,
Latitude and longitude,
Maximum temperature,
Humidity,
Cloudiness,
Wind speed,
Current Weather Description

![image](https://user-images.githubusercontent.com/111020934/191392427-da72ef52-1d59-4e97-b77d-6244a036a496.png)


2. Finding nearby hotels based on user inputs for a minimum and maximum temperature:

* Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
* Find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.
* Store the name of the first hotel in the DataFrame.
* Add pop-up markers to the map that display information about the city, current maximum temperature, current weather description and a hotel in the city.

![image](https://user-images.githubusercontent.com/111020934/191393275-1e7c0816-56c1-4e3e-ad3e-d91b8078a617.png)

3. Identify four cities from the list of potential travel destinations to create a travel route between the four cities as well as a marker layer map:

* From the map above we pick 4 cities and create a vacation itinerary route to travel between the four cities. 
* Get the latitude-longitude pairs as tuples from each city DataFrame using the to_numpy function and list indexing.
* Create a direction layer map using the start and end latitude-longitude pairs and stop1, stop2, and stop3 as the waypoints.

![image](https://user-images.githubusercontent.com/111020934/191394101-9720c27f-133a-4dd0-90c1-12825896143f.png)


* Create a marker layer map between the four cities by combining the four city DataFrames into one DataFrame.

![image](https://user-images.githubusercontent.com/111020934/191394166-6aa52fd2-c2a8-4106-9ac6-e3e365739232.png)


