# Get Recommendations by Country

## Introduction

In this tutorial, you will learn how to retrieve recommendations from the Recommendations database based on the country of the movie. This operation allows you to get a list of recommended movies filtered by a specific country.

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

**Step 2.** Open Postman: Launch the Postman application.

**Step 3.** Create a New Request: Click on "New" and then select "Request".

**Step 4.** Set Request Type: Choose GET from the dropdown menu.

**Step 5.** Enter URL: Type in the URL for getting recommendations by country. For example, if your API endpoint for getting recommendations by country is http://localhost:3000/recommendations/country/USA, use that URL.

**Step 6.** Send Request: Click on the "Send" button.

### Viewing the Response

If there are recommendations available for the specified country, you will receive a response containing a JSON array of recommended movies with details such as movie name, genre, year, country, language, and ID.

```json
[
  {
    "movie_id": 2,
    "rec": "Magnolia",
    "genre": "drama",
    "year": 1999,
    "country": "USA",
    "language": "English",
    "id": 3
  },
  {
    "movie_id": 3,
    "rec": "The Iron Giant",
    "genre": "animation",
    "year": 1999,
    "country": "USA",
    "language": "English",
    "id": 5
  }
]
```

### Error Handling

If there are no recommendations available for the specified country, you will receive an empty array as the response.

If there are any errors during the process, such as an invalid country or an issue with the database, you will receive an error response indicating the issue.

```json
{
  "error": "No recommendations found for the specified country."
}
```
