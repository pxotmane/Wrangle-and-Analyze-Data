## Introduction 
In the real world the data is rarely clean and has been collected from different resources. For this reason it is obvious, before going to the analysis stage and withdrawing conclusions, to do a data cleaning. Mastering data cleaning tools is very important for every data analyst because it allows to draw the desired conclusions while minimizing the risk of erroneous results.  

The data wrangled is from tweet database of Twitter account @dog_rates, also known as WeRateDogs. This dataset is about the humorous comment and rating of dogs in the @dog_rates account. This account is for rating dogs with a humorous comment about the dogs. The rating denominator is 10 and the numerator is more than 10 (14, 12, 17…), the idea for this numerator values that the dogs deserve a rating more than 10, this theory is resumed on this quote: “they’re good dogs Brent”.

## Technologies Used
- Python, Numpy, Pandas, Matplotlib, Seaborn, Requests, Tweepy, Json
- LaTex
- Jupyter Notebook 

## Wrangling process
The data wrangling process goes through 3 major steps: Gathering data, assessing data, cleaning data 

### Gathering data
The data of this project are gathered from three sources as following:
- Twitter archive enhanced: it’s a given data set by the Udacity Data Analyst Nanodegree instructors, this data set is the backbone of this project;
- Image predictions: I must gather data from a TSV file hosted in web server, I got the data by using the request python package to a TSV dataset to can read and analysis the data;
- Twitter API & JSON: the expected is gathering data from Twitter database by using the Tweepy library.

### Assessing data 
After creating three data frame from the gathering data (twitter-archive-enhanced data frame, retweet_count data frame, predict data frame), I explore the data frames to found the issues in each data frame. I perform a visual assessing and programmatically assessing to looking missing values issues, quality issues and tidiness issues (The details of all issues found you find them in the wrangling_report file).

### Cleaning data 
In this step, I tried to solve all issues found in the assessing step. The cleaning of each issue is performing on three steps: define, code and
test.

Before starting the cleaning process, I make a copy of each table to avoid losing or changing the gathered data by mistake.
For the missed values issues detected after the visualization assessing, I tried to extract more values for numerator and denominator ratings. Then, the more important quality problems that needed more work are cleaning the abnormal values of numerator rating and get the year, month also day in Twitter‐archive‐enhanced table.

On the other hand, in the Predict table the most complicate quality issues are get just the right predict with high percentage prediction, also extract the dog images names. Beside this complicated issues, I performed some formatting tasks like capital letters, type of columns, deleting useless columns…
Thereafter, they are two tidiness issues in this project; I merged all three tables in one table after melting the dog stages columns on one column. This two cleaning steps are for facilitation the analysis process after.

I debriefed 20 issues in this project but did not mean the final table is free of issues; the wrangling data is an iterative process in future needing data analysis process.
The final twitter_archive_master table contain 2223 observations with 13 columns, point out same columns had not the same number of observations but not mean are a NaN observations.

## Insights 
### Insight one: the most popular dog breed
After analyzing 2223 observations got from the wrangled data process and plotting it, I notice that the Golden retriever dog breed is the popular dog breed inside the WeRateDogs community by 162 tweets.

### Insight two: the dog breed get the most high retweet
Performing a mean calculation for 10 high‐retweeted dog breeds, I got that the Standard poodie dog breed is the most retweeted with an average of 7563.67 retweet followed by the Bedington terrier dog breed by 7299.50 retweet. Which is not the same as the first insight.

### Insight three: the dog breed get the most high favorite counting
For this insight, I got that the Black‐and‐tan coongound dog breed is most favorite for the most favorite for WeRateDogs twitter account visitors with an average 31161.00 favorite signs followed by the Bedington terrier dog breed with 22942.17 as an average. 

This third insight is not almost in the same way as the second insight where Standard poodie dog breed in the second place as most retweeted dog breed. This relationship between can be verified in the followed insight.

### Insight four: the correlation between favorite count and retweet count for dog breeds
To improve this insight I reuse the favorite mean and retweet mean for each dog breed, after plotting this two variables by using scatter plot, I can notice that the favorite count and retweet are positively correlated in almost observations. Which appear logic for this kind of relationship.

### Insight five: the most used rating for all tweets
For 2223 visitors WeRateDogs Twitter account use rating numerator equal or more than 10 (541 for 12, 446 for 11, 437 for 10, 344 for 13). This notice improve that the visitors accept this humorous principle of rating. 

### Insight six: Variation of tweet_id count, favorit_count, retweet_count values during the year
By using line chart to plotting favorite average and retweet average during the year (x axis) also adding bar chart for tweet count on same axis, I notice that the three variables don’t follow the same variation.

As we can observe the number of tweets increase in November and December but the favorite and retweet average decrease, which is antithesis for other months where the number of tweets decrease. 

## Conclusions
Even a dog breed is very popular for the most tweeters don’t mean is the most favorited or retweeted by other users. The selection of a preferable dog breed is up to others criteria, which need a depth analysis with more variables.

In other side, the increase of tweets number do not mean the increase of the visitors reaction for the tweeted dog breed. It can be explained by confusion of visitors for choosing the preferable dog breed when the number of tweets increase or the rate of dog breed tweets increasing is greater than the rate of favorite and retweet average increasing.<br>
Finally, the originality of humorist rating is what almost visitors prefer for rating the dogs, which mean is the asset of this twitter account.
