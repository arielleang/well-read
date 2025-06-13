# Service prerequisites

To run the **Well-Read** Service, you must have the following prerequisites in your system:

* The database file for the service
* The latest version of the JSON server
* The Postman desktop app
* A command line tool

After you have all the prerequisites in your system, [test the service](#test-the-service) by running a basic API request.

Expect this preparation to take about 10 minutes to complete.

## The database file for the service

To get the `well-read-db.json` database file, please contact the technical writer for the API documentation.
Once you have access to the file, download and save it to an easily accessible location in your system.

## The latest version of the JSON server

To download and install the JSON server, follow the instructions on the software's [official website](https://www.npmjs.com/package/json-server).

## The Postman desktop app

To download and install the Postman desktop app, follow the instructions on the app's [official website](https://www.postman.com/downloads/).
Because you're running the **Well-Read** Service locally in your system, you can't use the web version of Postman.

## A command line tool

You can use the built-in command line tool in your operating system or your preferred command line tool.

## Test the service

Now that you have all the prerequisites in your system, it's time to test the service by running a basic API request:

1. Open your preferred command line tool and run the following command:

    ```shell
    cd <directory of the database file location>
    json-server well-read-db.json
    ```

    If you installed the software correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Keep the JSON server running in that window and open another window of the command line tool to make the following test call to the service:

    ```shell
    curl http://localhost:3000/books
    ```

3. If the service is running correctly, you should see a list of books from the service, such as in this example:

    ```js
    {
      "title": "Red Rising",
      "author": "Pierce Brown",
      "page_count": 400,
      "subgenre":"science_fiction",
      "pace": "fast",
      "tags":["violence", "war", "dark"],
      "is_series":"true",
      "id": 1
    }
    ```

## Troubleshoot the service

If you receive an error during any step of the test, here are some common issues that may have caused the error:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you successfully completed the test, you're ready to do the [quick start tutorial](index.md#get-started) or the other [available tutorials](index.md#tutorials).
