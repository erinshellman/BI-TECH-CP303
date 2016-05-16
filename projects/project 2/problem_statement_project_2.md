# Project 2

### Introduction

Twitter is a social media platform that allows users to post 140 character messages to the whole wide Internet. Like many Internet companies, Twitter makes its money by selling ads, but everyone knows that Twitter has a [bot problem](http://www.wsj.com/articles/SB10001424052702304607104579212122084821400). Retailers who buy ad space want to know that they're getting a good return on investment, and not marketing to bots. Twitter needs your help to identify which users are bots so that their accounts can be eliminated and they can reassure their advertising customers that humans are seeing their ads.

### Data 

```{r}
str(twitter)
'data.frame':	3176 obs. of  15 variables:
 $ bot                     : int  0 0 0 0 0 0 0 0 0 0 ...
 $ statuses_count          : int  428 6239 80 12 4052 28 21 1379 2212 162 ...
 $ default_profile         : int  1 0 1 1 0 1 1 0 0 0 ...
 $ default_profile_image   : int  0 0 0 1 0 0 0 0 0 0 ...
 $ friends_count           : int  1867 896 161 1103 372 285 1555 291 2517 163 ...
 $ followers_count         : int  1680 372 54 140 387 31 192 184 3621 105 ...
 $ favourites_count        : int  0 4325 16 1 1751 0 15 188 212 340 ...
 $ geo_enabled             : int  0 1 0 0 1 0 1 0 1 0 ...
 $ listed_count            : int  29 4 15 1 21 1 0 9 145 6 ...
 $ account_age_hours       : int  3002 67482 23406 3676 14718 4898 2218 48548 57005 47479 ...
 $ diversity               : num  0.269 0.691 0.797 0.777 0.72 ...
 $ mean_mins_between_tweets: num  182 442 22847 4311 290 ...
 $ mean_tweet_length       : num  76 69.6 113.9 59.4 86.7 ...
 $ mean_retweets           : num  1.58 1.2 1.33 1 2.5 ...
 $ reply_rate              : num  0 0.2455 0.0492 0.5312 0.4419 ...
```

* **bot:** an indicator variable denoting if a user is a bot
* **statuses_count:** how many tweets have they posted?
* **default_profile:** is the profile the default?
* **default_profile_image:** is the profile photo the default?
* **friends_count:** how many people do they follow?
* **followers_count:** how many followers do they have?
* **favourites_count:** how many things has the user 'faved'
* **geo_enabled:** have they enabled geolocation services?         
* **listed_count:** how many people have listed them?
* **account_age_hours:** the age in hours of the account
* **days_since_last_tweet:** the number of days since the user lasted tweeted
* **diversity:** the [lexical diversity](https://en.wikipedia.org/wiki/Lexical_diversity) of their last 50 tweets.
* **mean_mins_between_tweets:** average number of minutes between tweets 
* **mean_tweet_length:** average tweet length
* **mean_retweets:** how many of their tweets are retweets?
* **reply_rate:** how many of their tweets are direct replies to other users?

Read more about the data [here](https://dev.twitter.com/rest/reference/get/users/lookup).

### Instructions

Build a classifier to identify whether a user is a bot using the techniques we've discussed as well as any others you think appropriate. You should discuss the rationale for applying the methods you chose, including a discussion of the assumptions you made, where the assumptions are violated, limitations of the analysis or data, and extensions for future work. Write a brief report (2 - 5 pages) of your analysis.

1. formalize the business problem as a data mining process
2. describe the outcome(s) variables
3. report on performance of your final model

### Questions to think about

* What will your output be?
  * a probability?
  * a score?
  * a tree?
* What are the consequences of false-positives? What about false-negatives?
* What other data sources could you pull into this dataset to improve your solution?
  * [twitterR](http://geoffjentry.hexdump.org/twitteR.pdf) 

### Tips

* Remember that you're the quantitative expert and the client depends on you to help them make data-driven decisions.  It's *your* job to provide clarity and knowledge on the topic, and to present statistical arguments such that a non-technical audience can understand your findings. 

* Although you might want to include figures and tables from an exploratory analysis, this is a report for your customer. That means you should be labeling axes, titling figures and providing all the information necessary to understand your results, and no more.
