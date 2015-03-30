# Project 2

### Introduction

Twitter is a social media platform that allows users to post 140 character messages to the whole wide Internet. Like many Internet companies, Twitter makes its money by selling ads, but everyone knows that Twitter has a [bot problem](http://www.wsj.com/articles/SB10001424052702304607104579212122084821400). Retailers who buy ad space want to know that they're getting a good return on investment, and not marketing to bots. Twitter needs your help to identify which users are bots so that their accounts can be eliminated and they can reassure their advertising customers that humans are seeing their ads.

### Data 

``{r}
str(users)
``

Read more about the data [here](https://dev.twitter.com/rest/public).

### Instructions

Build a classifier to identify whether a user is a bot using the techniques we've discussed as well as any others you think appropriate. You should discuss the rationale for applying the methods you chose, including a discussion of the assumptions you made, where the assumptions are violated, limitations of the analysis or data, and extensions for future work. Write a brief report (2 - 5 pages) of your analysis.

1. formalize the business problem as a data mining process
2. *define* the outcome(s) variables
3. use *aggregation* and *summaries* to create model inputs
4. report on performance of your final model

### Questions to think about

* What will your output be?
  * a probability?
  * a score?
  * binary outcome (bot or not)?
* What are the consequences of a false-positives? What about false-negatives?
* What other data sources could you pull into this dataset to improve your solution?
  * [twitterR](http://geoffjentry.hexdump.org/twitteR.pdf) 

### Tips

* Remember that you're the quantitative expert and the client depends on you to help them make data-driven decisions.  It's *your* job to provide clarity and knowledge on the topic, and to present statistical arguments such that a non-technical audience can understand your findings. 

* Although you might want to include figures and tables from an exploratory analysis, this is a report for your customer.  That means you should be labeling axes, titling figures and providing all the information necessary to understand your results, and no more.

### Submissions
