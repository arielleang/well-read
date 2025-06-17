# Put a book by ID

Updates the [book](book.md) object specified by the `id` parameter, if it exists.

## Method

`PUT`

## URL

```shell

{base_url}/books/{id}
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `title` | string | The name of the book | Yes |
| `author` | string | The person who wrote the book | Yes |
| `page_count` | number | The number of pages in the book | Yes |
| `subgenre` | string | The fantasy subgenre of the book | Yes |
| `pace` | string | The user's last name. Valid values are: `slow`, `medium`, `fast` | Yes |
| `is_series` | boolean | Whether the book belongs to a series or a stand-alone novel. If true, the book belongs to a series. | Yes |
| `id` | number | The book's unique record ID | Yes |

You should specify all the listed parameters as the `PUT` method requires you to input the whole object into the request body.

## Request headers

`Content-Type: application/json`

## Request body

Shows an example of key-value pairs you could use to update a book. In this example, the `historical` value was added to the `tags` parameter.

```js
{
    "title": "The Dragon Republic",
    "author": "R F Kuang",
    "page_count": 672,
    "subgenre":"grimdark",
    "pace": "medium",
    "tags":["violence", "sad", "gore", "war", "world-building", "historical"],
    "is_series":"true",
    "id": 3
}
```

## Return body

Returns the information from the request body as the updated `book` object.

```js
{
    "title": "The Dragon Republic",
    "author": "R F Kuang",
    "page_count": 672,
    "subgenre":"grimdark",
    "pace": "medium",
    "tags":["violence", "sad", "gore", "war", "world-building", "historical"],
    "is_series":"true",
    "id": 3
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
