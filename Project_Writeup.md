# Flood Risk of Top 10 Busiest NYC Subway Stations
Mai Tran

# Abstract
In September 2021, New York City (NYC) experienced a historic flood that submerged NYC subway stations, damaged infracstructure and surrounding properties, and ultimately endangered the livelihood of New Yorkers. In order to better prepare for the next historic flood, it is important to evaluate flood risk of the top 10 busiest NYC subway stations. Flood risk is evaluated based on the rainiest season in NYC and top 10 busiest NYC subway stations with the most flood incidents reported.

# Design
The design of the project essentially merges the top results of three data sets: rain data, NYC subway traffic data, and flood incidents data. Each of the following steps is a filtering process for each data set: 
  1) Find the rainiest month or season in NYC using recent weather data
  2) Find the top 10 busiest NYC subway stations during the rainiest season
  3) Find the top 10 busiest NYC subway stations with the most flood incidents during the rainiest season

# Data
1) Rain data: 165 data points of precipitation in the last 3 years (2019-2021) across all 5 NYC boroughs. Data from National Oceanic and Atmospheric Administration (NOAA). 
2) Subway traffic data: 2,504,395 data points of Metropolitan Transportation Authority (MTA) turnstile data.
3) Flood data: 31,185 data points of 311 NYC Street Flooding data from 2010 to 2021. 

# Algorithms


# Tools
1) DB Browser, SQLite, and SQLAlchemy for extraction, transformation, and loading (ETL) of data
2) Pandas for data manipulation
3) Matplotlib and Seaborn for plotting
4) Geopandas for geo-mapping

# Communication
