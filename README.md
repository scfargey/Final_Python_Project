# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
My goals in this project are to start understanding how to work with APIs as well as how to manipulate the data retrieved from them. In addition, building a clean dataset inside Python and then transforming it into a database. Since I have only ever worked with data from SAP databases in my work history this was a new and exciting challenge for me. 

## Pull CityBikes Data and store in CSV Files for consumption and analysis later (see City_Bikes.ipynb)
In this project, we aimed to extract and analyze data from a bike-sharing network to better understand station availability and e-bike presence. The process began by ensuring that the necessary data structure was available for manipulation. Specifically, we checked whether the dataset, contained information about both the network and its stations. This step was crucial to prevent potential errors in case the data was missing or improperly structured.

Once the existence of the required data was confirmed, we extracted the list of stations nested within the network information. For each station, we proceeded to extract key details such as the station name, geographic coordinates (latitude and longitude), the number of free bikes available, the number of e-bikes (if present, as this information was stored in a separate nested structure), and the number of empty bike slots. This extraction involved looping through all available stations and collecting this information in a structured format

The extracted data was then stored in a list of dictionaries, where each dictionary represented an individual station and its associated data. To facilitate further analysis and visualization, this list was converted into a pandas DataFrame, a common data structure in Python used for tabular data. Finally, we displayed the DataFrame to provide a clear view of the collected station information, making it easier to perform subsequent analyses or visualizations on the dataset.

This structured approach ensures that we can efficiently gather and analyze bike-sharing data, allowing for insights into bike availability and station usage patterns.

## Pull FourSquare and Yelp Data based on our stations information we were able to retrieve from the citybikes API (all restaurants within 1000M radius) (see Yelp_Foursquare.ipynb)
Pulled ans stored all restaurant information based on our bike locations in Vancouver. Utilizing the Yelp API was much easier and provided more intersting datapoints without exhaustive work to understand the API


### Merge the two datasets and then join with the city-bikes data for one large table (joining_data.ipynb)
Process is to now join both our Yelp and Foursquare datasets

## Results
I found the data from the Fourquare API to be incomplete while the Yelp API to be much more complete and easy to work with. The FourSquare APi did not seem to have any data in the Ratings Section when I pulled it in... so i excluded it, then realizing I was going to need the empty columns down the line anyways. I ran out of api requests so luckily I saved the data to a csv file and then pushed to the git hub repository.

In total, the yelp dataset resulted in over double the amount of restaurants and had a more complete datasetwith reviews...



## Challenges 
Overall I feel like this was a very challenging project in such a short amount of time. I hard a hard time finding a visualizaiton that made sense for the this project in addition to having an issue finding a regression model that did not have co-linearity or had logic that truly made sense to build of of. Not having foursquare ratings made this even more of a challenge as I really only had one dataset to work with. 

## Future Goals
If I had more time, I certainly would have spent more time working with the API data to figure out if it was something I was doing incorrectly with the FourSquare API. I also would have spent more time looking for features that could have properly predicted ratings, etc... Something that would have been interesting would have been total ratings, categories of restaurants, and bikes available to avg ratings.

Overall, if there was more time to work on this project I could have properly explored these datasets and APIs to build out a proper project. 
