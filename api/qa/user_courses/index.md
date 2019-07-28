
|Endpoint|Description|
|--------|-----------|
|[GET /user_courses](#get-user_course)| List all courses for the current user|
|[POST /user_courses](#create-user_course)| Create a new course for the current user|
|[PATCH or PUT /user_courses/:id](#patch-user_course)| Update a course for the current user|
|[DELETE /user_courses/:id](#delete-user_course)| Delete a course for the current_user|

## GET /user_courses

List all user_courses.

### Example Request

```curl -X GET https://api.speaken.com/api/v1/qa/user_courses```


    params.require(:user_course).permit(:qa_skill_id, :qa_course_id, :qa_topic_id, :confirmed)

## POST /user_courses

Create a new user_course

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user_course[:qa_skill_id]```|required|integer|ID of the skill|
|```user_course[:qa_course_id]```|required|integer|ID of the course|
|```user_course[:qa_topic_id]```|required|integer|ID of the topic|
|```user_course[:confirmed]```|not required|boolean|Is the course confirmed|

### Example Request

```curl -X POST https://api.speaken.com/v1/user_courses```


## PATCH|PUT /user_courses/:id

Update a user_course

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```user_course[:qa_skill_id]```|required|integer|ID of the skill|
|```user_course[:qa_course_id]```|required|integer|ID of the course|
|```user_course[:qa_topic_id]```|required|integer|ID of the topic|
|```user_course[:confirmed]```|not required|boolean|Is the course confirmed|


### Example Request

```curl -X PATCH https://api.speaken.com/v1/user_courses/1```


## DELETE /user_courses/:id

Delete a user_course.

### Example Request

```curl -X DELETE https://api.speaken.com/v1/user_courses/1```

