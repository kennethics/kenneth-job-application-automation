
# Kenneth's Job Application Automation

An AI-powered job search and application assistant built with n8n that automatically discovers jobs, finds hiring contacts, drafts tailored applications, generates customized resumes, and keeps a complete application tracking system.

---

# Business Problem

Job seekers spend hours every week performing repetitive tasks:

* Searching job boards
* Tracking opportunities
* Researching hiring managers
* Writing application emails
* Tailoring resumes
* Managing application status

Most of this work is manual and time-consuming.

This workflow automates the entire process while keeping the user in control through an approval step before any application is submitted.

---

# Workflow Architecture

```text
Schedule Trigger
        │
        ▼
JSearch API
(Job Discovery)
        │
        ▼
Google Sheets
(Job Database)
        │
        ▼
AI Contact Finder
(Hunter.io)
        │
        ▼
AI Email Generator
(Groq)
        │
        ▼
WhatsApp Approval Request
(CallMeBot)
        │
        ▼
User Decision
    │         │
    ▼         ▼
Approve     Reject
    │
    ▼
AI Resume Tailoring
    │
    ▼
Google Docs
    │
    ▼
Gmail Send
    │
    ▼
Update Tracking Sheet
```

---

# Integrations Used

## JSearch API

Searches newly posted remote jobs matching target criteria.

## Google Sheets

Stores:

* Job opportunities
* Contact information
* Application drafts
* Application status

## Groq AI

Used for:

* Hiring contact research
* Personalized application emails
* Resume tailoring

## Hunter.io

Finds HR managers and recruiters.

## CallMeBot

Sends WhatsApp approval notifications.

## Google Docs

Creates job-specific resumes automatically.

## Gmail

Submits approved applications.

---

# Expected Outcomes

✅ Daily automated job discovery

✅ Automatic hiring manager identification

✅ Personalized application email drafts

✅ AI-generated tailored resumes

✅ Human approval before submission

✅ Application tracking dashboard

✅ Reduced application preparation time by 80%+

---

# Setup Instructions

## Required Accounts

* n8n
* Groq
* Hunter.io
* Google Sheets
* Google Docs
* Gmail
* RapidAPI (JSearch)
* CallMeBot

---

## Configure Credentials

Add:

* Groq API Key
* Hunter API Key
* Google OAuth Credentials
* Gmail OAuth Credentials

---

## Configure Placeholders

Replace:

```text
YOUR_RAPIDAPI_KEY
YOUR_HUNTER_API_KEY
YOUR_CALLMEBOT_APIKEY
YOUR_PHONE_NO_INTL
YOUR_EMAIL
YOUR_SPREADSHEET_URL
YOUR_RESUME_FOLDER_ID
YOUR_N8N_PUBLIC_URL
```

---

## Import Workflow

n8n → Import from File

Upload:

```text
Kenneth_Job_Application_v2.json
```

---

## Activate Workflow

Click:

```text
Activate
```

Workflow will execute daily at 8 PM.

---

# Expected User Experience

1. Jobs discovered automatically
2. HR contact identified
3. Email draft generated
4. WhatsApp notification received
5. Approve or reject
6. Resume customized
7. Application submitted
8. Tracking sheet updated automatically

---

# Author

Kenneth Soriano

AI Automation Specialist | Business Analyst | Customer Success Professional
