# Privacy Policy — AI PDF Annotator

**Last updated: March 17, 2026**

## Overview

AI PDF Annotator is a Chrome extension that provides a built-in PDF reader with AI-powered annotation capabilities. This privacy policy explains how the extension handles user data.

## Data Collection

**We do not collect, store, or transmit any personal data to our servers.** The extension has no backend server, no analytics, no tracking, and no ads.

## Data Storage

All data is stored locally on your device using Chrome's built-in storage APIs:

- **API Keys** — Stored in `chrome.storage.local` on your device. Never sent anywhere except directly to the AI provider you configured (OpenAI, Anthropic, or your local server).
- **PDF Annotations** — Questions, AI responses, and screenshot thumbnails are saved per PDF document in `chrome.storage.local`.
- **Conversation History** — Chat history with AI is stored locally per document to enable follow-up questions.
- **User Preferences** — Theme, active AI provider, and model selections are stored locally.

## Third-Party AI Services

When you use the extension's AI features, the text or screenshots you select are sent directly from your browser to the AI provider you have configured:

- **OpenAI API** (api.openai.com) — if you choose OpenAI as your provider
- **Anthropic API** (api.anthropic.com) — if you choose Claude as your provider
- **Local AI servers** (localhost / 127.0.0.1) — if you use Ollama, LM Studio, or other local models
- **Custom endpoints** — any OpenAI-compatible API URL you configure

The extension sends requests directly from your browser to these services using your own API key. We do not proxy, log, or intercept these requests. Please refer to each provider's own privacy policy for how they handle your data.

## Permissions

The extension requests the following permissions, used solely for its core functionality:

| Permission | Purpose |
|---|---|
| `storage` / `unlimitedStorage` | Store annotations, settings, and API keys locally |
| `webRequest` | Detect PDF content-type headers for automatic interception |
| `webNavigation` | Detect navigation to PDF URLs |
| `tabs` | Redirect PDF tabs to the built-in reader |
| `declarativeNetRequest` | Modify CORS headers for localhost only, enabling local AI servers |
| `*://*/*` | Intercept PDF files from any website |
| `file:///*` | Open local PDF files |

## Data Sharing

We do not share any data with third parties. The only network requests made by the extension are:

1. AI API calls to the provider you configured (using your own API key)
2. PDF file downloads (the same URL your browser would fetch normally)

## Data Deletion

All extension data can be deleted by:

- Clicking "Clear chat" within the extension to remove conversation history for the current PDF
- Uninstalling the extension, which removes all stored data
- Clearing Chrome's extension storage via `chrome://settings/content/all`

## Children's Privacy

This extension is not directed at children under 13 and does not knowingly collect data from children.

## Changes to This Policy

We may update this privacy policy from time to time. Changes will be reflected in the "Last updated" date above.

## Contact

If you have questions about this privacy policy, please open an issue on our GitHub repository.
