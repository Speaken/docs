
|Endpoint|Description|
|--------|-----------|
|[GET /lemma_user_activity_types](#get-lemma_user_activity_types)| List all lemma user activity types|
|[POST /lemma_user_activity_types](#create-lemma_user_activity_types)| Create a new lemma_user_activity_type|
|[PATCH or PUT /lemma_user_activity_types/:id](#patch-lemma_user_activity_types)| Update a lemma_user_activity_types|
|[DELETE /lemma_user_activity_types/:id](#delete-lemma_user_activity_types)| Delete a lemma user activity type|

## GET /lemma_user_activity_types

List all lemma user activity type

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```only_count```|not required|boolean|Returns only the number of lemma user, group by activity type|


### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/lemma_user_activity_types?only_count=true```


## POST /lemma_user_activity_types

Create a new lemma_user_activity_type


### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lemma_user_activity_type[:qa_lemma_user_id]```|required|integer|qa_lemma_user_id|
|```lemma_user_activity_type[:activity_type]```|required|string|Type of activity. Can be writing,word_picking,flashcard,pronunciation |
|```lemma_user_activity_type[:due_date]```|required|datetime|due_date for the lemma_user_activity_type|
|```lemma_user_activity_type[:revision_count]```|required|number|Revision count for the lemma_user_activity_type|

### Example Request

```curl -X POST https://api.speaken.com/api/v1/qa/lemma_user_activity_types```


## PATCH|PUT /lemma_user_activity_types/:id

Update a lemma_user_activity_type

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lemma_user_activity_type[:qa_lemma_user_id]```|required|integer|qa_lemma_user_id|
|```lemma_user_activity_type[:activity_type]```|required|string|Type of activity. Can be writing,word_picking,flashcard,pronunciation |
|```lemma_user_activity_type[:due_date]```|required|datetime|due_date for the lemma_user_activity_type|
|```lemma_user_activity_type[:revision_count]```|required|number|Revision count for the lemma_user_activity_type|

### Example Request

```curl -X PATCH https://api.speaken.com/api/v1/qa/lemma_user_activity_types/1```


## DELETE /lemma_user_activity_types/:id

Delete a lemma_user_activity_type.

### Example Request

```curl -X DELETE https://api.speaken.com/api/v1/qa/lemma_user_activity_types/1```

