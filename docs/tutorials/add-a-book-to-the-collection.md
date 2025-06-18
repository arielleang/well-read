# Tutorial: Add a book to the collection

> Have you [installed the **Well-Read** Service](../service-prerequisites.md) in your development system?
> Make sure you have all the prerequisites to run the service in your system before you continue.

The **Well-Read** Service has an extensive collection of books in its database with different fantasy subgenres. However, the database occasionally needs to be updated to include newly published books or recommended novels.
This tutorial teaches you how to add a [`book`](../api/book.md) resource to the collection with properties that match a [`persona`](../api/persona.md) resource's criteria.

>The tutorial takes approximately 20 minutes to complete.

For this tutorial, you'll add a [`book`](../api/book.md) resource that matches the **Adrenaline Junkie** persona.
You can view the resource object for the **Adrenaline Junkie** persona below:

```js
{
    "name": "Adrenaline Junkie",
    "description": "Likes high-fantasy books in the realm of science fiction or medieval times that often includes an anti-hero that must save their world.",
    "subgenres_explored": ["science-fiction", "epic", "sword-and-stone", "futuristic"],
    "typical_pace": ["fast"],
    "related_tags":["dark","world-building", "emotional","adventurous", "war"],
    "id": 4
}
 ```

Using the `POST` method, you'll add the book **A Memory Called Empire** by Arkady Martine to the database, which shares the `science-fiction` subgenre and the `fast` reading pace preferences of the **Adrenaline Junkie** persona.

## Post a book

1. Start the service by running this command in your preferred command-line tool:

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{base_url}/books`
    * **Headers**: `Content-Type: application/json`
    * **Request body**:

    ```js
    {
        "title": "A Memory Called Empire",
        "author": "Arkady Martine",
        "page_count": 462,
        "subgenre":"science-fiction",
        "pace": "fast",
        "tags":["world-building", "politics", "mystery", "space opera"],
        "is_series":"true"
    }
    ```

    The request body must include all the properties listed in the [`book`](../api/book.md) resource page. It should also include the key-value pairs: `subgenre: science-fiction`, `pace: fast` to match the **Adrenaline Junkie** persona properties.

4. In the Postman app, click the **Send** button to make the request.
5. The response body should return the new `book` resource for **A Memory Called Empire**, including a unique ID for the book.

    ```js
    {
        "title": "A Memory Called Empire",
        "author": "Arkady Martine",
        "page_count": 462,
        "subgenre": "science-fiction",
        "pace": "fast",
        "tags": [
            "world-building",
            "politics",
            "mystery",
            "space opera"
        ],
        "is_series": "true",
        "id": 6
    }
    ```

## Next steps

Now that you've added a new [`book`](../api/book.md) resource to the collection, you can try to get it as a book recommendation by reviewing the steps in the [quickstart tutorial](../quickstart-tutorial.md).
You can also find all the books with the `science-fiction` subgenre by following the [Find books by subgenre](find-books-by-subgenre.md) tutorial.
