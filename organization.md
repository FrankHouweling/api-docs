Organization
=====================

The organization part supports the following commands.

| Command                            | Description                                    |
| :--------------------------------- |:---------------------------------------------- |
| [#tree](tree)                      | get the folder from the organization tree      |
| [#find](find)                      | find the first child matched by name           |
| [#query](query)                    | find all descendants by name and/or uid        |
| [#move](move)                      | move an entry in the tree                      |
| [#delete](delete)                  | remove an entry from the system (no way back)  |
| [#modify](modify)                  | modify information from an entry               |
| [#alias](alias)                    | create an alias from an entry                  |
| [#group](group)                    | add an entry to a group                        |
| [#objectclass](objectclass)        | get information from an entry                  |
| [#login](login)                    | verify login credentials                       |
| [#create](create)                  | create a new entry                             |
| [#search](search)                  | advanced search                                |
| [#objectclasses](objectclasses)    | see objectclass, this command returns multiple |
| [#entry](entry)                    | get tree information for this entry            |

## Tree ##
=======
## Tree ##
*Get the folder from the organization tree*
*Requires access level: read*

Parameters:
1. id => the id of the parent element

Returns:
array of organizationalUnits (folders)
