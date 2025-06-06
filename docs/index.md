# Well-Read Service: API documentation for a fantasy book recommendation service

Welcome to the REST API of **Well-Read**, a simple service where you can receive book recommendations from an extensive collection of fantasy novels based on personas crafted with different reader preferences.

Use this API to learn how to install the service in your system, add books to the collection, get book recommendations based on personas, and refine personas by adding preference tags to get better book recommendations.

|                                 |                                    |     **Quick links**     |                                 |                                         |
|---------------------------------|------------------------------------|:-----------------------:|---------------------------------|-----------------------------------------|
| [Install service](#get-started) | [API authentication](#get-started) | [Tutorials](#tutorials) | [API reference](#api-reference) | [About the service](#about-the-service) |

---

## Get started

> Have you [installed the Well-Read Service](placeholder.md) and [established an authenticated connection](placeholder.md) in your development system? Make sure you have all the requirements in your system before you begin.

Let's start with a quick tutorial on getting a book recommendation based on a specific reader persona. Make sure that the **Well-Read** Service in your system has at least one [`book`](api/book.md) resource and one [`persona`](api/persona.md) resource in its database before you start this tutorial.

Getting a book recommendation in the service requires that you use the `GET` method to retrieve the details of a [`persona`](api/persona.md) resource in the service.

**To get a book recommendation by persona:**

1. Start the service by using this command in your command-line tool.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/users`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```js
        {
            "last_name": "Jones",
            "first_name": "Jenny",
            "email": "jen.jones@example.com"
        }
        ```

4. In the Postman app, choose **Send** to make the request.
5. The response body should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

    ```js
    {
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com",
        "id": 5
    }
    ```

---

## Tutorials

Now that you've successfully [received your first book recommendation](#get-started), you can take a look at tutorials for more operations in the service:

* [Get all personas](placeholder.md)
* [Get a book by ID](placeholder.md)
* [Add a book](placeholder.md)
* [Update a persona's preference tags](placeholder.md)

---

## API reference

> The `{base_url}` value of the resources depends on the installation of the service.
>
> When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

### Resources for the To-Do Service

* [book](api/book.md)
* [persona](api/persona.md)

---

## About the service

TBD
