## Stop Time Performance Information

 *  Filename MUST be `stop_times_stats.txt`
 *  File MUST contain a record for every scheduled stop within a trip and route (i.e. the time when the Muni 14 Local Outbound that left at 8:02 gets to 24th St. and Mission St)
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain ONE the following TWO sets of required attributes:

**Option One**:
Required Attributes	| Description										
----------			| -------------		
`trip_id`			| ID that uniquely identifies a vehicle trip
`stop_id`			| ID that uniquely identifies a stop
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
`trip_id`			| ID that uniquely identifies a vehicle trip
`stop_id`			| ID that uniquely identifies a stop
`service_id`		| ID that uniquely identifies a service span in `calendar.txt`.
`start_time`		| Start time in HH:MM:SS for which route statistics are calculated.
`end_time`			| End time in HH:MM:SS for which route statistics are calculated.

File MAY contain the following attributes:

Optional Attributes		| Description										
----------				| -------------		
`scheduled_arrival_time`	| Scheduled arrival time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`scheduled_departure_time`	| Scheduled departure time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`observed_arrival_time`	| Actual arrival time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`observed_departure_time`	| Actual departure time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
