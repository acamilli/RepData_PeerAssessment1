---
title: "Project Assessment 1 - Reproducible Research"
author: "Alberto Camilli"
date: "Saturday, March 14, 2015"
output: html_document
---

Loading and preprocessing the data.

First I´m going to read the data then I´ll eliminate the rows with NAs and generate a df with no NA (dfNOna)


Now I´m going calculate average values over the remaining data.First I need to kwow the #days and the #steps per day. Results will be stored in a table (tabela1) so it can be retrieved whenever wanted. The total #steps per day will be plotted. Mean and median are subsequently calculated.

What is mean total number of steps taken per day?
Mean and median for the expurged data frame:
What is the average daily activity pattern?

Now I want to know the averages over each 5 minute interval. I´ll build up a second table, tabela2  and then plot the #steps per 5 minute interval


It can be seen that the maximum number of steps per interval is:

which occours at the interval:
Imputing missing values

Now I´m going to replace the excluded NAs with values that will be estimated as the average #steps for the existing data. 
First I´ll calculate the number of NA rows in the original data frame:

Then I´ll calculate the average over valid values in media_geral and use it as a criteria for fill in NA values.So a new data.frame (dfFull) will be constructed from the original one (df) and the same steps taken before will be repeated.

Mean and median for the stuffed data frame:

Are there differences in activity patterns between weekdays and weekends?

Now I´m going to compare weekdays to weekend behaviours.
A factor variable (period, with 2 levels, weekday and weekend) will be added to the full data frame

Now I join vertically the two tables into a new data.frame (dfm), rename columns, delete row names and plot a panel



