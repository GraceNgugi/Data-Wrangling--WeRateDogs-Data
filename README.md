# Data-Wrangling--WeRateDogs-Data
This project entails wrangling, analyzing and visualizing the WeRateDogs dataset to create interesting and trustworthy analyses and visualizations.  WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. 

To analyze the WeRateDogs dataset, we need to obtain data from three sources as follows:

a. Directly download the WeRateDogs Twitter archive data (twitter_archive_enhanced.csv)

b. Use the Requests library to download the tweet image prediction (image_predictions.tsv)

c. Use the Tweepy library to query additional data via the Twitter API (tweet_json.txt)

### Questions for Analysis

a. Is there a correlation between the retweet counf and favorite count?

b. Determine the most popular Dog stage.

c. Check the most used device. 

### Cleaning the dataset

***Quality issues*** 

NB/ There is a total of 2356 entries. The following have missing data issue. 

1. There are 78 replies in tweets (in_reply_to_status_id, in_reply_to_user_id) missing 2278. 
2. 181 retweets in (retweeted_status_id , retweeted_status_user_id   ,retweeted_status_timestamp) missing 2175.
3. There are 2297 expanded_urls with 59 tweets missing data. 
4. The name column have invalid names such as "a","an", "None".
5. Timestamp data type representend as object which is type 'str'.
6. The rating denominator should be 10 for all fields. 
7. Convert the tweet id data type to string. 
8. Change the name of id column in the tweet data to tweet_id to match that of twitter archive data and image predictions data. 

***Tidiness issue***

1. The dog stages included in separate columns like 'doggo','floofer','pupper','puppo'
2. There are three datasets which should be merged to one dataset. 
