# Data-Exploration-and-Analytics
**NYC Flights Data Exploration and Analytics**

All analyses in this project performed in R using the tidyverse package.

In this project I analyzed the flights data frame, which has information on 19 features for 336,776 flights that left New York City during the year 2013. The purpose of this project is to become more familiar with data transformations and
exploratory data analysis, assists me to think of solutions to questions. I obtained the
flights data frame by installing and loading the nycflights13 library in R studio.

***Objective-1 : I found median distance between airports for canceled flights shorter, longer, or roughly the same as for non-canceled flights using box plots with appropriate notches.***

Explanation: The boxplot is split into two groups based on whether the
flight was cancelled or not. The y-axis represents the distance between airports, and the x-axis
represents whether the flight was cancelled. The boxplot shows the distance distribution
between airports for each group, with the notches representing a confidence interval around
the median value. The red points represent the median distance for each group and the blue
points represent the mean distance for each group.
Comparing the two groups shows that the median distance between airports is slightly higher
for cancelled flights compared to non-cancelled flights. The mean distance between airports is
also higher for cancelled flights compared to non-cancelled flights.
However, it's important to note that this analysis only considers the relationship between
distance between airports and cancelled/non-cancelled flights

***Objective-2 : Analyzed whether the canceled flights tend to occur more often in certain months? That is, compared to
other months, are there certain months with a large proportion of their flights canceled***

Explanation: I analyzed this by generating bar plot with month of year on the x-axis and proportion of that month’s flights that are canceled on the y-axis. 

The data is first grouped by month and the proportion
of cancelled flights is calculated for each group. The resulting data is then plotted using
ggplot2, with the x-axis representing the months and the y-axis representing the
proportion of cancelled flights. Each bar in the plot represents a month, and the color of
the bar corresponds to the month. The plot also includes a title and labels for the x and
y-axis.
I use the guides function to remove the legend that would appear by default. Through
this analysis I found that the proportion rate is high for flights cancelled in the month
February(2). On the other hand very minimal rate of flights got cancelled in the October
month.

***Objective-3 : Found the relationship between average distance between airports for flights flown on
each of the 365 days of the year and the standard deviation of the distances between airports
for flights flown on each of those days.***

Explanation: This behaviour is found using Scatter plot. First, I start this by filtering out the cancelled flights
from the original flight's dataset, and selecting only the necessary variables (month, day, and
distance) for the analysis. Then, it calculates the average and standard deviation of distance for
each day. The resulting daily_distance dataset is used to create a scatter plot of mean distance
vs standard deviation of distance. The geom_smooth() function is used to fit a linear regression
line to the scatter plot, with confidence intervals.
From this plot, we can see that there is a positive linear relationship between the mean and
standard deviation of daily flight distances. As the mean distance increases, so does the standard
deviation. This makes intuitive sense, as longer flights are likely to have more variability in the
distance due to factors such as weather, air traffic, and flight routing.

