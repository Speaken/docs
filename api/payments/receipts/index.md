|Endpoint|Description|
|--------|-----------|
|[POST /receipts](#post-receipts)| Create a receipt|

## POST /receipts

Create a new receipt

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```receipt[:token]```|required|string|Token returned by apple to be validated|
|```receipt[:provider]```|not required|string|Token provider value (Apple or Android) - default to Apple|


### Example Request

```curl -X POST https://api.speaken.com/v1/payment/receipts```
