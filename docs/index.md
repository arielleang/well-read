# Well-Read Service: API documentation for a fantasy book recommendation service

Welcome to the REST API of **Well-Read**, a simple service where you can receive book recommendations from an extensive collection of fantasy novels based on personas crafted with different reader preferences.

Use this API to learn how to install the service in your system, add books to the collection, get book recommendations based on personas, and refine personas by adding preference tags to get better book recommendations.

|                                 |                                    |     **Quick links**     |                                 |                                         |
|---------------------------------|------------------------------------|:-----------------------:|---------------------------------|-----------------------------------------|
| [Service prerequisites](service-prerequisites.md) | [Quickstart tutorial](#get-started) | [Tutorials](#tutorials) | [API reference](#api-reference) | [About the service](#about-the-service) |

---

## Get started with a quickstart tutorial

> Have you [installed the **Well-Read** Service](service-prerequisites.md) in your development system?
> Make sure you have all the prerequisites to run the service in your system before you begin.

With the extensive selection of fantasy novels along with well-defined reader personas, it's easy and fun to get a book recommendation using the **Well-Read** Service.

Let's start with a quick tutorial to get book recommendations based on specific properties of a reader persona.

First, use the `GET` method to retrieve a [`persona`](api/persona.md) resource in the service. For this tutorial, get the **Morally Grey Malcontent** reader persona.

**Part 1: Get a persona by name**

1. Start the service by using this command in your preferred command-line tool.

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `http://localhost:3000/personas?name=Morally Grey Malcontent`
    * **Headers**: `N/A`
    * **Request body**:`N/A`

4. In the Postman app, click the **Send** button to make the request.
5. The response body should return the resource for the **Morally Grey Malcontent** persona:

    ```js
    {
        "name": "Morally Grey Malcontent",
        "description": "Likes high-stakes, violent books that explore morality.",
        "subgenres_explored": [
            "grimdark",
            "epic",
            "science-fiction"
        ],
        "typical_pace": [
            "medium",
            "fast"
        ],
        "related_tags": [
            "violence",
            "sad",
            "dark",
            "gore",
            "gothic",
            "war"
        ],
        "id": 2
    }
    ```

> You're halfway done with the tutorial.
> Keep the service running in your system and leave the Postman app open.

As a user looking for a book recommendation, use the `GET` method to retrieve a book resource based on the following properties in the persona you retrieved in your previous API request: `subgenres_explored: grimdark`, `typical_pace: medium`.

The equivalent key-value pairs for the `book` resource are: `subgenre: grimdark`, `pace: medium`.

**Part 2: Get a book by properties**

1. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `http://localhost:3000/books?subgenre=grimdark&pace=medium`
    * **Headers**: `N/A`
    * **Request body**:`N/A`
2. In the Postman app, choose **Send** to make the request.
3. The response body should return the `book` resources that match the filters:

    ```js
    {
        "title": "The Poppy War",
        "author": "R F Kuang",
        "page_count": 544,
        "subgenre": "grimdark",
        "pace": "medium",
        "tags": [
            "violence",
            "sad",
            "gore",
            "war",
            "world-building"
        ],
        "is_series": "true",
        "id": 2
    },
    {
        "title": "The Dragon Republic",
        "author": "R F Kuang",
        "page_count": 672,
        "subgenre": "grimdark",
        "pace": "medium",
        "tags": [
            "violence",
            "sad",
            "gore",
            "war",
            "world-building"
        ],
        "is_series": "true",
        "id": 3
    }
    ```

You now have some book recommendations based on specific properties taken from a reader persona.
After completing this tutorial, you can refine your search by narrowing down your filters or using different persona properties to get other book recommendations.

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## Tutorials

Now that you've successfully [received your first book recommendation](#get-started-with-a-quickstart-tutorial), you can take a look at tutorials for more operations in the service:

* [Get all personas](placeholder.md)
* [Get a book by ID](placeholder.md)
* [Add a book](placeholder.md)
* [Update a persona's preference tags](placeholder.md)

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## API reference

> The `{base_url}` value of the resources depends on the installation of the service.
>
> When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

### Resources for the To-Do Service

* [book](api/book.md)
    * [Post a book](api/books-post-a-book.md)
    * [Get a book by title](api/books-get-a-book-by-title.md)
    * [Put a book by ID](api/books-put-a-book-by-id.md)
    * [Delete a book by ID](api/books-delete-a-book-by-id.md)

* [persona](api/persona.md)
    * [Post a persona](api/personas-post-a-persona.md)
    * [Get a persona by name](api/personas-get-a-persona-by-name.md)
    * [Put a persona by ID](api/personas-put-a-persona-by-id.md)
    * [Delete a persona by ID](api/personas-delete-a-persona-by-id.md)

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## About the service

Fantasy is an expansive genre with a variation of sub-genres that are ever-expanding.
The **Well-Read** Service provides you with book recommendations based on the reader persona with which you identify most.
The service suggests novels based on pace, topics covered, and themes.
Use the **Well-Read** service to discover a variety of niche books that complement your reading style.

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)
