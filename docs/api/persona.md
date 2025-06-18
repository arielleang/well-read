# `persona` resource

> The `{base_url}` value of the resources depends on the installation of the service.
>
> When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

Base endpoint:

```shell

{base_url}/personas
```

Contains information about personas used to get book recommendations in the service.

## Resource properties

Sample `persona` resource

```js

{
    "name": "Rainy Day Reader",
    "description": "Likes low-risk, cozy books that elicit emotions of joy and wonder.",
    "subgenres_explored": ["cozy", "magical-realism", "low-fantasy"],
    "typical_pace": "slow",
    "tags": ["emotional","light","adventurous","funny"],
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | The name of the persona |
| `description` | string | A short description about the books the persona prefers |
| `subgenres_explored` | string | A comma-separated list of fantasy subgenres the persona prefers |
| `typical_pace` | string | The pace of books the persona prefers. Valid values are: `slow`, `medium`, `fast` |
| `tags` | string | A comma-separated list of words that describe the books the persona prefers |
| `id` | number | The persona's unique record ID |

## Read operations

* [Get a persona by name](personas-get-a-persona-by-name.md)
* [Get all personas](personas-get-all-personas.md)

## Create operations

* [Post a persona](personas-post-a-persona.md)

## Update operations

* [Put a persona by ID](personas-put-a-persona-by-id.md)

## Delete operations

* [Delete a persona by ID](personas-delete-a-persona-by-id.md)
