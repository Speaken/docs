|Endpoint|Description|
|--------|-----------|
|[POST /receipts](#post-receipts)| Create a receipt|

## POST /receipts

Create a new receipt

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```receipt[:token]```|required|string|Token returned by apple to be validated|


### Example Request

```curl -X POST https://api.speaken.com/v1/payment/receipts```
