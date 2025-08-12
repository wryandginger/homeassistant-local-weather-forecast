# Homeassistant 12h local weather forecast. ~94% accurate*  (USA Adapted and Enhanced!)
This is a fork of HAuser1234/homeassistant-local-weather-forecast
This has been adjusted to accept temperature in Fahrenheit, wind speed in miles per hour, and displays in 12 hour time format.

Enhancements:
I also break out the forecast across 3, 6, and 12 hours which seems to be accurate for my area. 
I load an "inverted" font at the 12 hour forecast to anticipate the sun level in 12 hours.
I provide a 3, 6, and 12 hour temperature forcast based on the trend. It's fairly accurate (+/- 3 degrees) based on my own sensor data.

This coode assumes you're using a pressure sensor that outputs in hPa (I'm using a kmpcil res005 zigbee environmental sensor)
You also need a weather sensor that that outputs in F and mph (I'm using an Acurite 5n1 weather station connected via rtl_433 to MQTT

# Features
* 2 Forecast Models (Zambretti, and Negretti & Zambra)
  (you may have to change the card to use the other model, depending on which model is more accurate at your location)
* rain probability
* approximate timestamps for weather change (at reboot it can take some time for them to be accurate!)
* text prognosis
* simple temperature forecast
* extract general weather conditions

# Sensors
Following sensors can be used:
* Barometer (required)
* Temperature (set value to 0 is missing) (optional)
* Wind speed (optional)
* Wind direction (optional)

# Card
* Note: Only the English lovelace card displays back in Fahrenheit. 
* Other language cards should still work but they will output centegrade forecasts
* weather_card_en.yaml outputs in 24-hour time and has no changes to the forecast data from the original repo.
* weather_card_en_12hr.yaml is the file with the enhancements I made. (see above)

# Installation
Please contribute ANY upgrades to the card or algorithm - this helps everybody!
* copy weather_forecast.yaml into your custom yaml integrations folder
how to make a integrations folder:
1. add this to your configuration.yaml:

```
homeassistant:
  packages: !include_dir_named integrations
```
  
2. create a folder named 'integrations' in your config directory
3. copy weather_forecast.yaml in this folder

* make changes for your individual setup (edit settings marked in weather_forecast.yaml
* copy the card as a manual yaml config into lovelace. !mushroom required, vertical-stack-in-card required!
* edit the current production of solar entity in the conditional cards


# sources
* https://github.com/HAuser1234/homeassistant-local-weather-forecast
* https://github.com/sassoftware/iot-zambretti-weather-forcasting
* https://integritext.net/DrKFS/zambretti.htm
* https://www.mikrocontroller.net/topic/385242
* http://www.beteljuice.co.uk/zambretti/forecast.html
* .* 94% according to https://github.com/sassoftware/iot-zambretti-weather-forcasting
_

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

