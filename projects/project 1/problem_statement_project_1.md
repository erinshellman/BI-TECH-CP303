# Project 1

### Intro 

Bike-share programs in urban cities are popping up all over the country. These systems allow people to rent bikes from stations for short-term use, then return the bikes to a station at their destination. Seattle recently installed [Pronto](https://www.prontocycleshare.com/) stations in locations all over the city, and Pronto wants to understand what factors predict a successful bike station. Use the methods you learned to help Pronto predict the best locations to install new bike-share stations.

### Data 

Read more about the data [here](https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset).

Both hour.csv and day.csv have the following fields, except hr which is not available in day.csv 

With the structure function, we can see that 

```{r}
str(daily)
'data.frame':	731 obs. of  16 variables:
 $ instant   : int  1 2 3 4 5 6 7 8 9 10 ...
 $ dteday    : Factor w/ 731 levels "2011-01-01","2011-01-02",..: 1 2 3 4 5 6 7 8 9 10 ...
 $ season    : int  1 1 1 1 1 1 1 1 1 1 ...
 $ yr        : int  0 0 0 0 0 0 0 0 0 0 ...
 $ mnth      : int  1 1 1 1 1 1 1 1 1 1 ...
 $ holiday   : int  0 0 0 0 0 0 0 0 0 0 ...
 $ weekday   : int  6 0 1 2 3 4 5 6 0 1 ...
 $ workingday: int  0 0 1 1 1 1 1 0 0 1 ...
 $ weathersit: int  2 2 1 1 1 1 2 2 1 1 ...
 $ temp      : num  0.344 0.363 0.196 0.2 0.227 ...
 $ atemp     : num  0.364 0.354 0.189 0.212 0.229 ...
 $ hum       : num  0.806 0.696 0.437 0.59 0.437 ...
 $ windspeed : num  0.16 0.249 0.248 0.16 0.187 ...
 $ casual    : int  331 131 120 108 82 88 148 68 54 41 ...
 $ registered: int  654 670 1229 1454 1518 1518 1362 891 768 1280 ...
 $ cnt       : int  985 801 1349 1562 1600 1606 1510 959 822 1321 ...
```

More data stuff I need to clean up...

Quarterly rentals
When a rental occurs within the system our software collects basic data about the trip. That data can be exported from our system and used for various types of analysis or research. By making this data available we hope to stimulate that analysis or research amongst a much wider community. Please note, all private data including member names has been removed from these files.

Duration - Duration of trip
Start date – Includes start date and time
End date – Includes end date and time
Start station – Includes starting station name and number
End station – Includes ending station name and number
Bike # - Includes ID number of bike used for the trip
Member Type – Lists whether user was a Registered (annual or monthly) or Casual (1 to 5 day) member. NOTE: The 3-day membership replaced the 5-day during Fall '11.

Station data (in xml)

### Instructions

Conduct an analysis using the techniques we discussed in this module as well as any others you think appropriate. You should discuss the rationale for applying the methods you chose, including a discussion of the assumptions you made, where the assumptions are violated, limitations of the analysis or data, and extensions for future work. Write a brief report (2 - 5 pages) of your analysis.

### Questions to think about

* What other data sources could you pull into this dataset to improve your solution?

### Tips

* Remember that you're the quantitative expert and the client depends on you to help them make data-driven decisions.  It's *your* job to provide clarity and knowledge on the topic, and to present statistical arguments such that a non-techincal audience can understand your findings. 

* Although you might want to include figures and tables from an exploratory analysis, this is a report for your customer.  That means you should be labeling axes, titling figures and providing all the information necessary to understand your results, and no more.

### Submissions

How are they going to turn these in?
