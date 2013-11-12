Organization
=====================

The organization part supports the following commands.

| Command                            | Description                                    | Access level |
| :--------------------------------- |:---------------------------------------------- |:-------------|
| [tree](#tree)                      | get the folder from the organization tree      | read         |
| [find](#find)                      | find the first child matched by name           | read         |
| [query](#query)                    | find all descendants by name and/or uid        | read         |
| [move](#move)                      | move an entry in the tree                      | delete       |
| [delete](#delete)                  | remove an entry from the system (no way back)  | delete       |
| [modify](#modify)                  | modify information from an entry               | write        |
| [alias](#alias)                    | create an alias from an entry                  | write        |
| [group](#group)                    | add an entry to a group                        | write        |
| [objectclass](#objectclass)        | get information from an entry                  | read         |
| [login](#login)                    | verify login credentials                       | read         |
| [create](#create)                  | create a new entry                             | write        |
| [search](#search)                  | advanced search                                | read         |
| [objectclasses](#objectclasses)    | see objectclass, this command returns multiple | read         |
| [entry](#entry)                    | get tree information for this entry            | read         |
| [wall](#wall)                      | get the wall of this entry                     | write        |

## Tree ##
_  Get the folder from the organization tree  _

Parameters:

- id => the id of the parent element

Returns:

- array of organizationalUnits (folders)


## Find ##
_ Find the first child matched by name _

Parameters:

- id => the id of the parent element
- name => the exact name of the element to find 

Returns:

- entry


## Query ##
_ Find all descendants by name and/or uid  _

Parameters:

- id => the id of the parent element
- q => the string that will match to the entry's name or uid
- _ optional _ limit
- _ optional _ offset

Returns:

- array of entries


## Move ##
_ Move an entry in the tree  _

Parameters:

- id => the id of the source element
- target => the id of the entry that it will be moved to

Returns:

- string: true/false


## Delete ##
_ Remove an entry from the system (no way back)  _

Parameters:

- id => the id of the parent element
- target => the id of the entry that will be removed

Returns:

- string: true/false


## Alias ##
_ Create an alias from an entry  _

Parameters:

- id => the id of the parent element
- target => the id of the entry that the entry will be moved to

Returns:

- string: true/false


## Group ##
_ Add an entry to a group  _

Parameters:

- id => the id of the element to add to the group
- target => the id of the group entry

Returns:

- string: true/false


## Objectclass ##
_ Get information from an entry  _

Parameters:

- id => the id of the element to add to the group
- tab => the name of the tab to get information from

Returns:

- mixed (depending on tab)


## Login ##
_ Verify login credentials  _

Parameters:

- uid => username
- password => password
- returnType => boolean|entry default: boolean

Returns:

- mixed (depending on return type)


## Create ##
_ Create a new entry  _

Parameters:

- id => the id of the parent element 
- name => name of the new element
- objectclass => objectclass (string) of the new element genkgoPerson|organization|group|organizationalRole etc.

Returns:

- entry object


## Entry ##
_ Get tree information for this entry  _

Parameters:

- id => the id of the element 

Returns:

- entry object
- 


## Wall (read) ##
_ Get wall posts for this entry  _

Parameters:

- id => the id of the entry
- _ optional _ type => the type of wallposts (default on log)

Returns:

- list of messages

## Wall (write) ##
_ Write a wall post from sender to recipients  _

Parameters:

- sender => the id of the sender entry
- type => The type of wallpost. Most common are public, private and log.
- recipients => array of the id's of the sender entries
- message => The message to be send

Returns:
- the send message
