# Well-Read Service: API documentation for a fantasy book recommendation service

Welcome to the REST API of **Well-Read**, a simple service where you can receive book recommendations from an extensive collection of fantasy novels based on personas crafted with different reader preferences.

Use this API to learn how to [install the service in your system](service-prerequisites.md), [add books to the collection](./tutorials/add-a-book-to-the-collection.md), [get book recommendations based on reader personas](quickstart-tutorial.md), and [refine reader personas to get better book recommendations](./tutorials/update-a-reader-persona.md).

>To help you receive more accurate book recommendations, you can take the [Well-Read Persona Quiz](https://form.typeform.com/to/ooSs9696) to determine which reader persona fits you the best.
>The quiz comprises of 6 personality-based multiple choice questions and takes approximately 5 minutes to complete.

![Image of an open book that reveals a lush forest in a fantasy world](landingpage.jpg)

|                                 |                                    |     **Quick links**     |                                 |                                         |
|---------------------------------|------------------------------------|:-----------------------:|---------------------------------|-----------------------------------------|
| [Service prerequisites](#service-prerequisites) | [Quickstart tutorial](#get-started-with-a-quickstart-tutorial) | [Tutorials](#tutorials) | [API reference](#api-reference) | [About the service](#about-the-service) |

---

## Service prerequisites

Before you can run the **Well-Read** Service, you need to have the following apps and files in your system:

* The database file for the service
* Version 0.17.0 of the JSON server or later
* The Postman desktop app
* A command-line tool

Follow the instructions in the [Service prerequisites](service-prerequisites.md) page to ensure that you have all you need to run the service properly.

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## Get started with a quickstart tutorial

Let's dive right into the **Well-Read** Service with a quick tutorial to get book recommendations based on specific properties of a reader persona.
Make sure you have all the [service prerequisites](service-prerequisites.md) in your development system and 20 minutes to take the tutorial before you begin.

> Access the quickstart tutorial [here](quickstart-tutorial.md).

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## Tutorials

After you've successfully [received your first book recommendation](quickstart-tutorial.md), you can take a look at more tutorials for things you can do in the service:

* [Find your reader persona](./tutorials/find-your-reader-persona.md)
* [Update a reader persona](./tutorials/update-a-reader-persona.md)
* [Add a book to the collection](./tutorials/add-a-book-to-the-collection.md)
* [Find books by subgenre](./tutorials/find-books-by-subgenre.md)

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## API reference

> The `{base_url}` value of the resources depends on the installation of the service.
>
> When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

### Resources and reference topics for the service

* [book](api/book.md)
    * [Post a book](api/books-post-a-book.md)
    * [Get a book by title](api/books-get-a-book-by-title.md)
    * [Get all books](api/books-get-all-books.md)
    * [Put a book by ID](api/books-put-a-book-by-id.md)
    * [Delete a book by ID](api/books-delete-a-book-by-id.md)

* [persona](api/persona.md)
    * [Post a persona](api/personas-post-a-persona.md)
    * [Get a persona by name](api/personas-get-a-persona-by-name.md)
    * [Get all personas](api/personas-get-all-personas.md)
    * [Put a persona by ID](api/personas-put-a-persona-by-id.md)
    * [Delete a persona by ID](api/personas-delete-a-persona-by-id.md)

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)

---

## About the service

Fantasy is a far-reaching genre with a variation of subgenres that are ever-expanding.
The **Well-Read** Service provides you with book recommendations based on the reader persona with which you identify most.
The service suggests novels based on pace, topics covered, and themes.
Use the **Well-Read** Service to discover a variety of niche books that complement your reading style.

[_^ Back to top_](#well-read-service-api-documentation-for-a-fantasy-book-recommendation-service)
