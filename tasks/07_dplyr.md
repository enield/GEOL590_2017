---
title: "Task 07: dplyr"
date: 17 February 2017
author: Drew Steen
---

# Resources
* R Studio's Data Wrangling Cheat Sheet. List of all R Studio cheat sheets [here](https://www.rstudio.com/resources/cheatsheets/)
* 

## Notes on built-in datasets
It makes sense to practice dplyr using large-ish data sets. Because those data sets make the package file size considerably bigger, they are distributed in packages of related data sets. To use the data sets, simply install and load them as you would with a regular pacakge. So, for instance:

```
install.packages("nycflights13")
library(nycflights)
```

We will be using two data packages: **nycflight13** and **babynames**. **nycflights13** contains the five distinct data sets:

* airlines
* airports
* flights
* planes
* weather

# Tasks

**All tasks should be done, to the extent possible, using tidyverse syntax including piping and functions.**



* Using the `nycflights13::weather`:
    * Determine whether there are any clear outliers in wind speed (`wind_speed`) that should be rejected. If so, filter those bad point(s) and proceed.
    * What direction has the highest median speed at each airport? Make a table and a plot of median wind speed by direction, for each airport. *Optional fun challenge: If you like, this is a rare opportunity to make use of `coord_polar()`.* 
* Using the **babynames** dataset:
    * Identify the ten most common male and female names in 2014. Make a plot of their frequency (`prop`) since 1880. (This may require two separate piped statements). 
    * 

(draft notes to myself)
* mutate task
    * window task, e.g. ranking task
* summarise task
* join task
* subsetting task
* reshaping task



## Optional challenge
 Using pipes and regular expressions, make a plot of the change in frequency of some letter pattern in names. For instance: how has the frequency of female names ending in "eigh" changed over time?