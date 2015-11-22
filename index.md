---
title       : Car vs Car
subtitle    : Developing Data Products Course Project
author      : Ven Reddy
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---
## Introduction

This is an application that loads Motor Trend's Car Data (mtcars) and allows
a person to compare two cars against each other using the UI rather
than a command line.



```
##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
##                               names
## Mazda RX4                 Mazda RX4
## Mazda RX4 Wag         Mazda RX4 Wag
## Datsun 710               Datsun 710
## Hornet 4 Drive       Hornet 4 Drive
## Hornet Sportabout Hornet Sportabout
## Valiant                     Valiant
```

--- .class #id 
## Side panel 

The side panel allows you to pick two cars, an attribute to plot.  Click on 
the Submit button to have the application show you the comparison of both cars.

--- .class #id
## Main panel

The main panel shows you what cars that you have selected and also shows
the various attributes for each car such as mpg, cylinders, horsepower, etc.

For example:


```r
# show two cars
data(mtcars)
mtcars$names <- rownames(mtcars)
f <- c("Datsun 710", "Valiant")
filter(mtcars, names %in% f)
```

```
##    mpg cyl disp  hp drat   wt  qsec vs am gear carb      names
## 1 22.8   4  108  93 3.85 2.32 18.61  1  1    4    1 Datsun 710
## 2 18.1   6  225 105 2.76 3.46 20.22  1  0    3    1    Valiant
```


--- .class #id
## Thank you

Thank you for using this application.  I am sure that you will agree that
for the non-R programmer this is a much easier way of comparing two cars
against each other.
