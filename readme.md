# Bay Wheels's trip data Exploration analysis
## by Amal Meer


## Dataset
[Link to the dataset](https://www.kaggle.com/franckjay/ford-gobike-data)

> This dataset contains information about Bay Wheels's trip during 2017.
There're more than 500000 records. Each record represents the trip information (including time, station, bike, user info.)
The data is complete and has no null values. Most of the features are numeric (duration, latitude, longitude, ...,).
The name and id attributes are nominal.

The data types of some features has been changed.

* start_time, end_time to timestamp
* user_type to categorical type
* start_station_id, end_station_id, bike_id to string object

The station_name,station_latitude, and station_longitude for the start and end point need to be seperated on another table. i.e. we shold have a table for the trip information (duration_sec, start_time, end_time, start_station_id, end_station_id, bike_id, user_type) and another table for the station information (station_name, station_latitude, station_longitude), but since this won't effect our analysis, I keep it as it it for simplicity.

I've added 2 column, day_week and start_hour. It repeat an information that could be extracted from the start_time, but using such an info make the visualization dramatically easier. It can be dropped later but I'll leave it.

## Summary of Findings

> * there're some stations that have more trips than another stations, getting the most, say 5, stations that has more trips will help the company to take care of these stations more.

* subscriber has more number of trips, around 4 times more than the casual customer.

* The number of trips has a notable drop on the weekends. This might be an indication that most people use bikes to get to their work

* The distribution of the trips count on hour of days is bimodal. There're 2 intervals where the number of trips has a notable increased. These intervals are around 8 AM, and 5 PM. These hours are the start and end time of the work day. This emphasize the fact that most people use bikes to get to their work.

* Most of the trips fall below 9000 seconds. i.e. 2.5 hours.

* The number of trips by subscriber are more than those taken by casual customers in general. Also, the number of trips by subscriber decreased on the weekend, while the number of the casual customers increased on the weekends. This might indicates that subscriber pay for membership as they use the bike all the week days to get to their work, while casual users use anothr mean of transport to get to their work, and use bikes for other usage.

* The usual customer has a higher duration median and higher IQR than subscriber. This was opposite to mt expectations.

* The weekends have different trend than the work days. On weekends, more bikes are used between 10AM to 5PM, less are used on the start and end of the day, while the work days behave the opposite, most bikes are used in the start and end of the work day (8 AM, 5PM).

* The subscribers use the bikes early on weekdays, and late on weekend, while the customer behave the opposite. In general, subscriber usually start much earlier. This emphasize that subscriber use the bikes to get to their work.


## Key Insights for Presentation

> For the presentation, I focus on the 3 features that influence the trip count that I found effective and might help busniess owners to take decisions. I take the count trip as dependent variable rather than the duration.

These features are: user_type, week_day, start_hour

The key insights are:

* subscriber has more number of trips, around 4 times more than the casual customer. subscriber must be given more attention as they are a core for this busniess. The bar chart below show this difference.

* The number of trips by subscriber are more than those taken by casual customers in general. Also, the number of trips by subscriber decreased on the weekend, while the number of the casual customers increased on the weekends. This might indicates that subscriber pay for membership as they use the bike all the week days to get to their work, while casual users use anothr mean of transport to get to their work, and use bikes for other usage.

* The weekends have different trend than the work days. On weekends, more bikes are used between 10AM to 5PM, less are used on the start and end of the day, while the work days behave the opposite, most bikes are used in the start and end of the work day (8 AM, 5PM)

* The subscribers use the bikes early on weekdays, and late on weekend, while the customer behave the opposite. In general, subscriber usually start much earlier. This emphasize that subscriber use the bikes to get to their work.
