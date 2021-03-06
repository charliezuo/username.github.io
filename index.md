---
title       : My Data App 
subtitle    : Canadian New Permanent Residents by Country of Origin
author      : Charlie Zuo 
job         : Data Science Specialization 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, quiz, shiny, interactive]
ext_widgets : {rCharts: [libraries/xChart]}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## About the dataset

1. Canada is a diverse country. People come to Canada from all over the world

![alt text](http://data.gc.ca/sites/default/files/canadapopoutbase.png)

--- .class #id

## Background Info

1. This data product aims to demonstrate that through a Shiny Application 

2. Data is downloaded from Government of Canada [Open Data website](http://data.gc.ca/data/en/dataset/6415c2d6-0e5a-4bf0-868c-b2037b2f1a4f)

3. Data is represented in time series in Quarters (e.g. 2012Q1). Time period is two years.


**Tools used for the application** 

1. [Shiny](http://shiny.rstudio.com/)
    + Using selectInput control to allow users to choose
2. [rCharts](http://rcharts.io/) 
    + Using xCharts library

--- .class #id 

## Data summary

```r
require(reshape2)
Data <- read.csv("can-perm-resid.csv")
names(Data) <- gsub("\\X", "", names(Data))
nData <- melt(Data)
```

```
## Using SourceCountry as id variables
```

```r
head(nData) 
```

```
##                SourceCountry variable value
## 1 People's Republic of China   2012Q1  7864
## 2                      India   2012Q1  6242
## 3                Philippines   2012Q1  7140
## 4                   Pakistan   2012Q1  1955
## 5   United States of America   2012Q1  2103
## 6                       Iran   2012Q1  1175
```

--- .class #id

## Tools used for the application 

1. Easy to use, simply  select a country from left hand side panel

2. It is straightforward, yet very informative about the immigration in Canada 

3. Over 130 countries are represented in this dataset!

4. Please enjoy, hope you like it

**[Immigration App](http://czuo.shinyapps.io/ShinyApp/)**
---







