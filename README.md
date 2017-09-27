
## GTFS-STAT

A GTFS-based data transit network data standard suitable for dynamic transit modeling.

**version**: 0.1.0  
**updated**: 26 September 2017  
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
[`stop_time_stats.txt`](/files/stop_times_stats.md)	| Stop time statistics
[`trip_stats.txt`](/files/trip_stats.md)			| Trip statistics
