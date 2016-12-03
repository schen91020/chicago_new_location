---
title:  "Data Exploration"
date:   2016-12-01 15:15:23
---
The type of business can make a difference in terms of taking advantage of the given data. In this analysis, I am assuming that it's a bakery that needs a lot of in-store traffic.

Among the brick and mortar retail businesses, there is much of a difference on how each can take advantage of the given data. For instance, a bakery can plan its menu according to whether it's a weekday (more breakfast items) or weekend (more high-tea items). But a clothing store probably will not change its inventory accordingly. The additional data that we seek can also be different. A bakery might wonder about the demographic of commuters whereas an Apple store might not care as much.

Given the assumption of a bakery trying to expand into new locations, I proceed to explore the given data.

The data is a compilation of time series of number of rides per station. There are 147 stations total. Let's take a quick look at stations and their respected number of rides.

![all_rides](/chicago_new_location/DataAnalysis/Images/all_rides.png){:class="img-responsive"}

It will certainly help if we can start a bakery near stations with the highest number of rides. However, we should not take the barcharts at face value. Let's take a quick look at the box plots.

![box_rides](/chicago_new_location/DataAnalysis/Images/box_all_rides.png){:class="img-responsive"}

As we explore the data further, it's beneficial to keep in mind that the stations with the highest rides can be due to outliers. If the new location needs steady foot traffic, seeking highest mean and lowest standard deviation in rides might help. For now, we move on.

These are the time series plot of the top 5 stations.

![max_rides](/chicago_new_location/DataAnalysis/Images/max_rides.png){:class="img-responsive"}

Let's take a moving average on the data to see if there is seasonality in it's rides. To start a new location, inventory can be adjusted due to seasonality.

![max_rides_ma](/chicago_new_location/DataAnalysis/Images/max_rides_ma.png){:class="img-responsive"}

There is a definite seasonality to the data. I wonder if it's weather related? Or is it because people are out of town for Christmas? For now, I will make a note of it and explore that further in the next section.

For a business, we should focus on opening locations with high foot traffic. But for completeness, let's take a look at the stations with the lowest number of rides.

![min_rides](/chicago_new_location/DataAnalysis/Images/min_rides.png){:class="img-responsive"}

This graph looks very different. It seems some of those stations didn't get any rides until a later time -- end of 2011. The station with lowest number of rides is Homan.

![homan_rides](/chicago_new_location/DataAnalysis/Images/homan_rides.png){:class="img-responsive"}

Initially, I thought stations with a low number of rides because of proximity to downtown. But from the graph it looks like Homan is a brand new station! This is good news, perhaps the new location can take advantage of the possible lower rent near a new station.

Let's take a look at the next station: Cermak-McCormick Place. Interestingly enough, it looks like another new station (started in 2015).

![cmp_rides](/chicago_new_location/DataAnalysis/Images/cmp_rides.png){:class="img-responsive"}

How about one more? Oakton-Skokie station is the next station with the lowest number of rides.

![os_rides](/chicago_new_location/DataAnalysis/Images/os_rides.png){:class="img-responsive"}

The station didn't get any rides until 2012. But its number of rides dropped to 0 during the second half of 2015. I wonder why this is the case. Could it be because other stations opened up and it took a hit? Or is the machine that reads the rides is broken? This begs the question of data integrity. Are the stations with the low rides really new or is it just because their machines are newly installed? If it's the latter case, the new business might not take advantage of a newly developed area in terms of rent, then it has to go with the established areas with highest number of foot traffic.

In the data, there is also a column called daytypes. City of Chicago gave some answers. There are 3 datatypes: "W" for Weekday, "A" for Saturday and "U" for Sunday/Holidays. Plotting daytypes vs. number of rides, we see:

![bar_daytype](/chicago_new_location/DataAnalysis/Images/daytype_rides.png){:class="img-responsive"}

Weekdays seem to a lot more rides. Verifying the finding with box-whisker charts:
![box_daytype](/chicago_new_location/DataAnalysis/Images/box_daytype_rides.png){:class="img-responsive"}

On average, the weekdays still have more rides but not as drastic of a difference as what a barchart shows. However, notice that Sunday/Holidays have a lot of outliers. If we were to start a new location based on the rides per station, the next step will be to explore the daytype per station. Maybe some stations will have some interesting behavior over the holidays. Here is a first look at this information. This visualization is helpful. However, I would prefer to see a change of ranking per daytype per station with lines connecting from one daytype column to another. I will discuss this idea further in the next section.

![box_daytype](/chicago_new_location/DataAnalysis/Images/stacked_daytype_rides.png){:class="img-responsive"}
