# `book` resource

> The `{base_url}` value of the resources depends on the installation of the service.
>
> When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

Base endpoint:

```shell

{base_url}/books
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
    "tags":["violence", "sad", "gore", "war", "world-building"],
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

* [Get a book by title](books-get-a-book-by-title.md)
* [Get all books](books-get-all-books.md)

## Create operations

* [Post a book](books-post-a-book.md)

## Update operations

* [Put a book by ID](books-put-a-book-by-id.md)

## Delete operations

* [Delete a book by ID](books-delete-a-book-by-id.md)
