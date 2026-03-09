# searchEmails

Search for emails. Use 'q' for query (e.g. 'from:alice')

## API Details

- **Method:** `GET`
- **Endpoint:** `https://gmail.googleapis.com/gmail/v1/users/me/messages`

### Query Arguments

```json
{
  "properties": {
    "maxResults": {
      "description": "Maximum number of messages to return. This field defaults to 100. The maximum allowed value for this field is 500. Recommended value is 10.",
      "type": "number"
    },
    "q": {
      "description": "The search query string. (e.g., 'from:alice')",
      "type": "string"
    }
  },
  "required": [
    "q"
  ],
  "type": "object"
}
```

## Required Variables

- `GMAIL_GOOGLEAPIS_COM_ACCESS_TOKEN`

## Headers

- `Authorization: Bearer ${GMAIL_GOOGLEAPIS_COM_ACCESS_TOKEN}`

