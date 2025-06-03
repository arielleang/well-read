---
layout: page
---

# `book` resource

Base endpoint:

```shell

{server_url}/books
```

Contains information about the books in the service.

A book resource describes the database of fantasy books used for recommendations in the service.

To get a book recommendation from the service, you must add a persona to
the service first. Learn more about the [`persona`](persona.md) resource.

## Resource properties

Sample `book` resource

```js

{
    "title": "The Poppy War",
    "author": "R F Kuang",
    "page_count": 544,
    "subgenre":"grimdark",
    "pace": "medium",
    "is_series":"true",
    "id": 2
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `title` | string | The name of the book |
| `author` | string | The person who wrote the book |
| `page_count` | number | The number of pages in the book |
| `subgenre` | string | The fantasy subgenre of the book |
| `pace` | string | The user's last name. Valid values are: `values` |
| `is_series` | boolean | Whether the book belongs to a series or a stand-alone novel. If true, the book belongs to a series. |
| `id` | number | The book's unique record ID |

## Read operations

* [Get all users](users-get-all-users.md)
* [Get users by ID](users-get-user-by-id.md)
* [Get user by last name](./users-get-user-by-last-name.md)

## Create operations

* [Post users](users-post-users.md)

## Delete operations

* [Delete user by ID](Ref_DELETE_User.md)
