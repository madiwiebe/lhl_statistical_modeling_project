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

### API Outputs
The coverage of each API was of good quality. A good number and variety of categories were returned by each platform, and there were minimal null values.

However, the coverage between Foursquare and Yelp had little overlap. When the results from each API were merged, only 157 business results out of a potential 2280 rows were common to both.

There were also discrepancies between the APIs when comparing the calculated distance between the bike station and a given business.

Additionally, each API has a different classification system for categorizing businesses, which means that more data cleaning and standardization would be required to have more accurate results.

### Data Quality
The data had an incredibly scattered distribution, and no parameters passed the Shapiro-Wilks test for normality.
It was therefore not very surprising to see that there existed very few candidates for correlation tests or regression models.
P-values were all very high, and R-squared values were all very low. No model had strong evidence to suggest that a relationship existed between any variables.
The strongest correlation was between distance from a bike station and number of reviews (p-value < 0.05). 
Regression analysis demonstrated that despite the correlation and low p-value, distance was not a good predictor for number of reviews (R-squared: 0.026).
Multivariate regression was not capable of producing a strong model either. When investigating the relationship between the number of free bikes at a bike station and the counts of each business category nearby, it was possible to narrow down the model to only include the most likely categories to be near a bike station, and those categories had low p-values (i.e. were statistically significant). However, even in this case, the R-squared value was low, and so further work would have to be done before using this model as an accurate predictor.

### Overall conclusions





## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
