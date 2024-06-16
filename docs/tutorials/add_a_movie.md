# Add a Movie for Recommendation

## Introduction

In this tutorial, you will learn how to add the movie "Inception" to the Movies database using a POST request. This operation allows you to insert a new movie with its details into the database.

## Before you start

Make sure you've looked through the [before you start](.../quickstart/before_you_start.md) page.

## Step-by-Step Guide

### Making a POST Request Using Postman

**Step 1.** Start your local service if it's not running.

```shell
    cd <your-github-workspace>/watch_more_movies/api
    # Run the service and monitor its database file for updates
    json-server watch-more-db-source.json
```

**Step 2.** Open Postman: Launch the Postman application.

**Step 3.** Create a New Request: Click on "New" and then select "Request".

**Step 4.** Set Request Type: Choose POST from the dropdown menu.

**Step 5.** Enter URL: Type in the URL for adding a movie. For example, if your API endpoint for adding movies is `http://localhost:3000/movies`, use that URL.

**Step 6.** Set Request Body: In the request body section, select the JSON option. Then, provide the required information needed for adding a movie.

For adding a movie, ensure you include the following details in the request body:

    movie_name: The name of the movie.
    genre: The genre of the movie.
    year: The release year of the movie.
    country: The country of origin of the movie.
    language: The language(s) spoken in the movie.

Note: The ID for the movie will be generated automatically by the server upon insertion into the database.

```json
{
  "movie_name": "Inception",
  "genre": "sci-fi",
  "year": 2010,
  "country": "USA",
  "language": "English",
  "id": 4
}
```

**Step 7.** Send Request: Click on the "Send" button.

Viewing the Response

If the movie is successfully added to the database, you will receive a response confirming the addition with the details of the added movie.

```json
{
  "message": "Movie added successfully.",
  "movie": {
    "movie_name": "Inception",
    "genre": "sci-fi",
    "year": 2010,
    "country": "USA",
    "language": "English",
    "id": 4
  }
}
```

### Error Handling

If there are any errors during the process, such as missing or invalid data, you will receive an error response indicating the issue.

```json
{
  "error": "Failed to add the movie. Please ensure all required fields are provided and try again."
}
```
