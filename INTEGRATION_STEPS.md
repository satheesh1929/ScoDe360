
## Wait, I'm Getting an Error?

If you see an alert saying **"There was a problem sending your message"**, it is almost always because of **Permissions**.

### The Solution (Fixing the 403 Forbidden Error)

1.  Go back to your Google Apps Script tab.
2.  Click the blue **Deploy** button > **Manage deployments**.
3.  You will see your current deployment (likely named "Active" or similar).
    *   Click the **Pencil Icon (Edit)** next to "Configuration".
4.  Look at **Who has access**.
    *   It **MUST** say **"Anyone"**.
    *   If it says "Myself" or "Anyone with Google Account", **CHANGE IT TO "Anyone"**.
5.  Click **Deploy** (or generic "Done"/"Update").
    *   *Note: If you made changes, you might need to create a NEW deployment to be sure permissions update.*
    *   **Safest Way:** Click **Deploy** > **New deployment** > ensure "Who has access" is **Anyone** > Deploy.
    *   **Copy the NEW URL** if it changed, and update your `index.html`.

### Why does it need "Anyone" access?
Since your website visitors don't have access to your private Google account, the script must be publicly accessible to receive the data they send. Don't worry, they can only *add* data (append rows), they cannot read your spreadsheet.

### 📧 Changing the "From" Email Address
The confirmation email is sent by the **Google Account that owns the script**. 

*   **To send from `team.scode360@gmail.com`:** You **MUST** log in to Google as `team.scode360@gmail.com`, create the script, and deploy it from that account.
*   **To send from `satheesh1929@gmail.com`:** Deploy it from your personal account.

**Note:** The script now includes `replyTo: "team.scode360@gmail.com"`, so replies will always go to the team email regardless of the sender.
