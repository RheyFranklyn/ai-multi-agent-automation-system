# Technical Documentation

## System Overview
This system is an AI multi-agent automation workflow built using n8n. It routes incoming requests into different AI agents (Support, Research, Productivity).

---

## Prerequisites

- n8n instance (cloud or local)
- Gemini or OpenAI API key
- Gmail OAuth2 credentials
- Google Sheets API access
- HTML to PDF API key

---

## Workflow Architecture

1. Webhook Trigger receives input
2. Normalize Input node standardizes data
3. AI Classifier (Gemini/OpenAI) categorizes request:
   - SUPPORT
   - RESEARCH
   - PRODUCTIVITY
4. Switch node routes request to correct branch

---

## Support Branch
- AI performs sentiment analysis
- AI categorizes issue (Billing / Technical / Feedback)
- Generates response
- Sends via Gmail
- Logs ticket in Google Sheets

---

## Research Branch
- AI generates structured research summary
- HTML report is created
- Converted to PDF
- Sent via Gmail

---

## Productivity Branch
- AI converts text into structured task list
- Generates formatted report
- Converts to PDF
- Sends via Gmail

---

## API Integrations

### Gemini/OpenAI
Used for classification and content generation.

### Gmail API
Used for sending automated responses.

### Google Sheets API
Used for logging support tickets and outputs.

### HTML to PDF API
Used for generating downloadable reports.

---

## Error Handling
- Invalid classification defaults to SUPPORT branch
- Missing input is handled via Normalize node

---

## How to Import Workflow
1. Open n8n
2. Click Import Workflow
3. Upload `workflow.json`
