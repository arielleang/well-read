# Post a book

Adds a new [book](book.md) object.

## Method

`POST`

## URL

```shell

{server_url}/books/
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `title` | string | The name of the book | No |
| `author` | string | The person who wrote the book | No |
| `page_count` | number | The number of pages in the book | No |
| `subgenre` | string | The fantasy subgenre of the book | No |
| `pace` | string | The user's last name. Valid values are: `slow`, `medium`, `fast` | No |
| `is_series` | boolean | Whether the book belongs to a series or a stand-alone novel. If true, the book belongs to a series. | No |

You should specify all the listed parameters, even though the **Well-Read** Service doesn't require any.

## Headers

`Content-Type: application/json`

## Request body

Shows an example of key-value pairs you could use to create a new book.

```json
{
    "title": "The Poppy War",
    "author": "R F Kuang",
    "page_count": 544,
    "subgenre":"grimdark",
    "pace": "medium",
    "tags":["violence", "sad", "gore", "war", "world-building"],
    "is_series":"true",
}
```

## Return body

Returns the information from the request body plus a unique ID for the book.

```json
{
    "title": "The Poppy War",
    "author": "R F Kuang",
    "page_count": 544,
    "subgenre":"grimdark",
    "pace": "medium",
    "tags":["violence", "sad", "gore", "war", "world-building"],
    "is_series":"true",
    "id": 2
}
```

## Return status

| Status value | Return status | Description |
| ------------ | ------------- | ------------------------------------------------------------ |
| 201          | Created       | The server successfully created a new resource. |
| 400          | Bad Request   | The server couldn't understand the request. Maybe a bad syntax? |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
