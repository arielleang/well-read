# Tutorial: Find your reader persona

> Have you [installed the **Well-Read** Service](../service-prerequisites.md) in your development system?
> Make sure you have all the prerequisites to run the service in your system before you continue.

The **Well-Read** Service features reader personas designed to match users with fantasy books in the collection.
This tutorial teaches you how to determine your own reader persona and how to retrieve the details of that [`persona`](../api/persona.md) resource using its name.

>The tutorial takes approximately 15 minutes to complete.

## Part 1: Complete the Well-Read Persona Quiz

First, take the [Well-Read Persona Quiz](https://form.typeform.com/to/ooSs9696) to determine which reader persona fits you the best. The quiz contains six personality-based multiple choice questions and takes approximately 5 minutes to complete.

## Part 2: Get a persona by name

After you complete the quiz and get your reader persona result, use the `GET` method to retrieve the [`persona`](../api/persona.md) resource in the service using the name of the persona.

For this tutorial, you'll need to retrieve the **Rainy Day Reader** persona.

1. Start the service by running this command in your preferred command-line tool:

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/personas?name=Rainy Day Reader`
    * **Headers**: `N/A`
    * **Request body**:`N/A`

4. In the Postman app, click the **Send** button to make the request.
5. The response body should return the resource for the **Rainy Day Reader** persona:

    ```js
    {
        "name": "Rainy Day Reader",
        "description": "Likes low-risk, cozy books that elicit emotions of joy and wonder.",
        "subgenres_explored": ["cozy", "magical-realism", "low-fantasy"],
        "typical_pace": "slow",
        "related_tags": ["emotional","light","adventurous","funny"],
        "id": 1
    }
    ```

## Next steps

Now that you have the details of your reader persona, you can use its properties to [get a book recommendation](../quickstart-tutorial.md).
You can also [update the persona](update-a-reader-persona.md) to give users a more defined idea of the persona's book preferences.
