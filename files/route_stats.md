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
`avg_scheduled_runtime`			| Float, average number of minutes from scheduled `arrival_time` at first stop to scheduled `departure_time` at last stop.
`avg_observed_runtime`			| Float, average number of minutes from observed `arrival_time` at first stop to observed `departure_time` at last stop.
`stdev_scheduled_runtime`		| Float, standard deviation 
`stdev_observed_runtime`		| Float, standard deviation of `actual_time`.
`semi_stdev_observed_runtime`	| Float, semi-standard deviation between scheduled and observed route run time.
`avg_scheduled_stopped_time`	| Float, average number of minutes scheduled time spent at all stops in a trip, from pull-in time to pull-out time.
`avg_observed_stopped_time`		| Float, average number of minutes observed time spent at all stops in a trip, from pull-in time to pull-out time.
`avg_stopped_delay`				| Float, difference between `avg_observed_stopped_time` and `avg_scheduled_stopped_time`.
`avg_scheduled_moving_time`		| Float, average number of minutes scheduled moving time (difference between `avg_scheduled_runtime` and `avg_scheduled_stopped_time`.
`avg_observed_moving_time`		| Float, average number of minutes observed moving time (difference between `avg_observed_runtime` and `avg_observed_stopped_time`.
`avg_moving_delay`				| Float, difference between `avg_observed_moving_time` and `avg_scheduled_moving_time`.
