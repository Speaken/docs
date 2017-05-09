|Endpoint|Description|
|--------|-----------|
|[GET /conversations](#get-conversation)| List all user conversations|
|[POST /conversations](#create-conversation)| Create a new conversation|
|[PATCH or PUT /conversations/:id](#patch-conversation)| Mark a conversation as read|
|[DELETE /conversations/:id](#delete-conversation)| Delete a converation|
|[GET /conversations/:id/messages](#get-conversation-messages)| List all conversation messages|
|[POST /conversations/:id/messages](#post-conversation-messages)| Send a new message to a conversation|

## GET /conversations

List all user conversations.

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```conversation[:type]```|not required|string|Inbox by default. Can be inbox|sentbox|
|```conversation[:from]```|not required|datetime|Minimum date where the conversation has been created|
|```conversation[:to]```|not required|datetime|Maximum date where the conversation has been created|
|```conversation[:user_ids]```|not required|array|Array of user ids where the conversations is related to|


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

## GET /conversations/:id/messages

List all conversation messages.

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```conversation[:from_id]```|not required|integer|List conversations where id is superior to this value|
|```conversation[:to_id]```|not required|integer|List conversations where id is less than this value|


### Example Request

```curl -X GET https://api.speaken.com/v1/conversations/1/messages```


## POST /conversations/:id/messages

Reply to a conversation message

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```conversation[:body]```|required|string|Content of the message|

### Example Request

```curl -X POST https://api.speaken.com/v1/conversations/1/messages```


