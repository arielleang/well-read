# Tutorial: Update a reader persona

> Have you [installed the **Well-Read** Service](../service-prerequisites.md) in your development system?
> Make sure you have all the prerequisites to run the service in your system before you continue.

The **Well-Read** Service features reader personas designed to match users with fantasy books in the collection.
This tutorial teaches you how to update a [`persona`](../api/persona.md) resource to add more details about the persona's book preferences.

>The tutorial takes approximately 15 minutes to complete.

For this tutorial, you'll update the `description` and `related_tags` properties of the **Enchanted Wanderer** persona.
You can view the current `persona` object below:

```js
 {
    "name": "Enchanted Wanderer",
    "description": "Likes fairytale-like fantasy that includes whitches, faries, or other creatures, often related to romance",
    "subgenres_explored": ["romantasy","magical-realism", "fairy-tale"],
    "typical_pace": ["slow"],
    "related_tags":["emotional","whimsical", "hopeful"],
    "id": 3
 }
 ```

Using the `PUT` method and the persona's ID to make an API request, you'll fix typos and add more details about the persona's book preferences in the `description` property. You'll also add the **happy-ending** value to the `related_tags` property.

## Put a persona by ID

1. Start the service by running this command in your preferred command-line tool:

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: PUT
    * **URL**: `{base_url}/personas/3`
    * **Headers**: `Content-Type: application/json`
    * **Request body**:

    ```js
    {
        "name": "Enchanted Wanderer",
        "description": "Likes fairytale-like fantasy that includes witches, fairies, or other creatures, often related to romance. Novels usually have a happy ending.",
        "subgenres_explored": ["romantasy","magical-realism", "fairy-tale"],
        "typical_pace": ["slow"],
        "related_tags":["emotional","whimsical", "hopeful", "happy-ending"],
        "id": 3
    }
    ```

    The request body must include the entire resource object. It should contain an updated `description` property that fixes the "witches" and "fairies" misspellings and a new sentence indicating that the reader persona prefers novels with happy endings. The `related_tags` property should also contain a new **happy-ending** value.

4. In the Postman app, click the **Send** button to make the request.
5. The response body should return the updated resource for the **Enchanted Wanderer** persona.
   Note that the `description` and `related_tags` properties should be updated with your changes.

    ```js
    [
        {
            "name": "Enchanted Wanderer",
            "description": "Likes fairytale-like fantasy that includes witches, fairies, or other creatures, often related to romance. Novels usually have a happy ending.",
            "subgenres_explored": [
                "romantasy",
                "magical-realism",
                "fairy-tale"
            ],
            "typical_pace": [
                "slow"
            ],
                "related_tags": [
            "emotional",
                "whimsical",
                "hopeful",
                "happy-ending"
            ],
            "id": 3
        }
    ]
    ```

## Next steps

With the newly updated details of the reader persona in mind, you can [add a book to the collection](add-a-book-to-the-collection.md) that would fit its criteria.
If you want to retrieve the [`persona`](../api/persona.md) resource to have the information ready before you update it, then you can take a look at the [Get a persona by name](../api/personas-get-a-persona-by-name.md) reference topic or follow the [Find your reader persona](find-your-reader-persona.md) tutorial.
