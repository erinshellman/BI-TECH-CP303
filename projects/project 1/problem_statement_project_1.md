Project 1

## Introduction

Bike-share programs in urban areas have popped up all over the country. These systems allow people to rent bikes from stations for short-term use, then return the bikes to a station at their destination. Recently [Pronto](https://www.prontocycleshare.com/) stations have been installed in locations all over Seattle, and Pronto wants to understand what factors predict a successful bike station so they can expand operations. Use the methods you learned to help Pronto predict the best locations to install new bike-share stations.

## Data 

You have one data set, [*bikeshare_2015.tsv*](https://raw.githubusercontent.com/erinshellman/BI-TECH-CP303/master/projects/project%201/data/bikeshare_2015.tsv). The *bikeshare_2015.tsv* file contains the station name, the ride duration in minutes per station, the number of rentals per station, the season, the lat/long of the station, and counts of amenities within a quarter mile of the bike station.

Here's the structure of the data set:
```{r}
str(data)
'data.frame':	1001 obs. of  76 variables:
 $ station                : Factor w/ 252 levels "10th & E St NW",..: 1 1 1 1 2 2 2 3 3 3 ...
 $ season                 : Factor w/ 4 levels "Winter","Spring",..: 2 3 4 1 1 4 3 1 4 3 ...
 $ duration_mean          : num  30 26.8 19.9 18.3 21.4 ...
 $ num_rentals            : int  4382 5144 2786 1286 307 4453 5135 420 1022 1348 ...
 $ id                     : int  199 199 199 199 159 159 159 93 93 93 ...
 $ lat                    : num  38.9 38.9 38.9 38.9 38.9 ...
 $ long                   : num  -77 -77 -77 -77 -77 ...
 $ no_bikes               : int  7 7 7 7 2 2 2 3 3 3 ...
 $ no_empty_docks         : int  7 7 7 7 20 20 20 8 8 8 ...
 $ atm                    : int  1 1 1 1 0 0 0 0 0 0 ...
 $ bank                   : int  4 4 4 4 4 4 4 0 0 0 ...
 $ bar                    : int  1 1 1 1 1 1 1 0 0 0 ...
 $ bench                  : int  0 0 0 0 0 0 0 0 0 0 ...
```

Nearby amenity data was retrieved from [Open Streetmap](https://www.openstreetmap.org/#map=5/51.500/-0.100) with the R package [*osmar*](http://osmar.r-forge.r-project.org/).

## Instructions

Conduct a predictive analysis that addresses the business problem using the techniques we've discussed as well as any others you think appropriate. You should discuss the rationale for applying the methods you chose, including a discussion of the assumptions you made, where the assumptions are violated, limitations of the analysis or data, and extensions for future work. Write a brief report (2 - 6 pages) of your analysis. Be succinct, but don't leave out any details you think are important.

1. formalize the business problem as a data mining process
2. *define* and *describe* the outcome(s) variables
3. *report* on the performance of your final model
4. *advise* the business stakeholders what to do

Sections you'll probably want to include in your report are an introduction to the business problem and brief description of the data, methods, results, and discussion. I've provided [an example report](https://github.com/erinshellman/BI-TECH-CP303/blob/master/projects/project%201/example_project.pdf) from a capstone course I took as a masters student that roughly outlines what you should aim for in your reports. No laughing please!

## Questions to think about

* What outcome are you modeling?
  * Number of rentals?
  * Ride duration?
* What is the output?
  * *e.g.* Will you provide a list of top 5 predictors?
  * A figure?
* What other data sources could you pull into this dataset to improve your solution? Here's some links for inspiration:
  * [Open Street Map in R](http://osmar.r-forge.r-project.org/) 
  * [DC crime data](http://data.octo.dc.gov/metadata.aspx?id=3)

## Tips

* Remember that you're the quantitative expert and the client depends on you to help them make data-driven decisions. It's *your* job to provide clarity and knowledge on the topic, and to present statistical arguments such that a non-technical audience can understand your findings. 

* Although you might want to include figures and tables from an exploratory analysis, this is a report for your customer. That means you should be labeling axes, titling figures, providing all the information necessary to understand your results, and no more.

## Submissions

Assignments will be submitted through Canvas. More info to follow.
