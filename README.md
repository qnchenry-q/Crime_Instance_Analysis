# Crime in Austin, Insights
"Justice is the sum of all moral duty" - William Godwin

One of the chief duties of the ideal state is the policing of the state in a just manner. The city of Austin houses data online for occurrences of arrests. Most of the data was pertaining to either time or location. My goal was to glean this data for insights into how the city is policed and by extension how the city can be policed more efficiently and/or justly. 
# More on the Data
[The data can be found here](https://www.kaggle.com/jboysen/austin-crime) There are ~159k data entries in the full set, however only 18% of the rows were fully populated upon my inspection. To get the ball rolling, I dropped all columns that didnt have coordinates. This reduced the set to 72,273 entries. 

The fields can be categorized three ways. Some fields describe the location, others the time, and a few provide information about the incident. I made the assumption early on that, in whatever machine learning models I applied, time and location would be the features and the target would be some descriptive value.

I ended up creating a categorical field derived from the description of the crime. Essentially, a crime was labeled 'severe' or 'non-severe'. This binary classifier was the target for my machine learning models. 
# Clustering
I knew from previous experience that cities are split into districts to aid police allocation. Since a large part of the data was pertaining to location, I created my own clusters using K-means. To decide how mamy clusters to use I first used a silhoutte score, which suggested I divide the city into North and South. However, I made the call to have the clusters be more granular, in sacrifice of time. I decided on 9 clusters to mirror the number of divisions the Austin police department uses. The algorithm was able to cluster the data seamlessly.
# Random Forest
# Takeaways
# Future Work
