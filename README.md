
## GTFS-STAT

A GTFS-based data transit network data standard suitable for dynamic transit modeling.

**version**: 0.1.2  
**updated**: 12 April 2018  
**created**: 26 September 2017  
**authors**:

 * Elizabeth Sall (UrbanLabs LLC)  
 * Drew Cooper (San Francisco County Transportation Authority)  
 
[issues]: https://github.com/osplanning-data-standards/GTFS-STAT/issues
[repo]: https://github.com/osplanning-data-standards/GTFS-STAT
[GTFS]: https://developers.google.com/transit/gtfs/reference


NOTE: This is a draft specification and still under development. If you have comments
or suggestions please file them in the [issue tracker][issues]. If you have
explicit changes please fork the [git repo][repo] and submit a pull request.

### Changelog

-  `0.1.2`: Removed `stop_stats.txt` in favor of making [`stop_time_stats.txt`](/files/stop_time_stats.md) a statistical summary file instead of list-like.  Similarly, made [`trip_stats.txt`](/files/trip_stats.md) a statistical summary file instead of list-like.  Finally, aligned statistical fields between [`trip_stats.txt`](/files/trip_stats.md), [`route_stats.txt`](/files/route_stats.md), and [`group_stats.txt`](/files/group_stats.md)
-  `0.1.1`: Add new file [`stop_stats.txt`](/files/stop_stats.md) for aggregation statistics at stop level. Update trip_stats.txt and stop_time_stats.txt to remove time windows, since these are containers for raw data rather than aggregations. Fix value types of aggregation fields from int->float. Clarify required vs optional for aggregation definition fields.
-  `0.1.0`: initial commit

# Specification

GTFS-STAT is an extension to a GTFS transit network with additional files that contain 
performance data.  

A GTFS-STAT transit network MAY include the following files:

Filename 					| Description										
----------					| -------------		
[`groups.txt`](/files/groups.md)					| Group definitions
[`group_stats.txt`](/files/group_stats.md)			| Group statistics
[`route_stats.txt`](/files/route_stats.md)			| Route statistics
[`stop_time_stats.txt`](/files/stop_time_stats.md)	| Stop time statistics
[`trip_stats.txt`](/files/trip_stats.md)			| Trip statistics
