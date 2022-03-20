# SurfsUp_Challenge.ipynb

## Overview

Using an SQLlite database, SQLalchemy was used to connect to, and extract data from the database. After the data was extracted from the database using a query in python, it was placed into a dataframe for further analysis separate from the database. 

## Results

The analysis compared between the temperatures in Hawaii in the months of June and December. 
 - The mean temperature in June was 74.9 degrees compared to the mean temperature of 71.0 degrees in December.
 - The lower quartile range was 73 degrees in June and 69 degrees in December.
 - The upper quartile range was 77 degrees in June and 74 degrees in December.

## Summary

When comparing the temperatures between the months of June and December, the descriptive statistics show that there really wasn't much of a temperature change between the "winter" and the "summer". The mean temperature in June is only 4 degrees warmer than the mean in December and the upper and lower quartile ranges differ by a few degrees as well. 

 - In order to get a more accurate assessment of the difference in seasons, the query `session.query(Measurement.date, Measurement.prcp).filter(extract('month',Measurement.date)==6).all()` could be written to find the precipitation rates for June and December. 
 - Queries could be written to see the difference in temperatures from the stations with the highest elevations as the lowest to get a more three dimensional window to describe the difference in seasons 
