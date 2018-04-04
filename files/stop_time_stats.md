## Stop Time Performance Information

 *  Filename MUST be `stop_times_stats.txt`
 *  File MUST contain a record for every scheduled stop within a trip and route (i.e. the time when the Muni 14 Local Outbound that left at 8:02 gets to 24th St. and Mission St)
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain the following required attributes:

Required Attributes	| Description										
----------			| -------------		
`trip_id`			| ID that uniquely identifies a vehicle trip
`stop_id`			| ID that uniquely identifies a stop

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

Optional Attributes		| Description										
----------				| -------------		
`scheduled_arrival_time`	| Scheduled arrival time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`scheduled_departure_time`	| Scheduled departure time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`avg_arrival_time`	| Average observed arrival time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`stdev_arrival_time`	| Standard deviation of observed arrival time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`semi_stdev_arrival_time`	| Float, semi-standard deviation between observed and scheduled arrival time.
`avg_arrival_time_diff`	| Float.  Average difference between observed and scheduled arrival time.
`avg_departure_time`	| Average observed departure time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`stdev_departure_time`	| Standard deviation of observed departure time at a specific stop for a specific trip on a route in HH:MM:SS format measured from midnight.  For trips that span multiple dates, the time should be entered as a value greater than 2400000
`semi_stdev_departure_time`	| Float, semi-standard deviation between observed and scheduled departure time.
`avg_departure_time_diff`	| Float.  Average difference between observed and scheduled departure time.
`pct_arrival_late_00_01` | Float. Percent of arrivals between on-time and 1 minute late.
`pct_arrival_late_01_05` | Float. Percent of arrivals between 1 minute and 5 mintues late.
`pct_arrival_late_05_10` | Float. Percent of arrivals between 5 minutes and 10 minutes late.
`pct_arrival_late_10_15` | Float. Percent of arrivals between 10 minutes and 15 minutes late.
`pct_arrival_late_15+` 	| Float. Percent of arrivals more than 15 minutes late.
`pct_departure_late_00_01` | Float. Percent of departures between on-time and 1 minute late.
`pct_departure_late_01_05` | Float. Percent of departures between 1 minute and 5 mintues late.
`pct_departure_late_05_10` | Float. Percent of departures between 5 minutes and 10 minutes late.
`pct_departure_late_10_15` | Float. Percent of departures between 10 minutes and 15 minutes late.
`pct_departure_late_15+` | Float. Percent of departures more than 15 minutes late.
`avg_arrival_remaining_seated_cap` | Float. Average amount of remaining seated capacity.
`avg_arrival_remaining_standing_cap` | Float. Average amount of remaining standing capacity.
`avg_arrival_remaining_cap` | Float. Average amount of remaining seated+standing capacity. 
`pct_unboardable_arrivals` | Float. Percent of arrivals with no remaining capacity.
`pct_boardable_arrivals_00_15` | Float. Percent of arrivals with remaining capacity between 0% (strictly greater than) and 15% 
`pct_boardable_arrivals_15+` | Float. Percent of arrivals with 15% or more remaining capacity.
