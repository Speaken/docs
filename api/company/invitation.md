|Endpoint|Description|
|--------|-----------|
|[GET /company/invitations](#get-invitations)| List all company invitation |
|[POST /company/invitations](#create-invitation)| Create a new company invitation token |
|[DELETE /company/invitations/:id](#delete-invitation)| Delete a company invitation token |


## GET /company/invitations

Get all company invitations

### Example Request

```curl -X GET https://api.speaken.com/v1/company/invitations```


## POST /company/invitations

Create a new user account

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```invitation[:credit]```|required|integer|Number of credit you want to give to the invited users|
|```invitation[:max_used]```|required|integer|Maximum numbers of time the invitation token can be used|

### Example Request

```curl -X POST https://api.speaken.com/v1/company/invitations```


## DELETE /company/invitations/:id

Delete a company invitation token

### Example Request

```curl -X DELETE https://api.speaken.com/v1/company/invitations/1```
