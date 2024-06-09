# Add a recommendation for a movie

## Overview

This API allows you to add a new recommendation to the database.

## Endpoints

### POST /recommendations

Add a new recommendation to the database.

#### Request Body
The request body should be a JSON object with the following fields:

- `movie_id` (integer): The ID of the movie for which you're adding a recommendation.
- `rec` (string): The title of the recommended movie.
- `genre` (string): The genre of the recommended movie.
- `year` (integer): The release year of the recommended movie.
- `country` (string): The country where the recommended movie was produced.
- `language` (string): The language of the recommended movie.
- `id` (integer): The unique ID of the recommendation.

#### Example Request

```json
{
  "movie_id": 1,
  "rec": "Broker",
  "genre": "Drama",
  "year": 2022,
  "country": "South Korea",
  "language": "Korean",
  "id": 4
}
```

Response

The response will be a JSON object confirming the addition of the recommendation with a success message and the details of the added recommendation.

```json
{
  "message": "Recommendation added successfully.",
  "recommendation": {
    "movie_id": 1,
    "rec": "Broker",
    "genre": "Drama",
    "year": 2022,
    "country": "South Korea",
    "language": "Korean",
    "id": 4
  }
}
```
