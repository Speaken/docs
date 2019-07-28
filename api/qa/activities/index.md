|Endpoint|Description|
|--------|-----------|
|[GET /activities](#get-activities)| List all user activities|
|[GET /activities/:id](#get-activity)| Get a specific activity|

## GET /activities

List all user activities.

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```:by_activity```|not required|string|Filter activities by an activity type|
|```:skill_id```|not required|integer|Filter activities by a skill id|
|```:topic_id```|not required|integer|Filter activities by a topic id|


### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/activities```


## Get /activities/:id

Get a specific activity

### Example Request

```curl -X POST https://api.speaken.com/api/v1/qa/activities/1```
