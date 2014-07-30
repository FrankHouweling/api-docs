Events
=====================
The following actions are available at the events site part.

| Command                            | Description                                    | Access level |
| :--------------------------------- |:---------------------------------------------- |:-------------|

## Albums ##
_  Returns the list of available photoalbums  _

Parameters:

- albumId => the id of the parent photoalbum where to look for subalbums (optional)

Returns:

- array of Photoalbums

### Example Post Values ###

Get all "root" photoalbums.

| Key                                | Value                                          |
| :--------------------------------- |:---------------------------------------------- |
| token                              | api token                                      |
| part                               | site                                           |
| command                            | model                                          |
| model                              | photoalbum                                     |
| action                             | albums                                         |

Get all the subalbums of photoalbum with id 3.

| Key                                | Value                                          |
| :--------------------------------- |:---------------------------------------------- |
| token                              | api token                                      |
| part                               | site                                           |
| command                            | model                                          |
| model                              | albums                                         |
| model                              | photoalbum                                     |
| action                             | albums                                         |
| albumId                            | 3                                              |

## Pictures ##
_  Returns a list of all pictures in a specific photoalbum  _
