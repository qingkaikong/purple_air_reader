# purple_air_reader

This is a simple script to print out a selected [purple air sensor](https://www.purpleair.com/map?opt=1/mAQI/a10/cC0#7/37.838/-122.24) to screen with the following information:

* sensor label
* temperature
* humidity
* two channel PM2.5 AQI for 
    * current
    * 10 min average
    * 60 min average
    * 1 hour average
    * 6 hour average
    * 24 hour average
    * 1 week average

This is just quick demo of how you can get the purple air sensor recordings. You need to get the key and id of the sensor from [purple air map](https://www.purpleair.com/map?opt=1/mAQI/a10/cC0#7/37.838/-122.24) by clicking the sensor near you and havoring your mouse on "Get This Widget". An example you can see is [here](https://www.purpleair.com/data.json?key=6BR4BQEDL0461CLD&show=68357). You can also check [purple air API documentation](https://docs.google.com/document/d/15ijz94dXJ-YAZLi9iZ_RaBwrZ4KtYeCy08goGBwnbCU/edit) for more details. 

After you get the data from purple air, you can use it in multiple applications, such as 
* Monitor the air quality near you, and set a threshold, if the PM2.5 value is higher than the threshold, send you an email. 
* Build a display at home to show the values using a LCD Screen Display and a micro-controller, or [this one](https://www.amazon.com/gp/product/B07STVP29Y). (suggested by my neighbor and it will be my next step)
* You can also read multiple sensors, and build an algorithm to predict the air quality in a region. 

## Dependencies
In order to convert the raw PM2.5 measurements to [AQI](https://www.airnow.gov/aqi/aqi-basics/), as the numbers shown on purple air map, we need this [python-aqi](https://github.com/hrbonz/python-aqi) package, just install it via pip. 