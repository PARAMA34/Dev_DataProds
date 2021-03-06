---
title       : Developing Data Products Project
subtitle    : Storm & Calamities Explorer
author      : Parama Bhattacharya
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Storm and Calamities Explorer

This presentation is created as part of the project for the coursera Developing Data Products course. The assignment is to reinforce the learning of the concepts 
* Shiny to build data product application
* R-presentation or Slidify to create data product related presentation

---

## The Application

To display the understanding of using shiny to build an application, a simple application called Storm and Calamities Explorer has been developed and deployed at :

The application allows the user to:
* Select inputs like - range of years and type of events
* Select the output to be displayed on the map, or as a graph, or as a table
* Also has an option to download the data

---

## Data Used

This application is based on the U.S. National Oceanic and Atmospheric Administration's (NOAA) storm database.

Dataset has been obtained from [here](https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2FStormData.csv.bz2) and processed for the course project. This is the same file we used for the Cousera's Reproducible Research Course.

Storms and other severe weather events can cause both public health and economic problems for communities and municipalities. Many severe events can result in fatalities, injuries, and property damage, and preventing such outcomes to the extent possible is a key concern.

---

## Data Processing


```r
library(data.table)
storm_data <- fread('storm_calamities.csv')
head(storm_data)
```

```
##    YEAR   STATE  EVTYPE COUNT FATALITIES INJURIES PROPDMG CROPDMG
## 1: 1950 alabama TORNADO     2          0       15 0.02750       0
## 2: 1951 alabama TORNADO     5          0       13 0.03500       0
## 3: 1952 alabama TORNADO    13          6      116 5.45250       0
## 4: 1953 alabama TORNADO    22         16      248 3.07000       0
## 5: 1954 alabama TORNADO    10          0       36 0.60753       0
## 6: 1955 alabama TORNADO     8          5       27 7.58000       0
```




