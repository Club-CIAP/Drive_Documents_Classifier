# 📄 Intelligent Document Classifier with n8n & AI

## Overview 📋

This project is an intelligent automation system that analyzes the content of new documents and automatically organizes them into a predefined folder structure, eliminating the need for manual classification. Built with n8n, it transforms a simple Google Drive folder into a smart inbox that leverages AI to categorize and route documents.

## How It Works

### Architecture and Workflow ⚙️

- **n8n**: Workflow orchestration and automation engine
- **Google Drive**: Cloud storage trigger and file management
- **Google Gemini (AI)**: Natural language processing for document classification
- **Discord**: Real-time notifications for successful classifications
- **Extract from File**: Text extraction from various document formats

### Core Processes 🧠

1. **File Detection**: Monitors the `[INBOX]` folder for new document uploads
2. **Content Extraction**: Downloads and extracts text content from documents
3. **AI Classification**: Sends content to Google Gemini with a clear prompt to classify into predefined categories
4. **Smart Routing**: Uses conditional logic (Switch node) to move files to the correct destination folder
5. **Notification**: Sends confirmation to Discord when classification is complete

### Workflow Structure

The system follows this automated pipeline:
```
Google Drive Trigger → Download File → Extract Text → Wait → AI Classification → Switch Logic → Move to Category Folder → Discord Notification
```

### Classification Categories

Documents are automatically organized into four categories:

- **Académico** (Academic)
- **Administrativo** (Administrative)
- **Finanza** (Finance)
- **Otros** (Others)

## Key Benefits ✅

- **Complete automation** of document organization with zero manual intervention
- **AI-powered classification** using state-of-the-art language models
- **Real-time processing** - documents are classified immediately upon upload
- **Instant notifications** keep teams informed of document processing
- **Scalable solution** using free-tier services and cloud infrastructure

## Use Cases 💼

- Automatic organization of business documents (invoices, contracts, reports)
- Academic paper classification for research teams
- Administrative document routing in organizations
- Smart inbox system for any document management workflow

## Requirements 👨‍💻

- **n8n** instance (self-hosted or n8n Cloud free plan)
- **Google Drive** account with API credentials
- **Google Gemini API** key (60 requests/minute free tier)
- **Discord Webhook** for notifications
- Predefined folder structure in Google Drive

## Technical Skills Learned 🎓

- **Workflow Automation**: Mastering logic and step-by-step process construction in n8n
- **API Integration**: Seamless connection between multiple cloud services
- **Applied Artificial Intelligence**: Practical use of large language models for real-world problems
- **Prompt Engineering**: Designing clear and efficient instructions for AI task execution
- **Cloud File Management**: Programmatic manipulation of files and folders
- **Conditional Logic**: Implementing business rules and decision-making based on AI output

## Project Configuration

### AI Prompt Design

The system uses a carefully crafted prompt to ensure accurate classification:
```
Clasifica este texto en UNA palabra: Académico, Administrativo, Finanza, Otros. 
Responde solo con la palabra.
Texto: [document content]
```

This prompt engineering approach ensures:
- Single-word responses for reliable parsing
- Clear category boundaries
- Consistent classification results


## Authors 👥

**Grupo 7 - ESPOL**
- Team Members: [George Giler, Alan Ureta y Paulette Maldonado]
- Institution: Escuela Superior Politécnica del Litoral
- Mentor: Johnny Zavala

---

## Getting Started

1. Clone the workflow JSON from `grupo7.json`
2. Import into your n8n instance
3. Configure credentials for Google Drive, Gemini API, and Discord
4. Set up your folder structure in Google Drive
5. Activate the workflow and start uploading documents!

## Free Tools Used 🆓

- **n8n**: Free cloud plan or self-hosted version
- **Google Gemini**: 60 requests/minute free tier
- **Discord**: Free webhooks for notifications
- **Google Drive**: Standard free storage tier

---
