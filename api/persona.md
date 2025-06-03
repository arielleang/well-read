---
layout: page
---

# `persona` resource

Base endpoint:

```shell

{server_url}/personas
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
| `typical_pace` | string | The pace of books the persona prefers. Valid values are: `values` |
| `tags` | string | A comma-separated list of words that describe the books the persona prefers |
| `id` | number | The persona's unique record ID |

## Read operations

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID _(coming soon)_](#resource-properties)
* [Get task by user ID](./tasks-get-tasks-by-user-id.md)
* [get task with full-text search](./tasks-get-tasks-with-search)

## Create operations

* [Add a task resource](./tasks-add-a-task.md)

## Update operations

* [Put task by ID](./tasks-put-task-by-id.md)
