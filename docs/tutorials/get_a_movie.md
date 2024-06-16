---
layout: page
---

# Get (or find) a Movie 

## Introduction

In this tutorial, you will learn how to retrieve a movie from the database using a GET request based on the movie's name. 
This operation allows you to access specific movie details by querying with the movie's name.

## Before you start

Make sure you've looked through the [before you start](.../quickstart/before_you_start.md) page.

## Step-by-Step Guide

### Making a GET Request Using Postman

**Step 1.** Start your local service if it's not running.

```shell
    cd <your-github-workspace>/watch_more_movies/api
    # Run the service and monitor its database file for updates
    json-server watch-more-db-source.json
```

Step 2. **Open Postman**: Launch the Postman application.

Step 3. **Create a New Request**: Click on "New" and then select "Request".

Step 4. **Set Request Type**: Choose `GET` from the dropdown menu.

Step 5. **Enter URL**: Type in the URL for the movie you want to retrieve. For example, to get the movie named "John Wick", enter `http://localhost:3000/movies/name/John%20Wick`. Note that spaces should be encoded as `%20`.

Step 6. **Send Request**: Click on the "Send" button.

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

