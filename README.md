
# 2001 US Flights Data Exploration

## Overview

This project encompasses the three phases of the data wrangling process: Gathering, Assessing and Cleaning. The dataset to be wrangled, analyzed and visualized is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs.
The whole data is gathered from different sources on different file formats, its quality and tidiness is assessed visually and programmatically, and then the data is cleaned for analysis and visualization, and finally stored.

## Install

The following packages are required to run the notebook:
-	Jupyter Notebooks
-	Python (includes json, os, re, ...)
-	pandas (includes numpy)
-	requests
-	tweepy
-	Matplotlib

Also, it is required to set up a Twitter Development account, to generate the Consumer key, Consumer_Secret, Access_Token and Access_Secret. Follow the directions in the “How to Apply” section from the link below:
https://developer.twitter.com/en/docs/basics/developer-portal/overview

## Sources

|Sources|Available on|Gathered|
|---|---|---|
|twitter-archive-enhanced.csv|‘WeRateDogs’|Twitter archive file is provided by Twitter to Udacity	Manually from Udacity’s servers|
|image_prediction.tsv|[At this link](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)|Programatically using requests library|
|tweet_json.txt|Twitter|Programmatically scrapped from Twitter’s API using Tweepy library|


## Files

|Files|Description|
|---|---|
|wrangle_act.ipynb|Code for whole data wrangling and data analysis|
|wrangle_report.pdf|Briefly describes the wrangling work|
|act_report.pdf|It communicates the insights and displays the visualization(s) drawn from the wrangled data|
|twitter_archive_master.csv|Store the clean data|

## Dataset

This dataset reports flights in the United States, including carriers, arrival and departure delays, and reasons for delays, in 2001.
This is a large dataset: more than 5.5 million records in total
The dataset can be found in the American Statistical Association (ASA) webpage: 
xxx [here](https://stat-computing.org/dataexpo/2009/the-data.html),
with feature documentation available [here](http://ggplot2.tidyverse.org/reference/diamonds.html).

Supplemental data: http://stat-computing.org/dataexpo/2009/supplemental-data.html

jan 259940	259940
feb 477824	477824
mar 531119	531119
apr 514187	514187
may 529940	529940
jun 520230	520230
jul 538440	538440
aug 544351	544351
sep 490698	490698
oct 443796	443796
nov 417386	417386
dec 429869	429869
	        5,697,780 


## Summary of Findings

In the exploration, I found that there was a strong relationship between the
price of a diamond and its carat weight, with modifying effects from the cut,
color, and clarity grades given to the diamond. The relationship is
approximately linear between price and carat when price is transformed to be on
a logarithmic scale and carat transformed to be on a cube-root scale. I found a
somewhat surprising result initially when the marginal trend for the cut, color,
and clarity variables indicated that higher diamond quality was associated with
lower price. However, higher diamond quality was also associated with smaller
diamonds. When I isolated diamonds of a single carat weight, there was a clear
positive relationship between higher diamond quality and higher diamond price.

Outside of the main variables of interest, I verified the relationship between
diamond carat weight and its x, y, and z dimensions. For the dataset given,
there was an interesting interaction in the categorical diamond quality
features. The lower clarity grades looked like they had slightly better
distribution of cut and color grades than diamonds with the higher clarity
grades.


## Key Insights for Presentation

For the presentation, I focus on just the influence of the four Cs of diamonds
and leave out most of the intermediate derivations. I start by introducing the
price variable, followed by the pattern in carat distribution, then plot the
transformed scatterplot.

Afterwards, I introduce each of the categorical variables one by one. To start,
I use the violin plots of price and carat across clarity. I'm only looking at
the clarity grade plot here since it's the clearest example of how the
categorical quality grades affect diamond pricing. The other two categorical
variables, cut and color, are covered afterwards, using point plots. I've made
sure to use different color palettes for each quality variable to make sure it
is clear that they're different between plots.


The challenge
The aim of the data expo is to provide a graphical summary of important features of the data set. This is intentionally vague in order to allow different entries to focus on different aspects of the data, but here are a few ideas to get you started:

- When is the best time of day/day of week/time of year to fly to minimise delays?
- Do older planes suffer more delays?
- How does the number of people flying between different locations change over time?
- How well does weather predict plane delays?
- Can you detect cascading failures as delays in one airport create delays in others? Are there critical links in the system?
You are also welcome to work with interesting subsets: you might want to compare flight patterns before and after 9/11, or between the pair of cities that you fly between most often, or all flights to and from a major airport like Chicago (ORD). Smaller subsets may also help you to match up the data to other interesting datasets.

Markdown syntax
https://daringfireball.net/projects/markdown/syntax

1st Prize
chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/http://stat-computing.org/dataexpo/2009/posters/wicklin-allison.pdf

2nd Prize
chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/http://stat-computing.org/dataexpo/2009/posters/hofmann-cook.pdf

Others:
chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/http://stat-computing.org/dataexpo/2009/posters/jiang.pdf# udacity-communicating-data-findings
