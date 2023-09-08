# Final-Project-Statistical-Modelling-with-Python

## Project/Goals

The objective of this project was to integrate bike station information with business information.

Bike station information:
- latitude
- longitude
- number of free bikes

Business information: 
- category
- distance from bike station
- ratings
- number of reviews

Bike station information was obtained by querying the citybikes API.

Business information was obtained by querying both Foursquare and Yelp APIs.

By combining this information, relationships between the bike station network and nearby businesses may be studied.

## Process
### 1. Select a bike network to study.
Dublin was chosen, as it had an intermediate number of bike stations (114) and a robust number of nearby businesses.
### 2. Obtain information for each bike station in the bike network.
Station name, latitude, longitude, number of free bikes, and number of empty slots.
### 3. Query the Foursquare API and the Yelp API using bike station latitudes and longitudes.
Parameters of interest included distance from the bike station, business names, business category, ratings, and number of reviews.
### 4. Consolidate Foursquare and Yelp results
Merge Pandas DataFrames, and compare with results when importing results to SQLite database and joining the tables.
### 5. Clean the data 
Standardization, normalization, handling null values.
### 6. Visualize the data
Identify potential patterns, perform some statistical analysis.
### 7. Define specific questions that may be answered by querying the data
- Does distance from a bike station affect the number of reviews for a business?
- Does distance from a bike station affect the ratings for a business?
- Is the density of bike station locations related to the density of business locations?
### 8. Create regression models to evaluate the correlation between variables of interest


## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
