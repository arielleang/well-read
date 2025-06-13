# Get a book by title

Returns the [book](book.md) specified by the `title` parameter, if it exists.

## Method

`GET`

## URL

```shell

{server_url}/books?title={value}
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `title` | string | The name of the book | Yes |

## Request headers

None

## Request body

None

## Return body

Returns the information retrieved by using `GET` to retrieve a book by `title`.

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
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
