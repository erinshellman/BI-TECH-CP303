# Project 2

### Introduction

Twitter is a social media platform that allows users to post 140 character messages to the whole wide Internet. Like many Internet companies, Twitter makes its money by selling ads, but everyone knows that Twitter has a [bot problem](http://www.wsj.com/articles/SB10001424052702304607104579212122084821400). Retailers who buy ad space want to know that they're getting a good return on investment, and not marketing to bots. Twitter needs your help to identify which users are bots so that their accounts can be eliminated and they can reassure their advertising customers that humans are seeing their ads.

### Data 

```{r}
str(users)
'data.frame':	5983 obs. of  14 variables:
 $ id                     : num  3.07e+09 9.82e+06 9.37e+08 3.02e+09 2.18e+09 ...
 $ bot                    : Factor w/ 2 levels "0","1": 1 1 1 1 1 1 1 1 1 1 ...
 $ followers_count        : int  1680 372 54 140 387 31 192 184 9 3621 ...
 $ friends_count          : int  1867 896 161 1103 372 285 1555 291 46 2517 ...
 $ default_profile        : Factor w/ 2 levels "0","1": 1 2 1 1 2 1 1 2 2 2 ...
 $ default_profile_image  : Factor w/ 2 levels "0","1": 2 2 2 1 2 2 2 2 2 2 ...
 $ favourites_count       : int  0 4325 16 1 1751 0 15 188 2 212 ...
 $ geo_enabled            : Factor w/ 2 levels "0","1": 1 2 1 1 2 1 2 1 1 2 ...
 $ account_age            : num  0.146 7.507 2.476 0.223 1.484 ...
 $ days_since_last_tweet  : num  2.27 2.2 3.57 8.39 2.13 ...
 $ listed_count           : int  29 4 15 1 21 1 0 9 0 145 ...
 $ profile_background_tile: Factor w/ 2 levels "0","1": 1 1 1 1 1 1 1 1 1 2 ...
 $ status_favorite_count  : int  0 2 0 0 0 0 0 0 0 0 ...
 $ verified               : Factor w/ 2 levels "0","1": 1 1 1 1 1 1 1 1 1 1 ...
```

**id:** user id 
**bot:** an indicator variable denoting if a user is a bot
**followers_count:** how many followers do they have?
**friends_count:** how many people do they follow?
**default_profile:** is the profile the default?
**default_profile_image:** is the profile photo the default?
**favourites_count:** how many things has the user 'faved'
**geo_enabled:** have they enabled geolocation services?         
**account_age:** the age in years of the account
**days_since_last_tweet:** the number of days since the user lasted tweeted
**listed_count:** how many people have listed them?
**profile_background_tile:** is the background image the default?
**status_favorite_count:** how many people faved their last tweet?
**verified:** is the user verified?

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
