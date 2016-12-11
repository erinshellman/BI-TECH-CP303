Project 1

## Introduction

Wild fires destroy millions of hectares of forest every year. Forest fires
are costly and dangerous and fast detection and response is the key to mitigating
their destruction.

## Data 

For this project you'll be using weather and meteorological data from the
northeast region of Portugal to predict the burned area (or size) of forest fires.

Here's the structure of the data set:
```{r}
> str(ff)
'data.frame':	517 obs. of  13 variables:
 $ X    : int  7 7 7 8 8 8 8 8 8 7 ...
 $ Y    : int  5 4 4 6 6 6 6 6 6 5 ...
 $ month: Factor w/ 12 levels "apr","aug","dec",..: 8 11 11 8 8 2 2 2 12 12 ...
 $ day  : Factor w/ 7 levels "fri","mon","sat",..: 1 6 3 1 4 4 2 2 6 3 ...
 $ FFMC : num  86.2 90.6 90.6 91.7 89.3 92.3 92.3 91.5 91 92.5 ...
 $ DMC  : num  26.2 35.4 43.7 33.3 51.3 ...
 $ DC   : num  94.3 669.1 686.9 77.5 102.2 ...
 $ ISI  : num  5.1 6.7 6.7 9 9.6 14.7 8.5 10.7 7 7.1 ...
 $ temp : num  8.2 18 14.6 8.3 11.4 22.2 24.1 8 13.1 22.8 ...
 $ RH   : int  51 33 33 97 99 29 27 86 63 40 ...
 $ wind : num  6.7 0.9 1.3 4 1.8 5.4 3.1 2.2 5.4 4 ...
 $ rain : num  0 0 0 0.2 0 0 0 0 0 0 ...
 $ area : num  0 0 0 0 0 0 0 0 0 0 ...
```

Variable | Description 
-------------- | ------------
X | x-axis spatial coordinate within the Montesinho park map: 1 to 9 
Y | y-axis spatial coordinate within the Montesinho park map: 2 to 9 
month | month of the year: 'jan' to 'dec' 
day | day of the week: 'mon' to 'sun' 
FFMC | FFMC index from the FWI system: 18.7 to 96.20 
DMC | DMC index from the FWI system: 1.1 to 291.3 
DC | DC index from the FWI system: 7.9 to 860.6 
ISI | ISI index from the FWI system: 0.0 to 56.10 
temp | temperature in Celsius degrees: 2.2 to 33.30 
RH | relative humidity in %: 15.0 to 100 
wind | wind speed in km/h: 0.40 to 9.40 
rain | outside rain in mm/m2 : 0.0 to 6.4 
area | the burned area of the forest (in ha): 0.00 to 1090.84 


*Note:* `area` is very skewed towards 0.0, thus it may make sense to model with the logarithm transform.

To learn more about the data, please see: [forest fires](https://archive.ics.uci.edu/ml/datasets/Forest+Fires)

## Instructions

Use the methods you learned in class to develop a model to predict the burn
area. Then, write a short memo to your stakeholders describing your findings and
providing your recommendation. Memo's should be 1 - 2 pages and be written as 
though you're updating your team, or your manager. Be succinct, but don't leave
out any details you think are important.

For this task you'll need to:
1. formalize the business problem as a data mining process
2. *define* and *describe* the outcome(s) variables
3. *report* on the performance of your final model
4. *advise* the business stakeholders what to do

## Tips

* Remember, you're the analyst and your stakeholders depend on you to help them make data-driven decisions. It's *your* job to provide clarity and knowledge on the topic, and to present the concepts so that a non-technical audience can understand your findings. 

* Although you might want to include figures and tables from an exploratory analysis, this is a report for your customer. That means you should be labeling axes, titling figures, providing all the information necessary to understand your results, and no more.

## Submissions

You will submit your memos on the course website.

## Peer review
