# Get all personas

Returns an array of [persona](persona.md) objects that contains all the reader personas in the database.

## Method

`GET`

## URL

```shell

{base_url}/personas
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

Returns the information retrieved by using `GET` to retrieve all the `persona` objects in the database.

```json
[
    {
        "name": "Rainy Day Reader",
        "description": "Likes low-risk, cozy books that elicit emotions of joy and wonder.",
        "subgenres_explored": ["cozy", "magical-realism", "low-fantasy"],
        "typical_pace": "slow",
        "related_tags": ["emotional","light","adventurous","funny"],
        "id": 1
    },
    {
        "name": "Morally Grey Malcontent",
        "description": "Likes high-stakes, violent books that explore morality.",
        "subgenres_explored": ["grimdark", "epic", "science-fiction"],
        "typical_pace":["medium", "fast"],
        "related_tags": ["violence","sad","dark","gore","gothic", "war"],
        "id": 2
    },
    {
        "name": "Enchanted Wanderer",
        "description": "Likes fairytale-like fantasy that includes whitches, faries, or other creatures, often related to romance",
        "subgenres_explored": ["romantasy","magical-realism", "fairy-tale"],
        "typical_pace": ["slow"],
        "related_tags":["emotional","whimsical", "hopeful"],
        "id": 3
    },
    {
        "name": "Adrenaline Junkie",
        "description": "Likes high-fantasy books in the realm of science fiction or medieval times that often includes an anti-hero that must save their world.",
        "subgenres_explored": ["science-fiction", "epic", "sword-and-stone", "futuristic"],
        "typical_pace": ["fast"],
        "related_tags":["dark","world-building", "emotional","adventurous", "war"],
        "id": 4
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
