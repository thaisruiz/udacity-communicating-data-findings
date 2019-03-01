
# Flights Data Exploration

## Overview

The objective of this project is to explore the variables of a selected dataset and the relationships between them, and to communicate the main findings using the visualizations from these
 Exploratory and Explanatory Data Analysis. The selected data contains information of domestic flights of period December 2008.

## Install

The following packages are required to run the notebook:
-	Jupyter Notebooks
-	Python
-	pandas (includes numpy)
-	matplotlib
-   seaborn
-	plotly
-   os
-   Counter

## Source

2001_8.csv is available to be downloaded [at this link](http://stat-computing.org/dataexpo/2009/the-data.html), by selecting (individual) year *2008*.

## Files

|Files|Description|
|---|---|
|Flights_exploration.ipynb|Code for whole data exploration through visualizations|
|Flights_slide_deck.ipynb| Brief presentation that illustrates the explanatory analysis|
|output_toggle.tpl|It communicates the insights and displays the visualization(s) drawn from the analysis|


## Dataset

This dataset reports the US flights on December 2008, with information on airlines, origin/destination cities, scheduled and actual arrival/departure times, delays time/causes and cancellation/divert status.

It contains almost 545,000 records and it is a subset of the file 2008.csv.
 
This file can be found in the American Statistics Association (ASA) webpage:
[at this link](http://stat-computing.org/dataexpo/2009/the-data.html), by selecting *2008* in the Get the Data section.
The data documentation is available in the readme.html when downloading the file, and the supplemental data [at this link](http://stat-computing.org/dataexpo/2009/supplemental-data.html).


## Summary of Findings

The flights dataset is comprised by four main datasets, which are exclusive among them: on time, delayed, cancelled and diverted.

A flight is considered on-time if its arrival delay is less than 15 minutes.

Since the interest of the analysis was to determine which airlines had more flight delays and what were the causes on December 2008, the cancelled and diverted flights datasets were removed. 

Per the data wrangling, the sum of the causes delay in minutes totals the arrival delay in the delayed flights subset. 

Per the exploration: 

- Out of 524,747 on track flights on December 2008, 356,100 were on time (67.86%) and 168,647 (32.14%) delayed.
- Out of the delayed set, 92.85% were medium delays and 7.15% long delays (arrival delays greater than ~2.5 hours) 
- Delay causes and airlines rank differently depending on different aspects of the data: 

Delay Causes Ranking (most to least):

|Per contributing time to arrival delays|Per frequency|Per impact on arrival delays|
|---|---|---|
|Late-arriving aircraft|NAS|Weather|
|NAS|Late-arriving aircraft|Late-arriving aircraft|
|Carrier|Carrier|Carrier|
|Weather|Weather|NAS|
|Security|Security|Security|

Airline ranking (best to worst):

|Per proportion of delayed flights|Per the median of the arrival delay|Per the relative frequency of delays by carrier|
|---|---|---|
|Hawaiian (18.5%)|Hawaiian|AirTran (17%)|
|US (26%)|AirTran|SkyWest (20%)|
|American (28%)|Delta|Envoy (21%)|
|United (30%)|US|ExpressJet(1) (22%)|
|ExpressJet (1) (31%)|Frontier|Endeavor (23%)|
|Southwest (31%)|Northwest|Alaska(25%)|
|Mesa (31%)|ExpressJet|American(25%)|
|AirTran (32%)|Alaska|United(25%)|
|Endeavor (33%)|Endeavor|Delta(26%)|
|Delta (33%)|American|Continental(27%)|
|Skywest (34%)|Southwest|ExpressJet(28%)|
|JetBlue (35%)|United|Northwest(28%)|
|NorthWest (35%)|PSA|PSA (30%)|
|Continental (35%)|Continental|US (30%)|
|ExpressJet (36%)|Envoy|Frontier (30%)|
|Envoy (36%)|SkyWest|JetBlue (32%)|
|Alaska(38%)|Mesa|Southwest (32%)|
|Frontier (39%)|ExpressJet(1) |Mesa (45%)|
|PSA (41%)|JetBlue|Hawaiian (55%)|

Days of the Week ranking (best to worst):

|Per relative average of delays|Per duration of the delay|
|---|---|
|Thursday|Thursday|
|Tuesday|Tuesday|
|Sunday|Wednesday|
|Friday|Monday|
|Wednesday|Sunday|
|Monday|Saturday|
|Saturday|Friday|

Delays are more frequent and longer during the Holidays, from Dec-17 through Dec-27.


## Key Insights for Presentation

For the presentation, the main focus was causes and airlines of delayed flights.

The first plots show the proportion of on-time vs delayed flights, as at the same the proportion of medium and large delays over the delayed flights set, through pie-charts.

Then started by introducing how the different causes of delays contributed to arrival delays per their average time of delay, plotting the proportions of time also on a pie-chart.

Since the number of flight operations is varied for the airlines, counted the relative frequency of delay causes by airline through stacked bars on a barplot.

Besides the frequency, calculated the weight of the impact of the delay causes on arrival delays, by box-plotting the arrival delays on a logarithmic scale since the arrival delay distribution has a long tail right-skewed shape.

Now got the ranking of delay causes from different aspects of the data. The similar approach is taken to rank the airlines.

The frequency of delayed flights per airline were plot on horizontal bars on top of the total flights, for comparing proportions.

The arrival delay per airline were shown using boxplots.

Finally, by reusing the Frequency of Delay Causes per Airline stacked bars, measured the performance of each carrier by taking only the delays caused by carrier, since it is the only cause within the airline's control.
    
