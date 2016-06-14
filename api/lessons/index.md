|Endpoint|Description|
|--------|-----------|
|[GET /lessons](#get-usersme)| List all lessons|
|[POST /lessons](#get-usersme)| Create a new lesson |
|[PATCH,PUT /lessons/:id](#get-usersme)| Update a lesson|
|[DELETE /lessons/:id](#get-usersme)| Delete a lesson|
|[POST /lessons/:lesson_id/reviews](#put-usersme)| Review a lesson |
|[POST /lessons/:lesson_id/users](#put-usersme)| Join an existing session |
|[DELETE /lessons/:lesson_id/users/:id](#put-usersme)| Left a session |
|[POST /lessons/:lesson_id/archive](#put-usersme)| Archive a lesson |
|[DELETE /lessons/:lesson_id/archive/:id](#put-usersme)| Stop archiving a lesson |

## GET /lessons

List all lessons

### Example Request

```curl -X GET https://api.speaken.com/v1/lessons```


## POST /lessons

Create a new lesson

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lesson[:invitee_id]```|required|integer|User's id of the user you want to call|
|```lesson[:schedule_at]```|not required|datetime|When the lesson will start (if you want to plan the lesson in the future). If you don't provide it, it's an immediate lesson|
|```lesson[:language_id]```|not required|integer|Language id you want to learn. See languages call to get all the list|
|```lesson[:message]```|not required|string|If you want to provide a message for the teacher|

### Example Request

```curl -X POST https://api.speaken.com/v1/lessons```


## PATCH|PUT /lessons/:id

Update a lesson (only for teacher)

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lesson[:status]```|required|integer|Lesson status. Can be :accepted (or 1), :refused (or 2)|
|```lesson[:status_message]```|not required|string|If you want to provide a status explication|
|```lesson[:comment]```|not required|string|If you want to add a message to the user|

### Example Request

```curl -X PUT https://api.speaken.com/v1/lessons/1```

## DELETE /lessons/:id

Delete a lesson

### Example Request

```curl -X PUT https://api.speaken.com/v1/lessons/1```


## POST /lessons/:lesson_id/reviews

Create a review

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lesson_id```|required|integer|Id of the lesson|
|```review[:note]```|required|datetime|Note of the review. Between 0 and 5|
|```review[:body]```|required|integer|Comment the review|

### Example Request

```curl -X POST https://api.speaken.com/v1/lessons/1/reviews```


## POST /lessons/:lesson_id/users

Join a lesson session

### Example Request

```curl -X POST https://api.speaken.com/v1/lessons/1/users```


## DELETE /lessons/:lesson_id/users/:id

Left a lesson session

### Example Request

```curl -X DELETE https://api.speaken.com/v1/lessons/1/users/1```

## POST /lessons/:lesson_id/archives

Start archiving a lesson

### Example Request

```curl -X POST https://api.speaken.com/v1/lessons/1/archives```


## DELETE /lessons/1/archives/1

Stop archiving the lesson

### Example Request

```curl -X DELETE https://api.speaken.com/v1/lessons/1/archives/1```
