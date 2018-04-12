## Additional Transit Vehicle Trip Performance Information

 *  Filename MUST be `trips_stats.txt`
 *  File MUST contain a record for every transit vehicle trip (i.e. the Muni 14 Local Outbound that leaves at 8:02 AM) 
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain the following required attributes:

Required Attributes	| Description										
----------			| -------------		
`trip_id`			| ID that uniquely identifies a vehicle trip

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

Optional Attributes	| Description										
----------			| -------------		
`scheduled_start_time` | String, HH:MM:SS, the `arrival_time` at the first scheduled stop
`scheduled_runtime`		| Float, number of minutes from scheduled `arrival_time` at first stop to scheduled `departure_time` at last stop.
`scheduled_stopped_time`| Float, number of minutes scheduled stop time.
`scheduled_moving_time`	| Float, number of minutes scheduled moving time.
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
