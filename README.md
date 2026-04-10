# n8n Automation Portfolio 🚀

A collection of production-ready n8n workflows demonstrating advanced automation pipelines, AI integrations, and secure data processing.

## 🛠️ Included Workflows

| Workflow                   | Key Features                                                            | Tech Stack                 |
| :------------------------- | :---------------------------------------------------------------------- | :------------------------- |
| **Lead Capture & Routing** | Form validation, Timezone conversion (Casablanca), Conditional routing. | JS, Google Sheets          |
| **Mistral AI OCR**         | Two-stage PDF processing, data extraction, and validation.              | Mistral AI, OCR API        |
| **Stability AI Gen**       | Text-to-image generation with automated cloud storage.                  | Stability AI, Google Drive |
| **LinkedIn Automation**    | Content generation from structured data (WIP).                          | Gemini 1.5 Flash, G-Sheets |

## 🧪 Technical Core

- **Data Transformation:** Custom JavaScript nodes for complex JSON manipulation and localization.
- **AI Orchestration:** Managing rate limits and context for Mistral, Stability, and Gemini models.
- **Security:** Zero-hardcoding policy. All sensitive data is managed via the n8n Credential Manager.
- **Cloud Integration:** Full integration with Google Cloud Console and Service Accounts.

---

## 🚀 Installation & Local Setup

To use these workflows in your own n8n instance, follow these steps:

### 1. Prerequisites

- **n8n installed** (Desktop app, Docker, or Cloud).
- **API Keys** for the services you intend to use (Mistral, Stability, or Google Cloud).

### 2. Import the Workflow

1. Clone this repository or download the specific `.json` file you want to use.
2. Open your n8n instance and click **New Workflow**.
3. Go to **Menu > Import from File** and select the `.json` file.

### 3. Configure Credentials (CRITICAL)

The workflows will import with "placeholder" credentials. To make them work:

1. Go to the **Credentials** tab in n8n.
2. Create new credentials for the required services (e.g., _Google Drive OAuth2_, _Header Auth_ for Mistral).
3. Open the red-flagged nodes in the workflow and select your newly created credentials from the dropdown.

### 4. Setup Environment Variables (Optional)

If you are using a self-hosted n8n instance and want to use a `.env` file, ensure your `N8N_BLOCK_ENV_VAR_ACCESS` is set to `false` in your environment config.
