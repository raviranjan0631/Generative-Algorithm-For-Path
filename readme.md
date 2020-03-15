Optimizing Travel RoutesUsing Machine Learning

Project goal** : **** The goal of our project is to **** optimize the travel routes **** for delivery person in a city having multiple number of locations. This problem is divided into two parts: In first part we used **** machine learning **** model on **** New-York taxi **** data and we predicted the travel time for a vehicle to reach from one point to another provided with pickup locations and drop off locations. In Second part, we fed the prediction into **** genetic algorithm **** which decides the best route for delivery vehicle to deliver in multiple location in minimum time.**



Pictorial view of** our **** pipeline:** data -&gt; machine learning algorithm-&gt;genetic algorithm

Data and Features** :** New York City taxi data set was taken fromKaggle.



Exploratory Data Analysis: After loading the data,We started with EDA, where we start our analysis on the travel time in the data.We observed that the values of travel time greater than 7000seconds are outliers.So we cleaned the data and used the data points where values of travel time are less than 7000seconds.Similarly, we removed the data points where the pickup location was not in New York.

Model** :** After doing Exploratory Data Analysis on the data,We started building our machine learning model.We selected an XGBoost model to accommodate for our complex numeric and categorical features.

Optimization** :** When we are provided with multiple locations, we fed these locations to the saved machine learning model, which predict the time to travel between each two given points. Then the algorithm evolves and find the visit order to locations which minimizes time spent in transit.

Results** :** The XGBoost model had an error of 2.65 minutes in estimating a single trip's time for a vehicle. While this is acceptable for one trip, the error may get bigger if we have more locations to visit. The genetic algorithm is useful in optimization and other applications relying on biological processed such as mutation, crossover and selection.