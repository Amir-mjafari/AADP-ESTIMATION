# AADP-ESTIMATION

* **PLEASE READ FOLLOWING INFORMATION TO UNDRESTAND THE OBJECTIVES AND TECHNIQUES USED IN THIS PROJECTS.**
* **WE ARE NOT ALLOWED TO SHARE THE DATA OF THIS PROJECT**

## PROJECT SUMMARY
We introduced ML methods based on site characteristics (e.g., nearby land use), weather conditions, date, and short-term counts (STC) to estimate Daily Pedestrian Traffic. The data was available for 94 stations (intersections) in Arizona, US, with an average of 223 continuous counting days at each intersection for passing pedestrians. A Neural Network Model trained by Keras library had an R-squared of 0.82, more explanatory than the Linear Regression Model with an R-squared of 0.71.

## PROJECT DESCRIPTIONS
Annual average daily pedestrians (AADP) are the average daily measure of pedestrians'
total volume on a walkway segment over a year. AADP is one of the critical attributes that
explain the collision rate. Although collecting pedestrian count data every day in a year
is the most accurate method of calculating AADP, it is not economically feasible for each
segment. Only some selected walkway locations have permanent count stations. However,
for others, short term counts (i.e., counts on just one or a couple of days) are available for
AADP estimating process.
The aim is to develop an ML method to estimate the AADP based on the short term
count volume(s). We expect that the AADP at a location is a function of site character-
istics(e.g., nearby land use), day of the week, day of the month, the month of the year,
weather conditions, and also short term count volume(s).
There are 94 available stations in Arizona, US which continuous counting is available
for them by a third party. We have 223 available continuous counting days on average for
each intersection.
For each station or intersection, we obtained Land Use characteristics from Google Maps
within the radius of 1=4 mile.
Land use characteristics are number of bus stations,schools,universities,libraries,conveniencestores,hospitals,clinics,shops,restaurants and bars nearby.
Short term counts (STC's) are sampled randomly among all available STC days for
each intersection. For the purpose of this project, we chose one random STC day for each
intersection. STC days are selected with some constraints (e.g., no weekend or holiday,
no inclement weather, etc.) to keep the STC days variance small in order to mitigate the
variance of the predictions.
Weather conditions also aect pedestrian volumes. Weather condition data is obtained
from a weather station located at TUCSON INTERNATIONAL AIRPORT, AZ US. We
are using the amount of perception and snow as two of the features in our model.
For the dates related feature, we use ONE-HOT vectors for the day of month and month
of the year. For the day of the week, we use binary categories, 0 for weekdays and 1 for
weekends.
The total data points are 21293, the number of data available before the COVID pan-
demic is 5901.
