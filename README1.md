#  YouTube Shorts Automation with n8n

An end-to-end automation workflow that generates and publishes YouTube Shorts automatically using n8n.

## What it does

This workflow automates:

Google Sheets
↓
AI Script Generation
↓
Text/Content Processing
↓
Creatomate Video Generation
↓
Video Rendering
↓
Google Drive
↓
YouTube Upload
↓
Google Sheets Update

## 🛠️ Technologies

- n8n
- Google Sheets API
- Google Drive API
- Creatomate API
- YouTube Data API
- OpenRouter / LLM
- JavaScript
- REST APIs

## 🔄 Workflow

The workflow:

1. Reads content from Google Sheets
2. Generates the required content using AI
3. Sends the content to Creatomate
4. Waits for video rendering
5. Checks the rendering status
6. Downloads the generated video
7. Uploads the video to YouTube
8. Updates the Google Sheet

##  Workflow Preview

Add a screenshot of the complete n8n workflow here.

##  Demo

Live automation environment:

> The n8n editor is kept private. A public demo/screenshot is provided instead.

##  Security

API keys, OAuth credentials, tokens and private workflow credentials are **not included** in this repository.

##  Author

**Akash Patil**

GitHub: https://github.com/akashpatil6294
