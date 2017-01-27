|Endpoint|Description|
|--------|-----------|
|[GET /company/users](#get-users)| List all company users |
|[POST /company/users](#create-user)| Join a company by specifying an invitation token |
|[UPDATE /company/users/:id](#update-user)| Update a company user |
|[DELETE /company/users/:id](#delete-user)| Remove a user from a company |


## GET /company/users

Get all company users (manager only)

### Example Request

```curl -X GET https://api.speaken.com/v1/company/users```


## POST /company/users

Join a company by specifying an invitation token

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```invitation[:token]```|required|string|Invitation token|

### Example Request

```curl -X POST https://api.speaken.com/v1/company/users```


## POST /company/users/1

Update a company user (manager only)

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user[:credit]```|required|integer|Number of credit a manager want to assign to the user|

### Example Request

```curl -X PATCH https://api.speaken.com/v1/company/users/1```


## DELETE /company/users/:id

Delete a company user (manager only)

### Example Request

```curl -X DELETE https://api.speaken.com/v1/company/users/1```
