---
layout: page
---

# Add a Recommendation for a Movie

## Introduction

In this tutorial, you will learn how to add a recommendation for the movie "Broker" to the Recommendations database using a POST request. This operation allows you to suggest a movie recommendation based on an existing movie in the database.

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

**Step 5.** Enter URL: Type in the URL for adding a recommendation. For example, if your API endpoint for adding recommendations is `http://localhost:3000/recommendations`, use that URL.

**Step 6.** Set Request Body: In the request body section, select the JSON option. Then, provide the required information needed for the recommendation.

For recommendations, ensure you include the following details in the request body:

    movie_id: The unique identifier of the movie for which you are adding a recommendation.
    rec: The name of the recommended movie.
    genre: The genre of the recommended movie.
    year: The release year of the recommended movie.
    country: The country of origin of the recommended movie.
    language: The language(s) spoken in the recommended movie.

Note 1: The `id` for the recommendation will be generated automatically by the server upon insertion into the database. Ensure to provide the correct movie `id` for the movie you're recommending.

Note 2: [Click here](tutorials/get_a_movie.md) to check if the movie is in the database before adding a recommendation and/or to find their `movie_id`.

See an example below for guidance.

```json
{
  "movie_id": 4,
  "rec": "Broker",
  "genre": "drama",
  "year": 2022,
  "country": "South Korea",
  "language": "Korean",
  "id": 8
}
```

**Step 7.** Send Request: Click on the "Send" button.

### Viewing the Response

If the recommendation is successfully added to the database, you will receive a response confirming the addition with the details of the added recommendation.

{
  "message": "Recommendation added successfully.",
  "recommendation": {
    "movie_id": 4,
    "rec": "Broker",
    "genre": "drama",
    "year": 2022,
    "country": "South Korea",
    "language": "Korean",
    "id": 8
  }
}

### Error Handling

If there are any errors during the process, such as missing or invalid data, you will receive an error response indicating the issue.

```json
{
  "error": "Failed to add recommendation. Genre must be provided and should be a string."
}
```

