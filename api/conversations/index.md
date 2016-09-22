|Endpoint|Description|
|--------|-----------|
|[GET /conversations](#get-conversation)| List all user conversations|
|[POST /conversations](#create-conversation)| Create a new conversation|
|[PATCH|PUT /conversations/:id](#patch-conversation)| Mark a conversation as read|
|[DELETE /conversations/:id](#delete-conversation)| Delete a converation|

## GET /conversations

List all user conversations.

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```conversation[:type]```|not required|string|Inbox by default. Can be inbox|sentbox|
|```conversation[:from]```|not required|datetime|Minimum date where the conversation has been created|
|```conversation[:to]```|not required|datetime|Maximum date where the conversation has been created|


### Example Request

```curl -X GET https://api.speaken.com/v1/converations```


## POST /conversations

Create a new conversation

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```conversation[:user_id]```|required|integer|user_id of the user we want to start a conversation with|
|```conversation[:messages]```|required|array|Array of Message (String) to be sent in the conversation|

### Example Request

```curl -X POST https://api.speaken.com/v1/conversations```


## PATCH|PUT /conversations/:id

Mark a conversation as read|unread

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```read```|required|boolean|Value can be true or false|

### Example Request

```curl -X PATCH https://api.speaken.com/v1/conversations/1```


## DELETE /conversations/:id

Delete a conversation.

### Example Request

```curl -X DELETE https://api.speaken.com/v1/conversations/1```
