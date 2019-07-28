
|Endpoint|Description|
|--------|-----------|
|[GET /user_topics](#get-user_topic)| List all user_topics|
|[GET /user_topics/:id](#get-specific-user_topic)| Get a user_topic by its id|
|[POST /user_topics](#create-user_topic)| Create a new user_topic|
|[PATCH or PUT /user_topics/:id](#patch-user_topic)| Update a user_topic|
|[DELETE /user_topics/:id](#delete-user_topic)| Delete a user_topic|

## GET /user_topics

List all user_topics.

### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/user_topics```


## GET /user_topics/:id

Get a user_topic by its ID

### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/user_topics/1```


## POST /user_topics

Create a new user_topic

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user_topic[:qa_topic_id]```|required|integer|ID of the topic|

### Example Request

```curl -X POST https://api.speaken.com/api/v1/qa/user_topics```


## PATCH|PUT /user_topics/:id

Update a user_topic

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user_topic[:qa_topic_id]```|required|integer|ID of the topic|

### Example Request

```curl -X PATCH https://api.speaken.com/api/v1/qa/user_topics/1```


## DELETE /user_topics/:id

Delete a user_topic.

### Example Request

```curl -X DELETE https://api.speaken.com/api/v1/qa/user_topics/1```
