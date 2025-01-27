# Google Sheets to Gmail Notification Workflow

## Overview
This is a simple **n8n** workflow that automates the process of sending email notifications via **Gmail** when a new row is added to a **Google Sheet**.

### Workflow Details:
1. **Trigger**: 
   The workflow is triggered whenever a new row is added to a Google Sheet.
   
2. **Action**:
   The workflow sends an email notification using **Gmail**, informing the user about the new entry in the sheet.

### Workflow File
The core workflow file is `workflow.json`. This file contains the configuration and nodes needed to set up the workflow in **n8n**.

### Steps to Set Up:
To run this workflow, follow these steps:

#### 1. **Set Up Google Sheets Credentials**:
   - Go to [Google Cloud Console](https://console.developers.google.com/).
   - Create a project and enable the **Google Sheets API** and **Google Drive API**.
   - Download the **OAuth2 credentials JSON file** and upload it to n8n in the **Google Sheets credentials** section.

#### 2. **Set Up Gmail Credentials**:
   - In the same project in the Google Cloud Console, enable the **Gmail API**.
   - Create OAuth2 credentials (OAuth client ID) and download the credentials file for Gmail.
   - Upload this file to n8n in the **Gmail credentials** section.

#### 3. **Upload `workflow.json` in n8n**:
   - After configuring your credentials, upload the `workflow.json` file in the **n8n UI** under the **Import Workflow** section.

#### 4. **Test the Workflow**:
   - Add a new row to your Google Sheet.
   - The workflow will trigger and send an email to the specified recipient.

### Requirements:
- n8n instance (self-hosted or cloud-based).
- Google Sheets and Gmail API credentials.

### Notes:
- Replace `"your-google-sheet-id"` with the actual ID of your Google Sheet.
- Configure the email recipient in the "Send Email" node to a valid email address.
