# Add a Movie for Recommendation

## Introduction

In this tutorial, you will learn how to add the movie "Inception" to the Movies database using a POST request. This operation allows you to insert a new movie with its details into the database.

## Step-by-Step Guide

### Making a POST Request Using Postman

**Step 1.** Open Postman: Launch the Postman application.

**Step 2.** Create a New Request: Click on "New" and then select "Request".

**Step 3.** Set Request Type: Choose POST from the dropdown menu.

**Step 4.** Enter URL: Type in the URL for adding a movie. For example, if your API endpoint for adding movies is http://localhost:3000/movies, use that URL.

**Step 5.** Set Request Body: In the request body section, select the JSON option. Then, provide the required information needed for adding a movie.

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

**Step 6.** Send Request: Click on the "Send" button.

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

