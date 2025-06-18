# Tutorial: Find books by subgenre

> Have you [installed the **Well-Read** Service](../service-prerequisites.md) in your development system?
> Make sure you have all the prerequisites to run the service in your system before you continue.

The **Well-Read** Service's book collection contains novels categorized with different fantasy subgenres.
This tutorial teaches you how to retrieve a list of [`book`](../api/book.md) resources with a specific fantasy subgenre.

>The tutorial takes approximately 5 minutes to complete.

For this tutorial, you'll retrieve a list of all the books in the database with the **epic** subgenre.

## Get books by subgenre

1. Start the service by running this command in your preferred command-line tool:

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/books?subgenre=epic`
    * **Headers**: `N/A`
    * **Request body**:`N/A`

4. In the Postman app, click the **Send** button to make the request.
5. The response body should return all the books in the database with the **epic** subgenre:

    ```js
    {
        "title": "Assasin's Apprentice",
        "author": "Robin Hobb",
        "page_count": 672,
        "subgenre": "epic",
        "pace": "slow",
        "tags": [
            "adventurous",
            "epic",
            "world-building"
        ],
        "is_series": "true",
        "id": 4
    },
    {
        "title": "Tress of the Emerald Sea",
        "author": "Brandon Sanderson",
        "page_count": 384,
        "subgenre": "epic",
        "pace": "slow",
        "is_series": "false",
        "tags": [
            "low-fantasy",
            "adventurous",
            "epic",
            "whimsical"
        ],
        "id": 5
    }
    ```

## Next steps

Now that you know how to retrieve books by subgenre, you can filter books using the other `book` resource properties.
View the [reference topics](../index.md#api-reference) for the `book` resource to experiment with different ways to retrieve books.
You can even combine different properties in your API request for more refined results.
