# n8n-automations
This is my first automation project built using n8n. It demonstrates a complete "Lead-to-Database" pipeline that includes data validation, custom JavaScript formatting, and conditional routing.



📋 Project Overview
The goal of this workflow is to take incoming form submissions and automatically organize them into different Google Sheets based on the user's age. It also ensures the submission timestamp is human-readable before being saved.




🛠️ How it Works
Trigger (Webhook/Form): Receives data including Name, Age, Phone, and a default submittedAt timestamp.
Date Formatting (Code Node): * Uses a custom JavaScript snippet to transform the ISO date (e.g., 2026-03-23T17:57:24) into a clean, readable format: YYYY/MM/DD H:MMpm.
Adjusts the time specifically for the Africa/Casablanca timezone.
Conditional Routing (Switch Node):
Route A: If Age >= 18, the data is sent to the "Greater than 18" Google Sheet.
Route B: If Age < 18, the data is sent to the "Less than 18" Google Sheet.
Database Integration: Saves the cleaned data into the appropriate Google Sheets using a Service Account for secure authentication.



🧪 Technical Skills Demonstrated

Workflow Logic: Using Switch nodes to handle conditional data paths.
JavaScript: Overwriting JSON objects and using Intl.DateTimeFormat for localization.
API Integration: Connecting to Google Cloud Console and managing Service Account permissions.
Data Transformation: Moving data from a raw "Trigger" state to a "Production-ready" spreadsheet format.



🚀 How to Import this Workflow

1-Download the lead-capture-workflow.json file from this repository.
2-Open your n8n instance and create a new workflow.
3-Click Menu > Import from File and select the downloaded JSON.
4-Configure your own Google Sheets Credentials within the nodes to start capturing leads!




