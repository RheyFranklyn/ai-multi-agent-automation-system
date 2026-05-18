# AI Multi-Agent Business Automation System

## Overview

This project is an AI-powered automation workflow built using n8n that streamlines customer support, research generation, and productivity management.

The system uses AI intent classification to route incoming requests into specialized AI agents:

* Smart Support Triage Agent
* AI Research Assistant
* Productivity Task Generator

---

## Tools Used

| Tool              | Purpose                |
| ----------------- | ---------------------- |
| n8n               | Workflow orchestration |
| Gemini/OpenAI     | AI processing          |
| Gmail API         | Email automation       |
| Google Sheets API | Data logging           |
| HTML to PDF API   | PDF generation         |

---

## Features

* AI Intent Classification
* Smart Customer Support Triage
* Research PDF Report Generation
* Productivity Task Report Generation
* Automated Email Delivery
* Google Sheets Logging

---

## Workflow Architecture

![Workflow Diagram](screenshots/workflow.png)

---

## Installation

1. Import the provided n8n workflow JSON file
2. Configure API credentials
3. Configure Gmail OAuth
4. Configure Google Sheets access
5. Run the workflow

---

## Documentation

* Technical Documentation → `/documentation/technical-users.md`
* Non-Technical Documentation → `/documentation/non-technical-users.md`
