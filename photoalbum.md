Photoalbum
=====================
The following actions are available at the photoalbum site part.

| Command                            | Description                                    | Access level |
| :--------------------------------- |:---------------------------------------------- |:-------------|
| [albums](#albums)                  | return the list of available photoalbums       | write        |
| [pictures](pictures)               | get all pictures in an album                   | write        |
| [picture](#picture)               | get the raw data of a given picture            | write        |

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

Parameters:

- albumId => the id of the photoalbum in which to look for pictures

Returns:

- array of picture names

### Example Post Values ###

Get all "root" pictures in photoalbum with id 3.

| Key                                | Value                                          |
| :--------------------------------- |:---------------------------------------------- |
| token                              | api token                                      |
| part                               | site                                           |
| command                            | model                                          |
| model                              | photoalbum                                     |
| action                             | pictures                                       |
| albumId                            | 3                                              |

## Picture ##
_  Returns raw data of a given picture  _

Parameters:

- albumId => the id of the photoalbum in which to look for the given picture
- photoName => the photo_name as given by the pictures api action

Returns:

- raw data of the given picture in full size

### Example Post Values ###

Get all "root" pictures in photoalbum with id 3.

| Key                                | Value                                          |
| :--------------------------------- |:---------------------------------------------- |
| token                              | api token                                      |
| part                               | site                                           |
| command                            | model                                          |
| model                              | photoalbum                                     |
| action                             | picture                                        |
| albumId                            | 3                                              |
| ohitiName                          | sample_picture.jpg                            |
