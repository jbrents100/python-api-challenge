# python-api-challenge
The WeatherPy directory contains 2 Jupyter Source Files WeatherPy.ipynb and VacationPy.ipynb which request
relevant data from 2 API providers OpenWeatherMap and Geoapify for over 500 cities within the desired
coordinates, and a repo output_data which contains the output images generated from WeatherPy.ipynb.

The two Jupyter Source Files utilize Pandas library to create DataFrame for each dataset. Matplotlib library was
imported to create series of scatter plots based on different variables. Scipy and linregress were also imported to
help with statistical computation and generate linear regresssion line for the data points. Citipy was imported to
generate list of cities with the coordinates, hvplot was imported for interactive data visualization, and geoviews is
imported to explore and visualize data geographically.

Weather Py

Temperature vs. Latitude

There is a fairly strong negative correlation between temperature and latitude with a correlation coefficient of -0.8440396793326146 on Northern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/451ea4cc-a5a4-4d20-a733-0e45b3ba5fc0)


There is a relatively strong positive correlation between temperature and latitude with a correlation coefficient of 0.7859640683290118 on Southern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/67d96afd-4be0-4499-ba03-e878a7e06cbf)


Humidity vs. Latitude

There is a relatively weak positive correlation between humidity and latitude with a correlation coefficient of 0.1668685706198491 on Northern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/8cbf8a9d-3308-4c1e-a89d-89b1766e16b7)


There is a relatively strong weak correlation correlation between humidity and latitude with a correlation coefficient of 0.1953398276874914 on Southern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/8b80c0f3-0d3d-47d7-820c-dd35bcaa1587)


Cloudiness vs. Latitude

There is a weak positive correlation between cloudiness and latitude with a correlation coefficient of 0.12429937547787359 on Northern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/385cbb78-fb7b-456c-a2a3-8b1e4f86f390)

There is a relatively weak positive correlation between cloudiness and latitude with a correlation coefficient of 0.1746799717585871 on Southern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/0801227b-7aa2-43b5-8d40-9e124043cdb4)

Wind Speed vs. Latitude

There is a negligible to almost no correlation between wind speed and latitude with a correlation coefficient of 0.20141766158895463 on Northern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/bae993e3-bf5f-471d-8eec-6e96ae7c18eb)

There is a weak negative correlation between wind speed and latitude with a correlation coefficient of -0.10997059658473013 on Southern Hemisphere.

![image](https://github.com/jbrents100/python-api-challenge/assets/139916502/64a79258-e5bf-4dfe-9e67-9bbd2a8f2e21)

VacationPy

Create city map that displays a point for every city in the city_data_df DataFrame using data in 
output_data/cities.csv. The size of the point is determined by the humidity level in each city.

<img width="343" alt="Screenshot 2023-10-18 180133" src="https://github.com/jbrents100/python-api-challenge/assets/139916502/502517c1-bd1f-4471-96cf-84dbf1ebfa7e">



Narrow down cities that fit the criteria and drop any results with null values, the criteria are listed below:

A max temperature lower than 27 degrees but higher than 21
Cloudiness less than 3
Wind speed less than 4.5 m/s

Create a new DataFrame called hotel_df which contains columns: City, Country, Lat, Lng, Humidity, 
and Hotel Name. For each city, use the Geoapify API to find the first hotel located within 10,000 metres of
each city and append the results to hotel df in a column called `Hotel Name'.

<img width="401" alt="Screenshot 2023-10-18 175340" src="https://github.com/jbrents100/python-api-challenge/assets/139916502/9740948d-2310-45be-9c0a-204273e45999">

Add the hotel name and the country as additional information in the hover message for each city in hotel 

<img width="334" alt="Screenshot 2023-10-18 175937" src="https://github.com/jbrents100/python-api-challenge/assets/139916502/015d21ac-b4b1-4967-af8e-8cc7e8593b2f">


