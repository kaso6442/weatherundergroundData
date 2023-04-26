# U.S. Weather History

This project uses weather data to track trends and records of temperatures and precipitation across the US. The time frame used is between July 1, 2014 and June 30, 2015. The averages and records are recorded for each of the 365 days. 10 weather stations were chosen from all regions of the country to provide a look at the many types of climates the US contains. The Data table below is how each of the weather station data is stored and there are multiple derived tables from them within the database created. 

The goal of this project is to demonstrate my knowledge and ability to use SQL and Python to create, populate, and manipulate a database. The use of triggers, constraints, indexes, and relationships between tables using foreign keys will be demonstrated through queries on the data set to update and delete items in the database.

## Questions to Answer
1. What days throughout the year were at or above the temperature record since 1880 in half or more than half of the represented regions?
2. How many days, what precentage of the year, was over average?
3. Which months or season is the most consistent? Which is the most unpredictable?
4. Do precipitation and temperature correlate in any way?

## Project Structure
```
Project
   |-- us-weather-history
   |   |-- .ipynb_checkpoints
   |   |   |-- KCLT-checkpoint.csv
   |   |   |-- KCQT-checkpoint.csv
   |   |   |-- README-checkpoint.md
   |   |   |-- actual_max_temp-checkpoint.png
   |   |   |-- queries-checkpoint.ipynb
   |   |   |-- visualize_weather-checkpoint.py
   |   |   |-- visualize_weather_run-checkpoint.ipynb
   |   |   |-- wunderground_parser-checkpoint.py
   |   |   |-- wunderground_scraper-checkpoint.py
   |   |-- KCLT.csv
   |   |-- KCQT.csv
   |   |-- KHOU.csv
   |   |-- KIND.csv
   |   |-- KJAX.csv
   |   |-- KMDW.csv
   |   |-- KNYC.csv
   |   |-- KPHL.csv
   |   |-- KPHX.csv
   |   |-- KSEA.csv
   |   |-- Python_Code
   |   |   |-- .ipynb_checkpoints
   |   |   |   |-- visualize_weather-checkpoint.py
   |   |   |   |-- visualize_weather_run-checkpoint.ipynb
   |   |   |   |-- wunderground_parser-checkpoint.py
   |   |   |   |-- wunderground_scraper-checkpoint.py
   |   |   |-- Images
   |   |   |   |-- .ipynb_checkpoints
   |   |   |   |   |-- actual_max_temp-checkpoint.png
   |   |   |   |-- actual_max_temp.png
   |   |   |   |-- actual_mean_temp.png
   |   |   |   |-- actual_min_temp.png
   |   |   |   |-- actual_precipitation.png
   |   |   |   |-- average_max_temp.png
   |   |   |   |-- average_min_temp.png
   |   |   |   |-- average_precipitation.png
   |   |   |   |-- philadelphia-weather-july14-june15.png
   |   |   |   |-- record_max_temp.png
   |   |   |   |-- record_max_temp_year.png
   |   |   |   |-- record_min_temp.png
   |   |   |   |-- record_min_temp_year.png
   |   |   |   |-- record_precipitation.png
   |   |   |-- visualize_weather.py
   |   |   |-- visualize_weather_run.ipynb
   |   |   |-- wunderground_parser.py
   |   |   |-- wunderground_scraper.py
   |   |-- README.md
   |   |-- Station_Data
   |   |   |-- .ipynb_checkpoints
   |   |   |   |-- KCLT-checkpoint.csv
   |   |   |   |-- KCQT-checkpoint.csv
   |   |   |-- KCLT.csv
   |   |   |-- KCQT.csv
   |   |   |-- KHOU.csv
   |   |   |-- KIND.csv
   |   |   |-- KJAX.csv
   |   |   |-- KMDW.csv
   |   |   |-- KNYC.csv
   |   |   |-- KPHL.csv
   |   |   |-- KPHX.csv
   |   |   |-- KSEA.csv
   |   |-- actual_max_temp.png
   |   |-- actual_mean_temp.png
   |   |-- actual_min_temp.png
   |   |-- actual_precipitation.png
   |   |-- average_max_temp.png
   |   |-- average_min_temp.png
   |   |-- average_precipitation.png
   |   |-- philadelphia-weather-july14-june15.png
   |   |-- queries.ipynb
   |   |-- record_max_temp.png
   |   |-- record_max_temp_year.png
   |   |-- record_min_temp.png
   |   |-- record_min_temp_year.png
   |   |-- record_precipitation.png
   |   |-- visualize_weather.py
   |   |-- visualize_weather_ran.ipynb
   |   |-- visualize_weather_run.ipynb
   |   |-- wunderground_parser.py
   |   |-- wunderground_scraper.py
   ```

-------------

This folder contains data and code behind the story [What 12 Months Of Record-Setting Temperatures Looks Like Across The U.S.](http://fivethirtyeight.com/features/what-12-months-of-record-setting-temperatures-looks-like-across-the-u-s/).

## Code

Code file | Description
---|---------
`wunderground_scraper.py` | Downloads weather data web pages from Weather Underground
`wunderground_parser.py` | Parses the weather data from Weather Underground into a flat CSV file
`visualize_weather.py` | Creates the visualization of the weather data

## Data

Column | Description
---|---------
`date` | The date of the weather record, formatted YYYY-M-D
`actual_mean_temp` | The measured average temperature for that day
`actual_min_temp` | The measured minimum temperature for that day
`actual_max_temp` | The measured maximum temperature for that day
`average_min_temp` | The average minimum temperature on that day since 1880
`average_max_temp` | The average maximum temperature on that day since 1880
`record_min_temp` | The lowest ever temperature on that day since 1880
`record_max_temp` | The highest ever temperature on that day since 1880
`record_min_temp_year` | The year that the lowest ever temperature occurred
`record_max_temp_year` | The year that the highest ever temperature occurred
`actual_precipitation` | The measured amount of rain or snow for that day
`average_precipitation` | The average amount of rain or snow on that day since 1880
`record_precipitation` | The highest amount of rain or snow on that day since 1880

Source: [Weather Underground](http://wunderground.com)
