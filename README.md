# YouTube Shorts Automation with n8n

An automated workflow for generating and publishing YouTube Shorts using n8n. The workflow takes content from Google Sheets, generates the required script using an AI API, processes the content, creates a video through Creatomate, and publishes the finished video to YouTube.

## Demo

### Complete Workflow Execution

This video shows the complete workflow running from the initial Google Sheets input through video generation and YouTube upload.

[Watch the complete workflow execution](https://youtu.be/nT-FBpS2-1g)

### Workflow Walkthrough

This video provides a step-by-step view of the workflow and the individual stages involved in the automation.

[Watch the workflow walkthrough](https://youtu.be/x48uF1NvSZQ)

## Workflow Architecture

![Workflow Architecture]

The workflow follows this general pipeline:

```text
Google Sheets
      |
      v
Read Content
      |
      v
AI Script Generation
      |
      v
Content Processing / Translation
      |
      v
Creatomate Video Generation
      |
      v
Render Status Check
      |
      v
Download Generated Video
      |
      v
YouTube Upload

```

## How It Works

### 1. Google Sheets

The workflow reads the content and processing status from Google Sheets. This provides a simple way to manage the content that needs to be converted into videos.

### 2. AI Content Generation

The selected content is sent to an AI API to generate the script used in the Short.

### 3. Content Processing

The generated content is processed and translated according to the workflow configuration before being passed to the video generation stage.

### 4. Video Generation

The processed script and media information are sent to Creatomate, which generates the video using a predefined template.

### 5. Render Status

Video generation is asynchronous, so the workflow checks the render status before continuing. If the video is not ready, the workflow waits and checks again.

### 6. Video Download

Once the render is completed successfully, the generated video is retrieved and prepared for upload.

### 7. YouTube Upload

The generated video is uploaded to YouTube using the YouTube Data API.


## Technologies Used

- n8n
- Google Sheets
- Google Drive
- OpenRouter
- Creatomate
- YouTube Data API
- Google Translate
- JavaScript
- REST APIs

## Key Features

- End-to-end workflow automation
- AI-based script generation
- Google Sheets integration
- Automated translation
- Template-based video generation
- Asynchronous render-status checking
- Automated YouTube publishing
- Google Sheets status tracking
- API-based integration between multiple services

## Project Structure

```text
n8n-youtube-shorts-automation/
|
├── README.md
├── workflow-screenshot.png
└── demo/
    ├── full-workflow-demo
    └── workflow-walkthrough
```

The demonstration videos are hosted externally to keep the repository lightweight.

## Security

API keys, OAuth credentials, access tokens, and other sensitive information should not be committed to the repository.

The workflow shared publicly should use placeholders or n8n credentials instead of exposing actual API credentials.

## Future Improvements

- Automatic thumbnail generation
- Automatic title and description generation
- Hashtag generation
- Duplicate-content detection
- Improved retry and error handling
- YouTube scheduling
- Analytics collection
- Support for additional content sources

## Author

Akash Patil

Computer Science Engineering Student

GitHub: https://github.com/akashpatil6294
