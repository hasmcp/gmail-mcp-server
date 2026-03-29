# gmail

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

**Base URL:** `https://gmail.googleapis.com/gmail/v1`

**OAuth2:** ✅ Enabled

**Documentation:** [https://developers.google.com/workspace/gmail/api/guides](https://developers.google.com/workspace/gmail/api/guides)

## Tools (2)

- [sendEmail](tools/send-email.md) — Send new email or reply to thread
- [searchEmails](tools/search-emails.md) — Search for emails. Use 'q' for query (e.g. 'from:alice')

