# Quickstart tutorial: Get a book recommendation based on a reader persona

> Have you [installed the **Well-Read** Service](service-prerequisites.md) in your development system?
> Make sure you have all the prerequisites to run the service in your system before you continue.

With the extensive selection of fantasy novels along with well-defined reader personas, it's easy and fun to get a book recommendation using the **Well-Read** Service.

Let's start with a quick tutorial to get book recommendations based on specific properties of a reader persona.

>The tutorial takes approximately 20 minutes to complete.

## Part 1: Get a persona by name

First, use the `GET` method to retrieve a [`persona`](api/persona.md) resource in the service.
For this tutorial, you'll need to retrieve the **Morally Grey Malcontent** reader persona.

1. Start the service by running this command in your preferred command-line tool.

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/personas?name=Morally Grey Malcontent`
    * **Headers**: `N/A`
    * **Request body**:`N/A`

4. In the Postman app, click the **Send** button to make the request.
5. The response body should return the resource for the **Morally Grey Malcontent** persona:

    ```js
    {
      "name": "Morally Grey Malcontent",
      "description": "Likes high-stakes, violent books that explore morality.",
      "subgenres_explored": ["grimdark", "epic", "science-fiction"],
      "typical_pace":["medium", "fast"],
      "related_tags": ["violence","sad","dark","gore","gothic", "war"],
      "id": 2
    }
    ```

> You're halfway done with the tutorial.
> Keep the service running in your system and leave the Postman app open.

## Part 2: Get a book by subgenre and pace

As a user looking for a book recommendation, use the `GET` method to retrieve a book resource based on the following properties in the persona you retrieved in your previous API request: `subgenres_explored: grimdark`, `typical_pace: medium`.

The equivalent key-value pairs for the `book` resource are: `subgenre: grimdark`, `pace: medium`.

1. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/books?subgenre=grimdark&pace=medium`
    * **Headers**: `N/A`
    * **Request body**:`N/A`
2. In the Postman app, choose **Send** to make the request.
3. The response body should return the `book` resources that match the filters:

    ```js
    [
      {
       "title": "The Poppy War",
        "author": "R F Kuang",
        "page_count": 544,
        "subgenre":"grimdark",
        "pace": "medium",
        "tags":["violence", "sad", "gore", "war", "world-building"],
        "is_series":"true",
        "id": 2
      },
      {
        "title": "The Dragon Republic",
        "author": "R F Kuang",
        "page_count": 672,
        "subgenre":"grimdark",
        "pace": "medium",
        "tags":["violence", "sad", "gore", "war", "world-building"],
        "is_series":"true",
        "id": 3
      }
    ]
    ```

You now have some book recommendations based on specific properties taken from a reader persona.

## Next steps

After completing this tutorial, you can refine your search by narrowing down your filters or using different persona properties to get other book recommendations.
You can also try out [more tutorials](index.md#tutorials) for other things you can do in the **Well-Read** Service.
