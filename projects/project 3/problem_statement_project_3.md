Project 3

### Introduction

Product recommendations are ubiquitous today, and it turns out they're fun to make! We're going to jam on some data from the company most famous for product recommendations: Amazon. They need your help to build the next generation of product recommendations for Amazon.com. Use the methods we learned in class to build a recommendation engine for a customer who likes the following titles:

1. Don't Be A Menace To South Central While Drinking Your Juice in the Hood. Id: 5335 ASIN: 6304167725
2. Data Mining Solutions: Methods and Tools for Solving Real-World Problems. Id: 22025 ASIN: 0471253847


### Data 

For this project you'll have two datasets, [people_who_bought.txt](https://s3-us-west-2.amazonaws.com/bi-tech-cp303/project+3/people_who_bought.txt) and [product_catalog.tsv](https://s3-us-west-2.amazonaws.com/bi-tech-cp303/project+3/product_catalog.tsv). The data are from the [Stanford Large Network Dataset Collection](http://snap.stanford.edu/data/index.html#amazon).

*people_who_bought* contains rows of product ids that are frequently purchased together.

```{r}
0,1,2,3,4,5
1,0,2,4,5,15
2,0,11,12,13,14
3,63,64,65,66,67
4,7,16,17,18,19
```
*product_catalog* contains information about the products including the average rating, the number of times downloaded, the product group, 

```{r}
str(catalog)
'data.frame':	536604 obs. of  7 variables:
 $ id           : int  0 1 2 3 4 5 6 7 8 9 ...
 $ avg_rating   : num  NA 5 4.5 5 4 0 4 4.5 4.5 0 ...
 $ downloaded   : int  NA 2 12 1 1 0 17 3 15 0 ...
 $ group        : Factor w/ 11 levels "","Baby Product",..: 1 3 3 3 3 3 3 6 3 3 ...
 $ reviews_count: int  NA 2 12 1 1 0 17 3 15 0 ...
 $ salesrank    : int  NA 396585 168596 1270652 631289 455160 188784 5392 277409 949166 ...
 $ title        : Factor w/ 447032 levels "","_Ism","_snd",..: 1 261101 63371 441724 203636 272520 165483 42508 211023 215889 ...
```

### Tips

* Remember you can pull out the right-hand side of association rules by subsetting: `subset(rules, (lhs %in% c('241')))`. Those associated items could be good recommendations.

* Remember that you're the quantitative expert and the client depends on you to help them make data-driven decisions.  It's *your* job to provide clarity and knowledge on the topic, and to present statistical arguments such that a non-techincal audience can understand your findings. 

* Although you might want to include figures and tables from an exploratory analysis, this is a report for your customer.  That means you should be labeling axes, titling figures and providing all the information necessary to understand your results, and no more.
