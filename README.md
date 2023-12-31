# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
My project was focused on analyzing businesses around various bike stations within Portland Oregon with focus on Biketown to see if there's a correlation between the number of bikes available at the station and the Average Reviews of the businesses within that station.

## Process
To accomplish my goal, I took the following steps: 
-I queried the City Bikes API to get bike stations for Biketown. This gave me 238 bike stations within the city. This result also included the latitude and longitude of each of the bike stations. -Next, I sent requests to both Foursquare and Yelp APIs to give me results of any business within a 1000m radius of each bike station. I also used a limit of 50 business per bike station. -After recieving and reviewing results from the both APIs, I decided to adopt the result from Yelp API as it provided me more information to help accomplish my goal. I ended up with a list of 4754 businesses. -Using this information -My next step was to merge data from the city bikes and the Yelp API into one. This way, I was able to pull data about each bike station alongside the corresponding business. I now had data like station name, number of bikes, rating and number of reviews in the same table. 
-To store my data, I created a sqLite3 database and stored my table in it. -I also carried out some exploratory data analysis on the data to help me understand the data set and a verification process to ensure my merge was successful and all the required data is present. 
-Next, I grouped the data by the station name, averaging the reviews for all the corresponsing businesses and also pulling in the number of bikes for each station. This narrowed my data down from 4754 rows to 238 rows. -Lastly, I built the regression model to define the relationship between the number of bikes in each station and the reviews of the businesses within a 1000m radius of that station.

## Results
In my chosen area, I found that the Yelp API provided a better quality of data with respect to the number of data points for each of the businesses and also the number of businesses returned. Yelp APi returned 4754 businesses for 238 bike stations while Foursquare API returned only 1015 businesses.

For the model, I was able to establish a statistically significant relationship between the independent variable (Number of bikes) and dependent variables (Reviews). However, I also mentioned that the relationship between them is weak as evidenced by the low R-squared value.

## Challenges 
I faced a couple of challenges while working on the project. I struggled working in a new environment and couldn't import any of the required libraries as they are all installed in a different environment. I also struggled with the Yelp API as there is a limit of 500 requests per day and I had no idea as such I had to use data for a different city. I assumed my code was wrong and wasted precious time troubleshooting. Lastly, I was not so sure how to go about the regression modelling as I had initially done a stats data check by using Average Rating and couldn't find data points with any significant relationship.

## Future Goals
In the future, I would love to learn more about error handling and how to understand errors arising from my code.
