HireMind - AI Resume Screening & Evaluation Pipeline
An end-to-end AI-powered HR automation workflow built with n8n, Groq, and Google Workspace that automates candidate screening from form submission to final evaluation — no manual resume filtering required.

How It Works

Candidate submits a form with their name, email, CV (PDF), and selected job role
CV is uploaded to Google Drive automatically for record-keeping
Profile Analyzer Agent reads the resume, extracts structured candidate data into JSON using Groq LLM
Job Description is automatically fetched from Google Sheets based on the selected role
HR Expert Agent evaluates the candidate against the JD — generating strengths, gaps, and a hire/no-hire recommendation
Results are distributed:

Qualified candidates receive an email via SendGrid
Hiring team gets a Slack notification with a summary
All evaluations are logged in a Google Sheet for tracking




Workflow Preview
<img src="Screenshot 2026-04-23 144119.png" alt="HireMind Workflow" width="100%"/>

Tech Stack
ToolPurposen8nWorkflow automationGroqLLM for profile analysis & HR evaluationGoogle DriveCV and JD storageGoogle SheetsJob role mapping & evaluation trackingSendGridCandidate email notificationSlackHiring team alert

Setup Instructions
1. Prerequisites

n8n installed (local or cloud)
Groq API key
Google Cloud account with Sheets & Drive API enabled
SendGrid account
Slack workspace

2. Google Drive Structure
├── jd/ — Upload your Job Description PDFs here
├── cv/ — Candidate CVs will be auto-uploaded here
├── Positions — Google Sheet: Job Role ↔ JD file URL mapping
└── Evaluations — Google Sheet: Final AI evaluation results
3. Positions Sheet Format
Job RoleJob Description LinkBackend Engineerhttps://drive.google.com/...Azure DevOps Leadhttps://drive.google.com/...
4. Import Workflow

Download workflow.json from this repo
Open n8n → Click "Import from file"
Connect your credentials (Groq, Google, SendGrid, Slack)
Update the Google Sheet and Drive folder IDs in the nodes
Run the workflow!


Project Structure
hiremind-ai-resume-screening/
├── workflow.png — Workflow preview image
├── workflow.json — n8n workflow export
└── README.md

Author
Golla Vishnu

LinkedIn: golla-vishnu
GitHub: vshnu07
