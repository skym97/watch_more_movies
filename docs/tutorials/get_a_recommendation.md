---
layout: page
---

# Get (or find) a Recommendation

## Introduction

In this tutorial, you will learn how to retrieve a movie from the movies database using a GET request based on the movie's name. 
This operation allows you to access specific movie details by querying with the movie's name.

## Before you start

Make sure you've looked through the [before you start](../quickstart/before_you_start.md) page.

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

Step 5. **Enter URL**: Type in the URL for the movie you want to retrieve. For example, to get the movie named "The Iron Giant", enter `http://localhost:3000/movies/name/The%20Iron%20Giant`. Note that spaces should be encoded as `%20`.

Step 6. **Send Request**: Click on the "Send" button.

### Viewing the Response

If the movie with the specified name exists, you will see a response similar to the following:

```json
 {
      "movie_id": 3,
      "rec": "The Iron Giant",
      "genre": "animation",
      "year": 1999,
      "country": "USA",
      "language": "English",
      "id": 5
    }
```

### Error Handling

If the recommendation does not exist or hasn't been added in, you will get a 404 Not Found response.

If you try to get a movie that does not exist (e.g., http://localhost:3000/movies/name/Unknown%20Movie), the server will respond with:

```json
{
  "error": "Recommendation not found"
}
```
### Related Information

To add a recommendation, refer to the [add a recommendation](tutorials/get_a_recommendation.md) tutorial. 
