# AI Client Onboarding & Document Automation

An AI-powered client onboarding solution built using **n8n, Google Gemini, Gmail, and Google Drive**. This project automates client information extraction and generates structured onboarding documents through an integrated AI workflow.

## Project Overview

Client onboarding involves reviewing emails, collecting business information, organizing client details, and preparing documents for meetings and business assessments.

This project focuses on simplifying these repetitive tasks through AI-powered workflow automation.

The system receives client emails through Gmail, uses Google Gemini to extract relevant business information, creates a client folder in Google Drive, and generates three structured documents:

- Client Profile
- Clarity Call Guide
- Thesis Readiness Diagnostic

## Project Objectives

- Automate the initial client onboarding process.
- Extract important business information from incoming emails.
- Reduce repetitive manual document preparation.
- Organize client information in Google Drive.
- Generate structured onboarding documents using AI.
- Improve consistency in client information and onboarding preparation.

## Technologies Used

| Technology | Purpose |
|---|---|
| n8n | Workflow automation and orchestration |
| Google Gemini | AI-powered information extraction and document generation |
| Gmail | Receiving and retrieving client emails |
| Google Drive | Creating client folders and storing documents |
| LLM Chains | Processing information and generating structured outputs |
| Prompt Engineering | Guiding AI responses and output structure |

## Workflow Architecture

The automation follows this sequence:

```text
Gmail Trigger
     |
     v
Get a Message
     |
     v
Basic LLM Chain
     |
     v
Google Gemini
     |
     v
Extract Client Information
     |
     v
Create Google Drive Folder
     |
     v
Generate Client Profile
     |
     v
Convert to File
     |
     v
Upload Client Profile
     |
     v
Generate Clarity Call Guide
     |
     v
Convert to File
     |
     v
Upload Clarity Call Guide
     |
     v
Generate Thesis Readiness Diagnostic
     |
     v
Convert to File
     |
     v
Upload Diagnostic Document
```

## How the Workflow Works

### 1. Gmail Integration

The workflow starts when a new email is received through the configured Gmail Trigger. The email content is then retrieved for AI processing.

### 2. AI-Powered Information Extraction

A Basic LLM Chain connected to Google Gemini analyzes the email and extracts structured client information, including:

- Client name
- Email address
- Company name
- Website
- Business type
- Business description
- Business goals
- Requirements
- Pain points
- Relevant details

The extraction prompt instructs the AI to use the information provided in the email rather than inventing missing details.

### 3. Automated Google Drive Folder Creation

The workflow creates a client folder in Google Drive to organize the generated onboarding documents.

### 4. Client Profile Generation

Google Gemini generates a structured client profile using the extracted information. The content is converted into a file and uploaded to Google Drive as `client.md`.

### 5. Clarity Call Guide Generation

The AI generates a clarity call guide containing relevant questions and discussion topics to help prepare for a client conversation.

The generated document is converted into a file and uploaded to Google Drive as `Clarity_Call_Guide.md`.

### 6. Thesis Readiness Diagnostic Generation

The workflow generates a business readiness diagnostic covering:

- Lead generation
- Sales processes
- Marketing automation
- Business operations
- Relevant questions and information gaps
- Suggested next steps

The diagnostic is converted into a file and uploaded to Google Drive.

## Key Features

- Automated Gmail-based onboarding trigger.
- AI-powered client information extraction.
- Google Gemini integration.
- Automated Google Drive folder creation.
- AI-generated client profiles.
- Automated clarity call preparation.
- Business readiness diagnostic generation.
- Automatic document conversion and upload.

## Challenges & Solutions

**Challenge: Accurate Information Extraction**

AI models may make assumptions or generate details that were not included in the original email.

**Solution:** Clear prompt instructions were added to ensure that the AI uses the information provided and avoids inventing missing details.

**Challenge: Generating Multiple Structured Documents**

Preparing different onboarding documents manually can involve repetitive work.

**Solution:** Separate Gemini-powered LLM Chains were used to generate the client profile, clarity call guide, and readiness diagnostic.

## Project Workflow Screenshot

The following screenshot presents the overall n8n workflow architecture, including Gmail integration, Google Gemini processing, Google Drive folder creation, and automated document generation.

![AI Client Onboarding Workflow Overview](screenshots/ai-client-onboarding-workflow-overview.png)

## Project Structure

```text
ai-client-onboarding-automation/
│
├── screenshots/
│   └── ai-client-onboarding-workflow-overview.png
│
├── workflow/
│   └── client-onboarding-workflow.json
│
└── README.md
```

## Project Status

**Development & Demo:** Developed and tested as an AI automation project during a software house internship. A demonstration was prepared and shared with the client for review.

**Deployment Status:** Live production deployment has not been confirmed.

## Skills Demonstrated

- AI Workflow Automation
- n8n Workflow Development
- Google Gemini Integration
- Gmail and Google Drive Integration
- Prompt Engineering
- LLM-Based Information Extraction
- Automated Document Generation
- Multi-Step Workflow Design
- Workflow Testing and Validation

## Author

**Muhammad**

Computer Science Graduate | AI Automation & Workflow Development

GitHub: [Muhammad6730](https://github.com/Muhammad6730)

---

*Building practical AI-powered automation solutions to simplify business processes and reduce repetitive tasks.*
