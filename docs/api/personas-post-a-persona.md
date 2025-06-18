# Post a persona

Adds a new [persona](persona.md) object.

## Method

`POST`

## URL

```shell

{base_url}/personas/
```

## Parameters

| Parameter name | Type   | Description | Required? |
| ------------- | ------ | ----------- | --------- |
| `name` | string | The name of the persona | No |
| `description` | string | A short description about the books the persona prefers | No |
| `subgenres_explored` | string | A comma-separated list of fantasy subgenres the persona prefers | No |
| `typical_pace` | string | The pace of books the persona prefers. Valid values are: `slow`, `medium`, `fast` | No |
| `tags` | string | A comma-separated list of words that describe the books the persona prefers | No |

You should specify all the listed parameters, even though the **Well-Read** Service doesn't require any.

## Headers

`Content-Type: application/json`

## Request body

Shows an example of key-value pairs you could use to create a new persona.

```json
{
    "name": "Rainy Day Reader",
    "description": "Likes low-risk, cozy books that elicit emotions of joy and wonder.",
    "subgenres_explored": ["cozy", "magical-realism", "low-fantasy"],
    "typical_pace": "slow",
    "related_tags": ["emotional","light","adventurous","funny"]
}
```

## Return body

Returns the information from the request body plus a unique ID for the persona.

```json
{
    "name": "Rainy Day Reader",
    "description": "Likes low-risk, cozy books that elicit emotions of joy and wonder.",
    "subgenres_explored": ["cozy", "magical-realism", "low-fantasy"],
    "typical_pace": "slow",
    "related_tags": ["emotional","light","adventurous","funny"],
    "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------ | ------------- | ------------------------------------------------------------ |
| 201          | Created       | The server successfully created a new resource. |
| 400          | Bad Request   | The server couldn't understand the request. Maybe a bad syntax? |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
