# ha-weather-card-mini
Homeassistant Weather Card Mini (Lovelace)

## Instructions
Copy the weather-card-mini.js and weather-card-mini.css to your www/custom_ui folder in home assistant

Add the following to your configuration.yaml:

```
weather:
  - platform: openweathermap
    api_key: YOUR_API_KEY
    mode: hourly
```

Add the following to your ui-lovelace.yaml file:

```
  resources:
    - url: /local/custom_ui/weather-card-mini.js
      type: js
      
      
  - type: "custom:weather-card-mini"
    entity_weather: weather.openweathermap
    entity_sun: sun.sun
```

## Todo
1. Clean-up code 
2. If today, don't display the day 
3. First weather of forecast should be current weather 
