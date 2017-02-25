---
title: "Task 07: dplyr"
date: 17 February 2017
author: Drew Steen
---

# Resources
* R Studio's Data Wrangling Cheat Sheet. List of all R Studio cheat sheets [here](https://www.rstudio.com/resources/cheatsheets/)
* R for Data Science: Chapter 5, 9-12
* Wickham (2014) [Tidy Data](http://vita.had.co.nz/papers/tidy-data.pdf)
* The [dplyr vignette](https://cran.rstudio.com/web/packages/dplyr/vignettes/introduction.html)
* Regular expressions guide - there are many quickstart guides and cheat sheets on the web. I think [this one](http://stat545.com/block022_regular-expression.html) is pretty good.

## Notes on built-in datasets
It makes sense to practice **dplyr** using large-ish data sets, since **dplyr** is designed handle big(ish) data. Because those data sets make the package file size considerably bigger, they are distributed in packages of related data sets. To use the data sets, simply install and load them as you would with a regular pacakge. So, for instance:

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
* Using `nycflights13::flights` and `nycflights13::airlines`:
    * Make a table with two columns: airline name (not carrier code) and median distance flown from JFK airport. The table should be arranged in order of decreasing mean flight distance. Hint: use a `_join` function to join `flights` and `airlines`.
* Make a *wide-format* data frame that displays the number of flights that leave Newark ("EWR") airport each month, from each airline
* Using the **babynames** dataset:
    * Identify the ten most common male and female names in 2014. Make a plot of their frequency (`prop`) since 1880. (This may require two separate piped statements). 
    * Make a single table of the 26th through 29th most common girls names in the year 1896, 1942, and 2014
* Write task that involves some of the functions on the Data Wrangling Cheat Sheet and execute it. You may either use your own data or data packages (e.g., the ones listed [here](https://blog.rstudio.org/2014/07/23/new-data-packages/)).



## Optional challenge
 Using regular expressions, make a plot of the change in frequency of some letter pattern in names. For instance: how has the frequency of female names ending in "leigh" changed over time relative to names ending in "lee"?
