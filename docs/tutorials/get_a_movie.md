---
layout: page
---

# GET (or find) a movie 

## Introduction

In this tutorial, you will learn how to retrieve a movie from the Movies database using a GET request based on the movie's name. 
This operation allows you to access specific movie details by querying with the movie's name.

## Step-by-Step Guide

### Making a GET Request Using Postman

Step 1. **Open Postman**: Launch the Postman application.

Step 2. **Create a New Request**: Click on "New" and then select "Request".

Step 3. **Set Request Type**: Choose `GET` from the dropdown menu.

Step 4. **Enter URL**: Type in the URL for the movie you want to retrieve. For example, to get the movie named "John Wick", enter `http://localhost:3000/movies/name/John%20Wick`. Note that spaces should be encoded as `%20`.

Step 5. **Send Request**: Click on the "Send" button.

### Viewing the Response

If the movie with the specified name exists, you will see a response similar to the following:

```json
{
  "movie_name": "John Wick",
  "genre": "action",
  "year": 2014,
  "country": "USA",
  "language": "English",
  "id": 1
}
```

### Error Handling

If the movie does not exist or hasn't been added in, you will get a 404 Not Found response.

If you try to get a movie that does not exist (e.g., http://localhost:3000/movies/name/Unknown%20Movie), the server will respond with:

```json
{
  "error": "Movie not found"
}
```

### Related Information

To add a movie, refer to the [add a movie tutorial](docs/tutorials/add_a_movie.md). 

