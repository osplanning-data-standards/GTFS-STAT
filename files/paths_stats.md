## Path Performance Information
### A path is a collection of routes that serve a common corridor or origin-destination pair

 *  Filename MUST be `paths.txt`
 *  File MUST contain a record for every transit route and in a path
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.

File MUST contain ONE of the following TWO sets of required attributes:

**Option One**:
Required Attributes	| Description										
----------			| -------------		
`path_id`			| ID that uniquely identifies a path.
`start_date`		| Start date in YYYYMMDD for which route statistics are calculated.
`end_date`			| End date in YYYYMMDD for which route statistics are calculated.
`start_time`		| Start time in HH:MM:SS for which route statistics are calculated.
`end_time`			| End time in HH:MM:SS for which route statistics are calculated.
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
`path_id`			| ID that uniquely identifies a path.
`service_id`		| ID that uniquely identifies a service span in `calendar.txt`.
`start_time`		| Start time in HH:MM:SS for which route statistics are calculated.
`end_time`			| End time in HH:MM:SS for which route statistics are calculated.

File MAY contain the following attributes:

Optional Attributes					| Description										
----------							| -------------		
`path_avg_scheduled_runtime`		| Integer, average number of minutes from scheduled `arrival_time` at first stop to scheduled `departure_time` at last stop for all route-segments in the path.
`path_avg_observed_runtime`			| Integer, average number of minutes from observed `arrival_time` at first stop to observed `departure_time` at last stop.
`path_stdev_scheduled_runtime`		| Float, standard deviation of scheduled runtime for all route-segments in the path
`path_stdev_observed_runtime`		| Float, standard deviation of observed runtime for all route-segments in the path.
`path_semi_stdev_observed_runtime`	| Float, semi-standard deviation between scheduled and observed run time for all routes in the path.
`path_avg_scheduled_stopped_time`	| Integer, average number of minutes scheduled time spent at all stops in a trip, for all route-segments in the path, from pull-in time to pull-out time.
`path_avg_observed_stopped_time`	| Integer, average number of minutes observed time spent at all stops in a trip, for all route-segments in the path, from pull-in time to pull-out time.
`path_avg_stopped_delay`			| Integer, difference between `path_avg_observed_stopped_time` and `path_avg_scheduled_stopped_time`.
`path_avg_scheduled_moving_time`	| Integer, average number of minutes scheduled moving time (difference between `path_avg_scheduled_runtime` and `path_avg_scheduled_stopped_time`.
`path_avg_observed_moving_time`		| Integer, average number of minutes observed moving time (difference between `path_avg_observed_runtime` and `path_avg_observed_stopped_time`.
`path_avg_moving_delay`				| Integer, difference between `path_avg_observed_moving_time` and `path_avg_scheduled_moving_time`.