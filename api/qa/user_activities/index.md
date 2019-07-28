
|Endpoint|Description|
|--------|-----------|
|[GET /user_activities](#get-user_activity)| List all user_activities|
|[POST /user_activities](#create-user_activity)| Create a new user_activity|
|[PATCH or PUT /user_activities/:id](#patch-user_activity)| Update a user_activity|

## GET /user_activities

List all user user_activities.

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```by_activity```|not required|boolean|Filter by an activity type. Can be writing,word_picking,flashcard,pronunciation|
|```topic_id```|not required|number|Filter user_activities by topic_id|
|```skill_id```|not required|number|Filter user_activities by skill_id|
|```completed```|not required|number|Only show completed user_activities|
|```activity_id```|not required|number|Only show user_activities corresponding to this activity_id|


### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/user_activities?by_activity=flashcard&topic_id=1&skill_id=1&activity_id=1&completed=true```


## POST /user_activities

Create a new user_activity.

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```size```|not required|number|Query Parameter. If used, it will automatically create LemmaUserActivityType and UserActivityItem for the activity_type|
|```user_activity[:qa_activity_id]```|required|string|Id of the qa_activity|
|```user_activity[:started_at]```|required|datetime|Date value when the user_activity has started|
|```user_activity[:ended_at]```|required|datetime|Date value when the user_activity has ended|
|```user_activity[:cefr_level]```|required|string|CEFR level.|
|```user_activity[:user_input]```|required|string|Value of what the user has entered|
|```user_activity[:article_id]```|not required|integer|Id of the article. Used only for word_picking activity type|
|```user_activity[:qa_user_activity_items_attributes][:qa_lemma_id]```|required|number|Id of the lemma|
|```user_activity[:qa_user_activity_items_attributes][:is_right]```|required|boolean|Is the value correct|
|```user_activity[:qa_user_activity_errors_attributes][:type]```|required|string|Error type|
|```user_activity[:qa_user_activity_errors_attributes][:body]```|required|string|Text value of the error|
|```user_activity[:qa_activity_attributes][:subject]```|required|string|Activity subject|
|```user_activity[:qa_activity_attributes][:name]```|required|string|Activity name|
|```user_activity[:qa_activity_attributes][:qa_activity_step_id]```|required|number|ID of the activity_step|
|```user_activity[:qa_activity_attributes][:type]```|required|string|Activity type. Can be writing,word_picking,flashcard,pronunciation|
|```user_activity[:qa_activity_attributes][:activity_child_id]```|not required|number|ID of another activity|
|```user_activity[:qa_activity_attributes][:level_required]```|required|string|Minimum level required for this activity|
|```user_activity[:qa_activity_attributes][:qa_activity_topic_attributes][:qa_topic_id]```|required|Activity's topic|
|```user_activity[:qa_activity_attributes][:qa_activity_skills_attributes][:qa_skill_id]```|required|number|Activity's skill|

### Example Request

```curl -X POST https://api.speaken.com/v1/user_activities```


## PATCH|PUT /user_activities/:id

Update a new user_activity. (started_at can't be edited)

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user_activity[:qa_activity_id]```|required|string|Id of the qa_activity|
|```user_activity[:ended_at]```|required|datetime|Date value when the user_activity has ended|
|```user_activity[:cefr_level]```|required|string|CEFR level.|
|```user_activity[:user_input]```|required|string|Value of what the user has entered|
|```user_activity[:article_id]```|not required|integer|Id of the article. Used only for word_picking activity type|
|```user_activity[:qa_user_activity_items_attributes][:qa_lemma_id]```|required|number|Id of the lemma|
|```user_activity[:qa_user_activity_items_attributes][:is_right]```|required|boolean|Is the value correct|
|```user_activity[:qa_user_activity_errors_attributes][:type]```|required|string|Error type|
|```user_activity[:qa_user_activity_errors_attributes][:body]```|required|string|Text value of the error|
|```user_activity[:qa_activity_attributes][:subject]```|required|string|Activity subject|
|```user_activity[:qa_activity_attributes][:name]```|required|string|Activity name|
|```user_activity[:qa_activity_attributes][:qa_activity_step_id]```|required|number|ID of the activity_step|
|```user_activity[:qa_activity_attributes][:type]```|required|string|Activity type. Can be writing,word_picking,flashcard,pronunciation|
|```user_activity[:qa_activity_attributes][:activity_child_id]```|not required|number|ID of another activity|
|```user_activity[:qa_activity_attributes][:level_required]```|required|string|Minimum level required for this activity|
|```user_activity[:qa_activity_attributes][:qa_activity_topic_attributes][:qa_topic_id]```|required|Activity's topic|
|```user_activity[:qa_activity_attributes][:qa_activity_skills_attributes][:qa_skill_id]```|required|number|Activity's skill|

### Example Request

```curl -X PATCH https://api.speaken.com/v1/user_activities/1```
