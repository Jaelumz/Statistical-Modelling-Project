# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The primary focus of my project was to analyze businesses in proximity to different bike stations in Portland, Oregon, with a specific emphasis on Biketown. The goal was to investigate whether a correlation exists between the quantity of bikes available at a station and the average reviews of the businesses located in that vicinity.

## Process
Steps followed to achieve project objectives:

- Utilized the City Bikes API to query bike stations for Biketown, resulting in 238 bike stations within the city. This information included the latitude and longitude of each bike station.
- Requests were made to both Foursquare and Yelp APIs to retrieve business results within a 1000m radius of each bike station, limiting the results to 50 businesses per bike station. The outcomes from both APIs, were reviewed and opted for the Yelp API results due to the richer information it provided, resulting in a list of 4754 businesses.
- Next step involved merging data from the City Bikes and Yelp API into a single dataset. This resulted in consolidating information about each bike station alongside corresponding business details, including station name, number of bikes, rating, and number of reviews, all within the same table; after which SQLite3 database was created to store the datatables.
- Subsequently, exploratory data analysis was done to comprehend the dataset and verify the merge for completeness. Afterwards the data was grouped by station name, calculating the average reviews for all corresponding businesses and incorporating the number of bikes for each station. This reduced the dataset from 4754 rows to 238 rows.
- To support findings, a regression model was built to establish the relationship between the number of bikes at each station and the reviews of businesses within a 1000m radius of that station.

## Results
Yelp API delivered a higher quality of data in terms of the quantity of data points for each business and the overall number of businesses retrieved. Specifically, the Yelp API yielded 4754 businesses for 238 bike stations, whereas the Foursquare API only returned 1015 businesses.

In developing the model, a statistically significant relationship between the independent variable (Number of bikes) and the dependent variable (Reviews) was identified; althoough the relationship is weak, as indicated by the low R-squared value.

## Challenges 
- Limitations with the Yelp API, allowing only 500 requests per day, led to the use of data from a different city due to unawareness of this restriction
- Difficulties importing the required libraries installed in a different environment.
- Difficulties with the regression modelling, particularly after a statistical data check using Average Rating failed to reveal any data points with a significant relationship.
- Mistakenly attributing code issues to the limitation, valuable time was spent on troubleshooting.

## Future Goals
Error handling techniques to easily understand and troubleshoot the code
