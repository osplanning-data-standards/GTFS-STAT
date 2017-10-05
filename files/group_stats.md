## Group Performance Information
### A group is a collection of routes that serve a common corridor or origin-destination pair

 *  Filename MUST be `group_stats.txt`
 *  File MUST contain a record for every transit route and in a group
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.

File MUST contain the following required attributes:

Required Attributes	| Description										
----------			| -------------		
`group_id`			| ID that uniquely identifies a group.
`start_time`		| Start time in HH:MM:SS for which route statistics are calculated.
`end_time`			| End time in HH:MM:SS for which route statistics are calculated.

File MUST contain ONE of the following TWO sets of required attributes:

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

Optional Attributes					| Description										
----------							| -------------		
`group_avg_scheduled_runtime`		| Float, average number of minutes from scheduled `arrival_time` at first stop to scheduled `departure_time` at last stop for all route-segments in the group.
`group_avg_observed_runtime`			| Float, average number of minutes from observed `arrival_time` at first stop to observed `departure_time` at last stop.
`group_stdev_scheduled_runtime`		| Float, standard deviation of scheduled runtime for all route-segments in the group
`group_stdev_observed_runtime`		| Float, standard deviation of observed runtime for all route-segments in the group.
`group_semi_stdev_observed_runtime`	| Float, semi-standard deviation between scheduled and observed run time for all routes in the group.
`group_avg_scheduled_stopped_time`	| Float, average number of minutes scheduled time spent at all stops in a trip, for all route-segments in the group, from pull-in time to pull-out time.
`group_avg_observed_stopped_time`	| Float, average number of minutes observed time spent at all stops in a trip, for all route-segments in the group, from pull-in time to pull-out time.
`group_avg_stopped_delay`			| Float, difference between `group_avg_observed_stopped_time` and `group_avg_scheduled_stopped_time`.
`group_avg_scheduled_moving_time`	| Float, average number of minutes scheduled moving time (difference between `group_avg_scheduled_runtime` and `group_avg_scheduled_stopped_time`.
`group_avg_observed_moving_time`		| Float, average number of minutes observed moving time (difference between `group_avg_observed_runtime` and `group_avg_observed_stopped_time`.
`group_avg_moving_delay`				| Float, difference between `group_avg_observed_moving_time` and `group_avg_scheduled_moving_time`.
