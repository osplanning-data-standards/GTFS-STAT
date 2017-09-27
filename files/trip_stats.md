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
`scheduled_runtime`		| Float, number of minutes from scheduled `arrival_time` at first stop to scheduled `departure_time` at last stop.
`observed_runtime`		| Float, number of minutes from actual `arrival_time` at first stop to actual `departure_time` at last stop.
`scheduled_stopped_time`| Float, number of minutes scheduled stop time.
`observed_stopped_time`	| Float, number of minutes actual stop time.
`stopped_delay`			| Float, number of minutes of stop delay.
`scheduled_moving_time`	| Float, number of minutes scheduled moving time.
`observed_moving_time`	| Float, number of minutes actual moving time.
`moving_delay`			| Float, number of minutes of moving delay.
