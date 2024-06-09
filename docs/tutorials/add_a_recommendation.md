# Add a Recommendation to the Database

## Introduction

In this tutorial, you will learn how to add a recommendation for the movie "Broker" to the Recommendations database using a POST request. This operation allows you to suggest a movie recommendation based on an existing movie in the database.

## Step-by-Step Guide

### Making a POST Request Using Postman

**Step 1.** Open Postman: Launch the Postman application.

**Step 2.** Create a New Request: Click on "New" and then select "Request".

**Step 3.** Set Request Type: Choose POST from the dropdown menu.

**Step 4.** Enter URL: Type in the URL for adding a recommendation. For example, if your API endpoint for adding recommendations is http://localhost:3000/recommendations, use that URL.

**Step 5.** Set Request Body: In the request body section, select the JSON option.

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

**Step 6.** Send Request: Click on the "Send" button.

Viewing the Response

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

