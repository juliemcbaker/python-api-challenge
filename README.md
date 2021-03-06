# python-api-challenge

Julie Baker
June 2021

WeatherPy is a program that does the following:
1. generates a random list of 1500 latitude-longitude coordinates;
2. uses citipy to identify cities nearest to those coordinates -- for this iteration, 583 cities were found;
3. uses a series of api calls to openweathermap.org to gather weather data for the cities in the list -- 543 cities from the list produced weather results and remained in the list;
4. plots trends between latitude and a subest of weather outcomes (temperature, humidity, cloudiness, and wind speed) to identify whether any relationships exist between the variables.

The following files were generated by WeatherPy:
1. cities.csv (the 543 cities plus their weather data for use in VacationPy)
2. scatterplots: 01_latVtemp.png, 02_latVhumid.png, 03_latVclouds.png, 04_latVwind.png
3. linear regressions for latitude vs. temperature: 05_NorthLatTemp.png, 06_SouthLatTemp.png
4. linear regressions for latitude vs. humidity (%): 07_NorthLatHumid.png, 08_SouthLatHumid.png
5. linear regressions for latitude vs. cloudiness (%): 09_NorthLatClouds.png, 10_SouthLatClouds.png
6. linear regressions for latitude vs. wind speed (mph): 11_NorthLatWind.png, 12_SouthLatWind.png

Brief descriptions of trends are included within the WeatherPy Jupyter notebook

VacationPy is a program that does the following:
1. reads in the cities.csv file that was created by WeatherPy;
2. converts the csv file to a pandas df;
3. uses gmaps to create a heat map of the locations from the list of cities with % humidity determining the intensity of the heat signatures;
4. reduces the list of cities to include those with the following criteria: max temp 65-85F, humidity 30-70%, wind speed 2.5-10mph, cloudiness < 20% -- 13 cities fit this description;
5. creates a df for this small subset of cities;
6. uses google nearbysearch to find the first hotel for each of the cities;
7. generates output that includes the first hotel, its location, and its rating for each city--cities without lodging produce an output that it's being skipped -- 11 cities produced hotel results;
8. adds markers to the heatmap for the cities that remained for the hotel search

The following files were generated by VacationPy:
1. heatmap20June.png (initial heatmap which has a hybrid style cenetered at 0,0)
2. markedheatmap.png (also has hybrid style & 0,0 center)
3. altmarkview.png (which has google standard map & is centered in the Pacific Ocean) -- I'm honestly not sure why it looks the way it does, it's just want generated from some code I had pulled over & didn't need, but left in because the map looked different.
