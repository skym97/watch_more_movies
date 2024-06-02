---
layout: page
---
# `movies` resource

Base endpoint:

```shell
{server_url}/movies
```
Contains information about the movies added for the purpose of receiving recommendations.

## Resource Properties

Sample `movies` resource

```js

  {
      "movie_name": "John Wick",
      "genre": "action",
      "year": 2014,
      "country": "USA",
      "language": "English",
      "id": 1
    }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `movie_name` | string | The movie's name |
| `genre` | string | The movie's genre |
| `year` | number | The year the movie was released |
| `language` | string | The language the movie is in |
| `id` | number | An identifying number for a movie to pair with recommendations |