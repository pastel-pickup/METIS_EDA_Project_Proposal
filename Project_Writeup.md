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
2) Subway traffic data: 2,504,395 data points of subway station turnstile data in most recent rainiest months: 7/2020, 7/2021, 9/2021. Data from Metropolitan Transportation Authority (MTA). 
3) Flood data: 31,185 data points of reported street flooding incidents from 2010 to 2021. Data from 311 NYC Street Flooding. 

# Algorithms
Data Cleaning and Manipulation in Pandas

1) Rain Data: collapsed all precipitation data of last 3 years into a monthly median precipitation for all 5 NYC boroughs. The month with the highest median precipitation was found to be July.

2) Subway Traffic Data: The following turnstile data were eliminated from analysis: reversed/negative counts, duplicates, and outliers. It was found 95% of MTA turnstiles had 3107 daily counts pre-pandemic. Since during-pandemic data were observed, it was expected daily counts to be 50% of pre-pandemic level. Therefore, max counter of 3100 daily counts was set as a baseline and a mask to filter out outliers for during-pandemic data. It was found the top 10 busiest stations were 1) 34 St - Penn Station, 2) Mets - Willets Point, 3) Fulton St, 4) Grand Central - 42 St, 5) 34 St - Herlad Square, 6) 23 St, 7) 42 St - Port Auth, 8) Path New WTC, 9) 86 St, 10) 125 St. 

3) Flood Data: 311 NYC Street Flooding data were linked with Top 10 Busiest Subway Stations data via zipcode column, and the Top 10 Busiest Subway Stations with Highest Flood Risk were found to be 1) 42 St - Port Auth, 2) 23 st, 3) Mets-Willets Point, 4) 34St - Penn Station, 5) 34St - Herald Square, 6) 125 St, 7) Grand Central - 42 St, 8) 86 St, 9) Path New WTC, 10) Fulton St. 

# Tools
1) DB Browser, SQLite, and SQLAlchemy for extraction, transformation, and loading (ETL) of data into Python
2) Pandas for data manipulation
3) Matplotlib and Seaborn for data visualization

# Communication
1) Rainiest month determined was July:

![rainfall](https://user-images.githubusercontent.com/67651332/149432879-511882c4-1c4d-472c-9603-13adf3a7fa3a.png)

2) Top 10 busiest NYC subway stations around July:

![top_10_busiest_stations](https://user-images.githubusercontent.com/67651332/149432906-478b4b42-9ff7-4540-a23d-b2a83c9521a0.png)

3) Top 10 Busiest Stations with Highest Flood Risk

![top_10_busiest_stations_highest_risk](https://user-images.githubusercontent.com/67651332/149434621-8dd1bd0e-e58a-4043-8e10-473ec856d3be.png)
