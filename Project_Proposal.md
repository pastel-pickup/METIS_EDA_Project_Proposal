# What is the framing question of your analysis, or the purpose of the model/system you plan to build?
To determine the top 3 most crowded NYC MTA stations that are also susceptible to infrastructure damage due to future flooding based on relationships between foot traffick turnstile data and FEMA flood map for the 3 rainiest months of NYC of the past 3 years. 

# Who benefits from exploring this question or building this model/system?
- MTA maintenance staff given their staffing shortages due to COVID-19. With this information, MTA could have a narrowed focus on their maintenace efforts in the next 3-5 years to prevent potential loss of life, damage to infrafructure, and surrounding properties. 
- Insurance companies
- Real estate developers
- Residents of surrounding MTA stations
- Tourists and travelers

# What dataset(s) do you plan to use, and how will you obtain the data?
1) MTA Turnstile Data, collected for the last three July months (rainiest month in NYC): July 2019, July 2020, and July 2021. http://web.mta.info/developers/turnstile.html
2) FEMA Flood Maps for NYC: https://hazards.fema.gov/femaportal/prelimdownload/searchResult.action
3) Rainfall/Precipitation Data for rainiest July months: https://www.wunderground.com/history/monthly/us/ny/new-york-city/KLGA/date/2019-7
4) Rainfall/Precipitation Data for rainiest July months from gov site:https://www.weather.gov/wrh/climate?wfo=okx

I plan to join all the tabular data based on July months and maybe days using Pandas. After that, I will overlay the data on a map against the FEMA flood map. 

# What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?
An individual sample for the first dataset would include all the entrances and exits for each station in all 3 July months. An individual sample from the second dataset would be a zipcode with the highest mean rainfall in each July month. 

# If modeling, what will you predict as your target?
I expect to see some busiest stations of MTA that are also in the FEMA floop map that also have the highest mean July rainfall. 

# How do you intend to meet the tools requirement of the project?
I will get both MTA and rainfall data with July months as the common column in .csv format and import these .csv files into Pandas for joining and analysis. If these Panda dataframes are too small, I might need to look into Vaex, a Python library dealing with bigger data. If the data turn out too be bigger, I might need to look into Hadoop or AWS for other big data warehousing and scraping solutions. I might need to utilize geopy, a Python library for mapping geographic locations to connect my FEMA Flood Map with the stations with highest rainfall that are also busiest. 

# Are you planning in advance to need or use additional tools beyond those required?
I might employ some Image Analysis technique that involves overlaying images. 

# What would a minimum viable product (MVP) look like for this project?
I would have mapped the MTA stations with July rainfall data. If I had more time, I would have mapped the above data with FEMA Flood Map, and perhaps predict which 3 top stations will get flooded in the next 3-5 years using Regression Analysis. 



