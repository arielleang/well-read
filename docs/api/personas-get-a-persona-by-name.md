# Get a persona by name

Returns the [persona](persona.md) specified by the `name` parameter, if it exists.

## Method

`GET`

## URL

```shell

{base_url}/personas?name={value}
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `name` | string | The name of the persona | Yes |

## Request headers

None

## Request body

None

## Return body

Returns the information retrieved by using `GET` to retrieve a persona by `name`.

```json
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
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
