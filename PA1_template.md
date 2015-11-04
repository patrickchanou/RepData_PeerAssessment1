##Reproducible Research: Peer Assessment 1

##Loading and preprocessing the data

if(!file.exists('activity.csv')){
    unzip('activity.zip')
}
activityData <- read.csv('activity.csv')
names(activity)
# [1] "steps"    "date"     "interval"
library(lattice)
activity$date <- as.Date(activity$date, "%Y-%m-%d")

##What is mean total number of steps taken per day?
I will use to approaches 

First is using aggregate function

StepsTotal <- aggregate(steps ~ date, data = activity, sum, na.rm = TRUE)




