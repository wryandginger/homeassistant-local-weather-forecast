# Homeassistant 12h local weather forecast. ~94% accurate*
This is a fork of HAuser1234/homeassistant-local-weather-forecast
This has been adjusted to accept Temperature in Fahrenheit and wind speed in miles per hour

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
* full English and German support
*
* (Note: Only the English lovelace card displays back in Fahrenheit. This still uses 24 hour time)

# Sensors
Following sensors can be used:
* Barometer (required)
* Temperature (set value to 0 is missing) (optional)
* Wind speed (optional)
* Wind direction (optional)

# Card
English and German version:

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
https://github.com/HAuser1234/homeassistant-local-weather-forecast
https://github.com/sassoftware/iot-zambretti-weather-forcasting
https://integritext.net/DrKFS/zambretti.htm
https://www.mikrocontroller.net/topic/385242
http://www.beteljuice.co.uk/zambretti/forecast.html

.* 94% according to https://github.com/sassoftware/iot-zambretti-weather-forcasting
_

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

