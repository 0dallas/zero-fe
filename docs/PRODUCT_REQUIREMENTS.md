# Product Requirements

## Overview

This application is an Enterprise AI Platform.

Users can chat with LLMs.

Users can upload documents.

Users can configure connectors.

Users can manage conversations.

Users can evaluate responses.

---

## Authentication

The application requires authentication.

Unauthenticated users cannot access the application.

Authentication uses JWT provided by the FastAPI backend.

Features:

- Login

- Logout

- Refresh Token

- Forgot Password (future)

---

## Dashboard

After login, users enter the dashboard.

Dashboard contains:

- Sidebar

- Main Content

- User Menu

---

## Chat

Users can:

- Create conversation

- Rename conversation

- Delete conversation

- Ask questions

- Receive streaming responses

- Stop generation

- Regenerate answer

---

## Documents

Users can:

- Upload PDF

- Upload DOCX

- Upload TXT

- Delete documents

- View ingestion status

---

## Connectors

Users can manage:

- Jira

- Confluence

- SharePoint

- GitHub

- Slack

- Google Drive

---

## User Settings

Users can:

- Change theme

- Configure language

- Configure AI model

- Configure temperature

- Configure retrieval parameters

---

## Administration

Future module.
