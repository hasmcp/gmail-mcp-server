# gmail

# Gmail MCP Server

## Search emails

You can use standard Gmail search operators to refine your results. You can combine multiple filters by adding space after the filter applied. 
* `from:amy@example.com`: Find emails sent from a specific person.
* `subject:dinner`: Find emails with "dinner" in the subject line.
* `after:2024/01/01 before:2024/02/01`: Find emails received in January 2024.
* `in:sent`: Search only messages in the Sent folder.
* `is:unread`: Find unread messages.
* `"exact phrase"`: Search for an exact phrase

## Read email content

Use the messageId coming from the search results.

## Send email

Send only the available attributes in your request. Do not forget to set any required attribute. While sending email `from` attribute should be asked to user if not known. At worst case don't send the `from` attribute.

## Providers

### [gmail](gmail)

Gmail provider is using Gmail API to search, read and send emails using Gmail API. 

To use this provider, please obtain OAuth2 ClientID and Client Secret by following the steps below:


1. **Create a Project**:
    - Go to the https://console.cloud.google.com/.
    - Create a new project named "HasMCP Gmail".

2. **Enable Gmail API**:
    - Navigate to **APIs & Services > Library**.
    - Search for "Gmail API" and click **Enable**.

3. **Configure Consent Screen**:
    - Go to **APIs & Services > OAuth consent screen**.
    - Select **External** (unless using a Workspace org) and click **Create**.
    - Enter an App Name (e.g., "HasMCP") and Support Email.
    - **Important**: Add the following **Scopes**:
      - `https://www.googleapis.com/auth/gmail.readonly`
      - `https://www.googleapis.com/auth/gmail.compose`
    - Add your own email address as a **Test User**.

4. **Create Credentials**:
    - Go to **APIs & Services > Credentials**.
    - Click **Create Credentials > OAuth client ID**.
    - Select **Web application**.
    - **Authorized Redirect URIs**: Enter `https://app.hasmcp.com/oauth2/callback` (Confirm this URI in your HasMCP Provider settings).
    - Click **Create**.
    - **Copy the Client ID and Client Secret**.

More details are available in: https://docs.hasmcp.com/tutorials/gmail-mcp-server

#### Tools (3)

- [sendEmail](gmail/tools/send-email.md) — Send new email or reply to thread
- [searchEmails](gmail/tools/search-emails.md) — Search for emails. Use 'q' for query (e.g. 'from:alice')
- [readEmailSnippet](gmail/tools/read-email-snippet.md) — Read initial part of the email content along with email headers.

