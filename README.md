# Final-Project-Statistical-Modelling-with-Python
My project was focused on analyzing businesses around various bike stations within the City of Montreal to see if there's a correlation between the number of bikes available at the station and the ratings of the businesses within that station.
## Project/Goals
To accomplish my goal, I took the following steps: -I queried the City Bikes API to get bike stations within the city of Montreal. This gave me 160 bike stations within the city. This result also included the latitude and longitude of each of the bike stations. -Next, I sent requests to both Foursquare and Yelp APIs to give me results of any business within a 1000m radius of each bike station. I also used a limit of 50 business per bike station. -After recieving and reviewing results from the both APIs, I decided to adopt the result from Yelp API as it provided me more information to help accomplish my goal. I ended up with a list of 3182 businesses. -Using this information -My next step was to merge data from the city bikes and the Yelp API into one. This way, I was able to pull data about each bike station alongside the corresponding business. I now had data like station name, number of bikes, rating and number of reviews in the same table. -To store my data, I created a sqLite3 database and stored my table in it. -I also carried out some exploratory data analysis on the data to help me understand the data set and a verification process to ensure my merge was successful and all the required data is present. -Next, I grouped the data by the station name, averaging the ratings for all the corresponsing businesses and also pulling in the number of bikes for each station. This narrowed my data down from 3182 rows to 160 rows. -Lastly, I built the regression model to define the relationship between the number of bikes in each station and the ratings of the businesses within a 1000m radius of that station.

## Process
### (your step 1)
### (your step 2)

## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
