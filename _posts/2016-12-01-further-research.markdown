---
title:  "Further Research"
date:   2016-12-01 15:04:23
---
From the initial exploration, we found the station with highest number of rides is Clark/Lake. The station with lowest number of rides is Homan.

Locating these two stations on a map will be helpful.

![stations_max_min](/chicago_new_location/DataAnalysis/Images/stations_max_min.png){:class="img-responsive"}

Seeing the locations of these two stations, it explains the number of rides. It will be great to combine the number of rides per station and locate them on a map. A very rough idea looks like this:

![map_barcharts](/chicago_new_location/DataAnalysis/Images/map_barcharts.jpeg){:class="img-responsive"}

We have witnessed the seasonality in rides. To see if it's weather related, I can get the historical data  and compare. The weather data will look like:

![historical_weather](/chicago_new_location/DataAnalysis/Images/historical_temp_chicago.png){:class="img-responsive"}

The coldest months are December. Does that coincide with the lowest number of rides?

![max_rides_ma](/chicago_new_location/DataAnalysis/Images/max_rides_ma.png){:class="img-responsive"}

Zooming in, the trough does seem to coincide with the lowest temperature in Chicago.

![cl_head_ma](/chicago_new_location/DataAnalysis/Images/cl_head_ma.png){:class="img-responsive"}

However, what about the folks who travel? Perhaps, they simply left town. We can look at airline data. For now, I will only include a link:

[air_traffic](http://www.flychicago.com/OHare/EN/AboutUs/Facts/Air-Traffic-Data.aspx)

In the data exploration, we have mentioned if a new location is looking for steady foot traffic, perhaps looking for a station with the highest mean and lowest standard deviation might help. First look at the mean vs stdev chart grouped by stations:

![mean_std_rides](/chicago_new_location/DataAnalysis/Images/mean_std_rides.png){:class="img-responsive"}

But just like in many other fields of study, there is no free lunch. As the number of rides increase, we are also witnessing an increase in standard deviation. Therefore, applying some optimization algorithm will help in identifying a few stations here.

If a bakery is to open a new location, demographic information will certainly help. One, the income level helps to determine the price point. Sell a slice of cake for $6.99 will not work in a low income area. There is a very good resource at [data_usa](https://datausa.io/profile/geo/chicago-il/) that will help in finding out more about the type of potential customers. The data that can be explored will be:

![income_map](/chicago_new_location/DataAnalysis/Images/data_usa_income.png){:class="img-responsive"}

Age, heritage and language will all need to be considered. Having time-stamp on the commuters data will also help the new location to anticipate the traffic.
Combining that with the station information, we will have a much better idea of where to start a new location. In particular, if near a busy station, during a certain time of the day, there are many kids, the bakery can prepare items that will be suitable.

Also note that the daytype provided is only for workday vs. Saturday and holidays. We can also explore if there are variations among different days.

We can also explore proximity to office buildings around each potential new location. Assuming we are going to start the new location near a busy station. What about the nearby shops and competitions? I have included a google map here. Using an API will be something we consider in the future.

![bakery_map](/chicago_new_location/DataAnalysis/Images/google_bakeries.png){:class="img-responsive"}
