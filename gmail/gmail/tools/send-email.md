# sendEmail

Send new email or reply to thread

## API Details

- **Method:** `POST`
- **Endpoint:** `https://gmail.googleapis.com/gmail/v1/users/me/messages/send`

### Request Body

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "properties": {
    "bcc": {
      "description": "List of BCC recipients",
      "items": {
        "format": "email",
        "type": "string"
      },
      "type": "array"
    },
    "body": {
      "description": "Email body content (used for text/plain or when htmlBody not provided)",
      "type": "string"
    },
    "cc": {
      "description": "List of CC recipients",
      "items": {
        "format": "email",
        "type": "string"
      },
      "type": "array"
    },
    "from": {
      "description": "Sender email address (e.g. sender@example.com)",
      "format": "email",
      "type": "string"
    },
    "htmlBody": {
      "description": "HTML version of the email body",
      "type": "string"
    },
    "inReplyTo": {
      "description": "Message ID being replied to",
      "type": "string"
    },
    "mimeType": {
      "default": "text/plain",
      "description": "Email content type",
      "enum": [
        "text/plain",
        "text/html",
        "multipart/alternative"
      ],
      "type": "string"
    },
    "subject": {
      "description": "Email subject",
      "type": "string"
    },
    "threadId": {
      "description": "Thread ID to reply to",
      "type": "string"
    },
    "to": {
      "description": "List of recipient email addresses",
      "items": {
        "format": "email",
        "type": "string"
      },
      "type": "array"
    }
  },
  "required": [
    "from",
    "to",
    "subject",
    "body"
  ],
  "title": "Email Schema",
  "type": "object"
}
```

## Required Variables

- `GMAIL_GOOGLEAPIS_COM_ACCESS_TOKEN`

## Headers

- `Authorization: Bearer ${GMAIL_GOOGLEAPIS_COM_ACCESS_TOKEN}`
- `Content-Type: application/json`

