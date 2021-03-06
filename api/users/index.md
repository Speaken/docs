|Endpoint|Description|
|--------|-----------|
|[GET /users](#get-usersme)| List all teachers |
|[POST /users](#get-usersme)| Create a new user account |
|[GET /users/:id](#get-usersme)| Get user informations |
|[GET /users/me](#get-usersme)| Get authenticated user informations |
|[PATCH,PUT /users/:id](#get-usersme)| Update authenticated user|
|[GET /users/:user_id/reviews](#put-usersme)| List all reviews for a user |
|[GET /users/:user_id/availabilities](#put-usersme)| List all user availabilities |
|[POST /users/:user_id/availabilities](#put-usersme)| Add a new availability |
|[POST /users/:user_id/followers](#put-usersme)| Follow a user |
|[DELETE /users/:user_id/followers](#put-usersme)| Unfollow a user |
|[POST /users/:user_id/favorite_tutors](#post-favorite)| Favorite a tutor |
|[DELETE /users/:user_id/favorite_tutors](#delete-favorite)| Unfavorite a tutor |
|[POST /users/:user_id/recommended_tutors](#post-favorite)| Add a recommended tutor |
|[DELETE /users/:user_id/recommended_tutor_tutors](#delete-favorite)| Delete a recommended tutor |
|[GET /users/email/resend_confirmation](#resend-confirmation-email)| Resend confirmation email |

resend_confirmation_email

## POST /oauth/token

Log in user

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```username```|required|string|User's email|
|```password```|required|string|User's password|
|```grant_type```|required|string|Value: **password**|


### Example Request

```curl -X POST https://api.speaken.com/v1/oauth/token```

## GET /users

List all teachers

### Example Request

```curl -X GET https://api.speaken.com/v1/users```


## POST /users

Create a new user account

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```first_name```|required|string|User's first name|
|```last_name```|required|string|User's last name|
|```gender```|required|string|User's gender Either **male** or **female**|
|```email```|required|string|User's email|
|```password```|required|string|User's password|
|```birthday```|not required|date|User's birthday in ```YYYY-MM-DD``` format|
|```location```|not required|string|User's place|
|```latitude```|not required|string|User's latitude|
|```longitude```|not required|string|User's longitude|
|```remote_avatar_url```|not required|string|User's avatar url|
|```remote_background_url```|not required|string|User's background image url|
|```timezone```|not required|string|User's timezone|
|```phone```|not required|string|User's phone|
|```bio```|not required|string|User's bio|
|```invited_by_token```|not required|string|User's invitation token|
|```goals```|not required|string|User's goals|
|```accepted_lesson_types```|not required|string|User's accepted lesson types|
|```interests```|not required|string|User's interests|
|```user_languages_attributes```|not required|string|User languages|
|```settings```|not required|string|User settings |

### Example Request

```curl -X POST https://api.speaken.com/v1/users```


## GET /users/:id

Get user informations

### Example Request

```curl -X GET https://api.speaken.com/v1/users/1```


## GET /users/me

Get authenticated user informations

### Example Request

```curl -X GET https://api.speaken.com/v1/users/me```


## PATCH|PUT /users/:id

Update user informations

### Example Request

```curl -X PUT https://api.speaken.com/v1/users/1```


## GET /users/:user_id/reviews

List all reviews for a user

### Example Request

```curl -X GET https://api.speaken.com/v1/users/1/reviews```


## GET /users/:user_id/availabilities

List all user availabilities

### Example Request

```curl -X GET https://api.speaken.com/v1/users/1/availabilities```


## POST /users/:user_id/availabilities

Add a new availability

### Example Request

```curl -X POST https://api.speaken.com/v1/users/1/availabilities```


## POST /users/:user_id/followers

Follow a user

### Example Request

```curl -X POST https://api.speaken.com/v1/users/1/followers```


## DELETE /users/:user_id/followers


Unfollow a user

### Example Request

```curl -X DELETE https://api.speaken.com/v1/users/1/followers```

## POST /users/:user_id/favorite_tutors

Favorite a tutor

### Example Request

```curl -X POST https://api.speaken.com/v1/users/1/favorite_tutors```


## DELETE /users/:user_id/favorite_tutors


Unfavorite a tutor
### Example Request

```curl -X DELETE https://api.speaken.com/v1/users/1/favorite_tutors```


## POST /users/:user_id/recommended_tutors

Add a recommended tutor

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```tutor_id```|required|number|ID of the tutor we want to set as recommended for the user_id|

### Example Request

```curl -X POST -d '{"tutor_id":"2"}' https://api.speaken.com/v1/users/1/recommended_tutors```


## DELETE /users/:user_id/recommended_tutors


Delete a recommended a tutor

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```tutor_id```|required|number|ID of the tutor we want to set as recommended for the user_id|

### Example Request

```curl -X DELETE -d '{"tutor_id":"2"}' https://api.speaken.com/v1/users/1/recommended_tutors```

## GET /users/email/resend_confirmation

Resend account confirmation email

### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```email```|required|string|User's email|

### Example Request

```curl -X GET https://api.speaken.com/v1/users/email/resend_confirmation?email=XXX```
