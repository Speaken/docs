|Endpoint|Description|
|--------|-----------|
|[GET /users/:user_id/reviews](#get-usersme)| Get all user reviews |
|[POST /lessons/:lesson_id/reviews](#get-usersme)| Create a new review for a lesson |

## GET /users/:user_id/reviews

Get all user reviews 

### Example Request

```curl -X GET https://api.speaken.com/v1/users/:user_id/reviews```

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user_id```|not required|integer|Id of the user we want to retrieve the list of reviews|


## POST /lessons/:lesson_id/reviews

Create a new review for a lesson

### Example Request

```curl -X POST https://api.speaken.com/v1/lessons/1/reviews```

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lesson_id```|required|integer|Id of the lesson related to the review|
|```body```|required|string|Text of the review to be displayed on user's profile|
|```note```|required (only for a user)|integer|Note (between 0 and 5) of the teacher|
|```call_quality```|not required|integer|Note (between 0 and 5) for the quality of the call|
|```details['vocabulary']```|required (only for teacher)|integer|Note (between 0 and 5) for the vocabulary's user quality|
|```details['grammar']```|required (only for teacher)|integer|Note (between 0 and 5) for the grammar's user quality|
|```details['coolness']```|required (only for teacher)|integer|Note (between 0 and 5) for the coolness' user quality|
|```details['oral']```|required (only for teacher)|integer|Note (between 0 and 5) for the oral's user quality|
