## Path Definition Information
### A path is a collection of routes that serve a common corridor or origin-destination pair

 *  Filename MUST be `paths.txt`
 *  File MUST contain a record for every transit route and in a path
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.

File MUST contain the following required attributes:

**Option One**:
Required Attributes	| Description										
----------			| -------------		
`path_id`			| ID that uniquely identifies a path.
`route_id`			| ID that uniquely identifies a route.

File MAY contain the following attributes:
Optional Attributes	| Description										
----------			| -------------	
`path_name`			| Text name of the path
`path_description`	| Text description of the path
`direction_id`		| ID that contains a binary value that indicates the direction of the trip.  This should be included and match `direction_id` values in trips.txt if `direction_id` is included in trips.txt
`first_stop_id`		| First `stop_id` in the route to be included in the path.
`last_stop_id`		| Last `stop_id` in the route to be included in the path.