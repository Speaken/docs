|Endpoint|Description|
|--------|-----------|
|[GET /events](#get-usersme)| List all user events|

## GET /events

List all user events. Event type (object_type) can be:
- Lesson (You have received a new request for a lesson)
- Mailboxer::Message (You have received a new message)
- Review (You have a pending review)

### Example Request

```curl -X GET https://api.speaken.com/v1/events```
