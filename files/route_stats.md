## Transit Route Performance Information

 *  Filename MUST be `routes_stats.txt`
 *  File MUST contain a record for every transit route (i.e. the Muni 14 Local) 
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.

File MUST contain the following required attributes:

Required Attributes	| Description										
----------			| -------------		
`route_id`			| ID that uniquely identifies a route.
`start_time`		| Start time in HH:MM:SS for which route statistics are calculated.
`end_time`			| End time in HH:MM:SS for which route statistics are calculated.

AND, ONE of the following TWO sets of required attributes:

**Option One**:

Required Attributes	| Description										
----------			| -------------		
`start_date`		| Start date in YYYYMMDD for which route statistics are calculated.
`end_date`			| End date in YYYYMMDD for which route statistics are calculated.
`monday`			| 0 or 1. A binary value indicating whether route statistics include Mondays.
`tuesday`			| 0 or 1. A binary value indicating whether route statistics include Tuesdays.
`wednesday`			| 0 or 1. A binary value indicating whether route statistics include Wednesdays.
`thursday`			| 0 or 1. A binary value indicating whether route statistics include Thursdays.
`friday`			| 0 or 1. A binary value indicating whether route statistics include Fridays.
`saturday`			| 0 or 1. A binary value indicating whether route statistics include Saturdays.
`sunday`			| 0 or 1. A binary value indicating whether route statistics include Sundays.

**Option Two**:

Required Attributes	| Description										
----------			| -------------		
`service_id`		| ID that uniquely identifies a service span in `calendar.txt`.

File MAY contain the following attributes:

Optional Attributes				| Description										
----------						| -------------		
`direction_id`					| ID that contains a binary value that indicates the direction of the trip.  This should be included and match `direction_id` values in trips.txt if `direction_id` is included in trips.txt
`avg_runtime_scheduled`		| Float, number of minutes from scheduled `arrival_time` at first stop to scheduled `departure_time` at last stop.
`stdev_runtime_scheduled`		| Float, standard deviation of scheduled runtime for all route-segments in the group.
`avg_stopped_time_scheduled`| Float, number of minutes scheduled stop time.
`stdev_moving_time_scheduled`	| Float, standard deviation of number of minutes scheduled moving time.
`avg_moving_time_scheduled`	| Float, number of minutes scheduled moving time.
`stdev_stopped_time_scheduled`	| Float, standard deviation of number of minutes scheduled time spent at all stops in a trip, for all route-segments in the group, from pull-in time to pull-out time.
`avg_runtime`		| Float, average number of minutes from observed `arrival_time` at first stop to observed `departure_time` at last stop.
`stdev_runtime`		| Float, standard deviation of number of minutes from observed `arrival_time` at first stop to observed `departure_time` at last stop.
`semi_stdev_runtime`		| Float, semi-standard deviation number of minutes from observed `arrival_time` at first stop to observed `departure_time` at last stop.
`avg_stopped_time`	| Float, average number of minutes observed stop time.
`stdev_stopped_time`	| Float, standard deviation number of minutes observed stop time.
`semi_stdev_stopped_time`	| Float, semi-standard deviation average number of minutes observed stop time.
`avg_moving_time`	| Float, average number of minutes observed moving time.
`stdev_moving_time`	| Float, standard deviation number of minutes observed moving time.
`semi_stdev_moving_time`	| Float, standard deviation number of minutes observed moving time.
`pct_late_start_00_01` | Float. Percent of trips that start between on-time and 1 minute late.
`pct_late_start_01_05` | Float. Percent of trips that start between 1 minute and 5 mintues late.
`pct_late_start_05_10` | Float. Percent of trips that start between 5 minutes and 10 minutes late.
`pct_late_start_10_15` | Float. Percent of trips that start between 10 minutes and 15 minutes late.
`pct_late_start_15+` 	| Float. Percent of trips that start more than 15 minutes late.
