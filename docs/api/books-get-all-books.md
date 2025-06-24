# Get all books

Returns an array of [book](book.md) objects that contains all the books in the database.

## Method

`GET`

## URL

```shell

{base_url}/books
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

Returns the information retrieved by using `GET` to retrieve all the `book` objects in the database.

```json
[
    {
        "title": "Red Rising",
        "author": "Pierce Brown",
        "page_count": 400,
        "subgenre":"science_fiction",
        "pace": "fast",
        "tags":["violence", "war", "dark"],
        "is_series":"true",
        "id": 1
  
    },
    {
       "title": "The Poppy War",
        "author": "R F Kuang",
        "page_count": 544,
        "subgenre":"grimdark",
        "pace": "medium",
        "tags":["violence", "sad", "gore", "war", "world-building"],
        "is_series":"true",
        "id": 2
    },
    {
        "title": "The Dragon Republic",
        "author": "R F Kuang",
        "page_count": 672,
        "subgenre":"grimdark",
        "pace": "medium",
        "tags":["violence", "sad", "gore", "war", "world-building"],
        "is_series":"true",
        "id": 3
    },
    {
        "title": "Assasin's Apprentice",
        "author": "Robin Hobb",
        "page_count": 672,
        "subgenre":"epic",
        "pace": "slow",
        "tags":["adventurous", "epic", "world-building"],
        "is_series":"true",
        "id": 4
    },
    {
        "title": "Tress of the Emerald Sea",
        "author": "Brandon Sanderson",
        "page_count": 384,
        "subgenre":"epic",
        "pace": "slow",
        "is_series":"false",
        "tags":["low-fantasy", "adventurous", "epic", "whimsical"],
        "id": 5
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
