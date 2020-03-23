### Data Wrangling,Analyses and Visualization on Weratedogs tweets

### Introduction
The dataset i have wrangled and analysed is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for me to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. 

### Project Details

### Gathering data
* Twitter_archive_enhanced.csv was Provided by Udacity and was loaded into a dataframe called df_archieve.
* Using the tweet IDs in the WeRateDogs Twitter archive, i queried the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt file.Then read this .txt file line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count. 

* The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.)was present in each tweet according to a neural network. This file (image_predictions.tsv) was hosted on Udacity's which i downloaded programmatically using the Requests library and the followng url: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv

### Assessing and cleaning Data
Assessed them visually and programmatically for quality and tidiness issues. Detected 14 quality and 3 tideness issues.Cleaned the issues documented while assessing.
* Ran a loop to replace the null values with None in the archieves table 
* Converted the the data types of tweet_id and timestamp column 
* Replaced the single letters in the names column to None 
* Converted the datatype of tweet_id column from integer to object 
* Replaced the null values with None in the columns 
* Converted the datatypes of  Created_id to datetime, id and id_str to object 
* Replaced the None values to empty strings and added the 4 columns of doggo,pupper,puppo,floofer into a single column called dog_category.
* Dropped unecessary columns
* Added 2 columns from the df_clean dataset to archieve data frame
* Joined the dataframes to get a single dataframe twitter_archive_master.

### Analysis and Visualization
The following were the steps taken in analysis and visualization of the wrangled data
* categories of dogs with highest number of ratings
* categories with highest favorite_count
* Plot the relationship between favorite count and rating numeraor of all 4 categories

### Requirements
* Python
* Numpy
* Pandas
* Matplotlib
* requests
* json
* tweepy
* datetime
