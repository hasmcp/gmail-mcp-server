# readEmailSnippet

Read initial part of the email content along with email headers.

## API Details

- **Method:** `GET`
- **Endpoint:** `https://gmail.googleapis.com/gmail/v1/users/me/messages/{messageId}`

### Path Arguments

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "properties": {
    "messageId": {
      "description": "message id",
      "type": "string"
    }
  },
  "required": [
    "messageId"
  ],
  "type": "object"
}
```

## Required Variables

- `GMAIL_GOOGLEAPIS_COM_ACCESS_TOKEN`

## Headers

- `Authorization: Bearer ${GMAIL_GOOGLEAPIS_COM_ACCESS_TOKEN}`

