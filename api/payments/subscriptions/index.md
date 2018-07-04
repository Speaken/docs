|Endpoint|Description|
|--------|-----------|
|[POST /payment/subscriptions](#post-subscriptions)| Create a new web subscription|
|[GET /payment/subscriptions/:id](#get-subscription)| Show user web subscription|
|[PUT /payment/subscriptions/:id](#update-subscription)| Update user web subscription|
|[DELETE /payment/subscriptions/:id](#delete-subscription)| Delete user web subscription|

## POST /payment/subscriptions

Create a new web (stripe) subscription

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```subscription[:plan_id]```|required|integer|ID of the Plan|


### Example Request

```curl -X POST https://api.speaken.com/v1/payment/subscriptions```



## GET /payment/subscriptions/:id

Show details about user web (stripe) subscription

### Example Request

```curl https://api.speaken.com/v1/payment/subscriptions/1```


## PUT /payment/subscriptions/:id

Update user web (stripe) subscription

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```subscription[:plan_id]```|required|integer|ID of the new plan|


### Example Request

```curl -X PUT https://api.speaken.com/v1/payment/subscriptions/1```


## DELETE /payment/subscriptions/:id

Delete user web (stripe) subscription

### Example Request

```curl -X DELETE https://api.speaken.com/v1/payment/subscriptions/1```
