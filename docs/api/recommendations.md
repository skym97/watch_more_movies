---
layout: page
---
# `recommendations` resource

Base endpoint:

```shell
{server_url}/recommendations
```
Contains information about the recommendations added for certain movies.

## Resource Properties

Sample `recommendations` resource

```js

{
      "movie_id": 1,
      "rec": "The Legend of the Drunken Master",
      "genre": "action",
      "year": 2000,
      "country": "Hong Kong",
      "language": "Cantonese",
      "id": 1
    }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `movie_id` | number | Unique record ID for the recommended movie |
| `rec` | string | The recommended movie's name |
| `genre` | string | The recommended movie's genre |
| `year` | number | The year the recommended movie came out |
| `country` | string | The country the recommended movie is from |
| `language` | string | The language the recommended movie is in |
| `id` | number | Unique record ID for a movie |

## Operations

`user` resource that supports these operations.

### READ (GET)

* [Get (or find) a recommendation](../tutorials/get_a_recommendation.md)

* [Get recommendations by genre](../tutorials/get_recommendations_by_genre.md)

* [Get recommendations by country](../tutorials/get_recommendations_by_country.md)

* [Get recommendations by language](../tutorials/get_recommendations_by_language.md)

### CREATE (POST)

* [Add a recommendation](../tutorials/add_a_recommendation.md)
