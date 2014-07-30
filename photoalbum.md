Photoalbum
=====================
The following actions are available at the photoalbum site part.

| Command                            | Description                                    | Access level |
| :--------------------------------- |:---------------------------------------------- |:-------------|
| [albums](#albums)                  | return the list of available photoalbums       | write        |
| [find](#find)                      | find the first child matched by name           | write        |
| [query](#query)                    | find all descendants by name and/or uid        | write        |

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
| model                              | albums                                         |

Get all the subalbums of photoalbum with id 3.

| Key                                | Value                                          |
| :--------------------------------- |:---------------------------------------------- |
| token                              | api token                                      |
| part                               | site                                           |
| command                            | model                                          |
| model                              | albums                                         |
| albumId                            | 3                                              |
