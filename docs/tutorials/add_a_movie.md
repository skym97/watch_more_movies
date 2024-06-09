# Add a movie for recommendation

## Overview

This API allows you to add a new movie to the database.

## Endpoints

### POST /movies

Add a new movie to the database.

#### Request Body
The request body should be a JSON object with the following fields:

- `movie_name` (string): The name of the movie.
- `genre` (string): The genre of the movie.
- `year` (integer): The release year of the movie.
- `country` (string): The country where the movie was produced.
- `language` (string): The language of the movie.
- `id` (integer): The unique ID of the movie.

#### Example Request

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

Response

The response will be a JSON object confirming the addition of the movie with a success message and the details of the added movie.

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
