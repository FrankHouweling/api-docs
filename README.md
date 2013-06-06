api-docs
========

The Genkgo API works as follows

1. Generate an API key in the Genkgo Admin
2. Grant rights to connect to the API and execute your operations
3. Include the Genkgo API source in your project. At this moment [nodejs](https://www.github.com/genkgo/api-nodejs) and [PHP](https://www.github.com/genkgo/api-php) are supported languages. Feel free to add you own language.
4. Construct an API object. The constructor has two parameters
	- the location of the API and;
	- your API key
5. Send your command. This method has three parameters
	- organization part, e.g. organization, site, communication, financial and/or project
	- command, please see below the specific command per organization part
	- parameters for the command
6. The return variable will be an array, object or boolean. Internally, the API works with JSON. The API script encodes to JSON before sending variables and decodes the JSON when receiving the result.
	- Conform RFC 4627, the returned JSON is encoded in Unicode. The default encoding is UTF-8.
	
## Organization

The organization part supports the following commands.

| Command                           | Parameters                         | Result            |
| :-------------------------------- |:---------------------------------- | :---------------- |
| tree                              | undocumented                       | undocumented      |
| find                              | undocumented                       | undocumented      |
| query                             | undocumented                       | undocumented      |
| move                              | undocumented                       | undocumented      |
| delete                            | undocumented                       | undocumented      |
| modify                            | undocumented                       | undocumented      |
| alias                             | undocumented                       | undocumented      |
| group                             | undocumented                       | undocumented      |
| objectclass                       | undocumented                       | undocumented      |
| login                             | undocumented                       | undocumented      |
| create                            | undocumented                       | undocumented      |
| search                            | undocumented                       | undocumented      |
| objectclasses                     | undocumented                       | undocumented      |
| entry                             | undocumented                       | undocumented      |
