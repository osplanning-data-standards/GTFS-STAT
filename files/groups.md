## Group Definition Information
### A group is a collection of routes that serve a common corridor or origin-destination pair

 *  Filename MUST be `groups.txt`
 *  File MUST contain a record for every transit route and in a group
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.

File MUST contain the following required attributes:

Required Attributes	| Description										
----------			| -------------		
`group_id`			| ID that uniquely identifies a group.
`from_node_set`		| A list of nodes that define the starting point of a group. A route must contain these nodes to be included in the group, and the nodes in `from_node_set` must precede the nodes in `to_node_set`. The list of nodes should be enclosed in square brackets and separated by commas. Ex. [embarc_bart, embarc_muni]
`to_node_set`		| A list of nodes that define the ending point of a group.  A route must contain these nodes to be included in the group, and the nodes in `to_node_set` must follow the nodes in `from_node_set`.


File MAY contain the following attributes:

Optional Attributes	| Description										
----------			| -------------	
`group_name`		| Text name of the group
`group_description`	| Text description of the group
`thru_node_set`		| A list of nodes that define a midpoint of a group.  A route must contain these nodes to be included in the group, and the nodes in `thru_node_set` must fall between the nodes in `from_node_set` and `to_node_set`.