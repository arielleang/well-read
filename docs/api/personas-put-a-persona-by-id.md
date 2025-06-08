# Put a persona by ID

Updates the [persona](persona.md) object specified by the `id` parameter, if it exists.

## Method

`PUT`

## URL

```shell

{server_url}/personas/{id}
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `name` | string | The name of the persona | Yes |
| `description` | string | A short description about the books the persona prefers | Yes |
| `subgenres_explored` | string | A comma-separated list of fantasy subgenres the persona prefers | Yes |
| `typical_pace` | string | The pace of books the persona prefers. Valid values are: `slow`, `medium`, `fast` | Yes |
| `tags` | string | A comma-separated list of words that describe the books the persona prefers | Yes |
| `id` | number | The persona's unique record ID | Yes 

You should specify all the listed parameters as the `PUT` method requires you to input the whole object into the request body.

## Request headers

`Content-Type: application/json`

## Request body

Shows an example of key-value pairs you could use to update a persona. In this example, the `animal-companions` value was added to the `subgenres_explored` parameter.

```js
{
    "name": "Enchanted Wanderer",
    "description": "Likes fairytale-like fantasy that includes whitches, faries, or other creatures, often related to romance",
    "subgenres_explored": ["romantasy","magical-realism", "fairy-tale", "animal-companions"],
    "typical_pace": ["slow"],
    "related_tags":["emotional","whimsical", "hopeful"],
    "id": 3
}
```

## Return body

Returns the information from the request body as the updated `book` object.

```js
{
    "name": "Enchanted Wanderer",
    "description": "Likes fairytale-like fantasy that includes whitches, faries, or other creatures, often related to romance",
    "subgenres_explored": ["romantasy","magical-realism", "fairy-tale", "animal-companions"],
    "typical_pace": ["slow"],
    "related_tags":["emotional","whimsical", "hopeful"],
    "id": 3
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
