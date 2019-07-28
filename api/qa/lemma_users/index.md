|Endpoint|Description|
|--------|-----------|
|[GET /lemma_users](#get-lemma_users)| List all user lemmas|
|[PATCH or PUT /lemma_users/:id](#patch-lemma_users)| Update a user lemma|
|[DELETE /lemma_users/:id](#delete-lemma_users)| Delete a user lemma|

## GET /lemma_users

List all lemmas for the current user

### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/lemma_users```


## PATCH|PUT /lemma_users/:id

Update a lemma (for the current user only)

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lemma_user[:context]```|required|string|Update the context for this lemma|

### Example Request

```curl -X PATCH https://api.speaken.com/api/v1/qa/lemma_users/1```


## DELETE /lemma_users/:id

Delete a lemma (for the current user only)

### Example Request

```curl -X DELETE https://api.speaken.com/api/v1/qa/lemma_users/1```

