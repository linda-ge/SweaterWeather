# Sweater Weather
Sweater Weather makes apparel recommendations for users based on forecast data from the AccuWeather API. Not sure whether to wear a thick sweater or a coat? Sweater Weather gently guides users to layer appropriately.

# Why?
To demonstrate implementation of React Native in a fun and practical way. To transform accurate information into actionable insights.

# User Stories
- As a user, I want to look up today's forecast for my current location.
- As a user, I want to look up the next week's forecast to pack for my next travel destination.
- As a user, I want to receive recommendations on weather-appropriate apparel.
- As a user, I want to give feedback on whether the recommendation was correct for my personal preference.
- As a user, I want my feedback to better calibrate recommendations going forward.

# About the App
If the user allows the app to access their current location, the geoposition is fed into the AccuWeather API's GET request. Specifically, in `App.js`, this code block below passes the user's latitudinal/longitudinal coordinates into a fetchWeather method that calls the AccuWeather Locations API.
````
navigator.geolocation.getCurrentPosition(
  position => {
    this.fetchWeather(position.coords.latitude, position.coords.longitude);
  }
 ````
From there, the Locations API returns a response including a `locationKey`, which maps multiple-to-1 using geoposition search (e.g. (40.711, 73.9897)), postal code text search (e.g. zip code 10010), or text search using city name (e.g. New York, NY). The `locationKey`, which for New York, NY is 2627449, then calls the Forecast and Current Conditions APIs.
  
# Key Technologies
- React Native
- Expo
- HTML, CSS, JavaScript
- APIs
    - [AccuWeather API](https://developer.accuweather.com/)

# Work
This app is currently in-progress. All code is pushed to a private repository.
