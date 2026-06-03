# n8n Workflow Automation Projects

A collection of practical n8n automation workflows for email management, lead capture, CRM updates, job market research, and AI-assisted productivity.

## Projects

### AI Email Classifier & Response Assistant

An AI-powered Gmail automation workflow that classifies incoming emails with Google Gemini, applies the correct Gmail labels, archives selected messages, and creates draft replies for personal emails.

**Folder:** [ai-email-classifier-assistant](ai-email-classifier-assistant/)

**Highlights:**

- Gmail email classification using Gemini 2.5 Pro
- Categories for jobs, work, personal, finance, support, travel, updates, social, and promotions
- Automatic Gmail label assignment
- Inbox cleanup by marking messages as read and removing the Inbox label
- AI-generated Gmail drafts for personal email replies using Gemini 2.5 Flash

**Workflow file:** `ai-email-classifier-assistant/My workflow 2.json`

### Lead Management Automation

A lead management workflow that captures form submissions, stores leads in Google Sheets, qualifies them by budget, notifies the business owner, sends service-specific follow-up emails, and updates CRM-style lead status.

**Folder:** [lead-management-automation](lead-management-automation/)

**Highlights:**

- n8n form trigger for lead capture
- Google Sheets lead database
- Budget-based lead qualification
- Internal Gmail notification for qualified leads
- Personalized follow-up emails for SEO and ADS inquiries
- Contacted and rejected status updates in Google Sheets

**Workflow file:** `lead-management-automation/My workflow.json`

### Job Market Automation

An n8n workflow that uses Apify scrapers to collect Google Maps company data and Indeed job listings, stores the results in Google Sheets, and includes a Gmail digest branch for qualified leads.

**Folder:** [job-market-automation](job-market-automation/)

**Highlights:**

- Scheduled Apify scraping for Google Maps businesses
- Scheduled Apify scraping for Indeed job listings
- Google Sheets append-or-update storage for companies and jobs
- Dedupe matching by website and company URL
- Lead filtering, sorting, and Gmail summary generation

**Workflow file:** `job-market-automation/My workflow 3.json`

## Repository Structure

```text
n8n-workflows/
├── README.MD
├── ai-email-classifier-assistant/
│   ├── My workflow 2.json
│   ├── README.MD
│   └── screenshots/
│       ├── draft.png
│       ├── gmail-labels.png
│       └── workflow.png
├── job-market-automation/
│   ├── My workflow 3.json
│   ├── README.MD
│   └── screenshots/
│       ├── jobs-sheet.png
│       └── workflow.png
└── lead-management-automation/
    ├── My workflow.json
    ├── README.MD
    └── screenshots/
        ├── form.png
        ├── sheets.png
        └── workflow.png
```

## Requirements

- n8n
- Gmail OAuth2 credentials
- Google account access
- Google Sheets credentials for the lead workflow
- Apify credentials for the job market workflow
- Google Gemini credentials for the AI email workflow

## How To Use

1. Open the folder for the workflow you want to use.
2. Read the project-specific `README.MD`.
3. Import the workflow JSON file into n8n.
4. Configure credentials and account-specific IDs.
5. Test the workflow with sample data.
6. Activate the workflow when everything looks correct.

## Notes

- Workflow credentials are not included and must be configured in your own n8n instance.
- Gmail labels, Google Sheet IDs, email recipients, Apify actor settings, and model credentials are account-specific.
- Review all email templates, AI prompts, scraper inputs, and automation rules before activating.

## Author

Vivek Suyal

If you found these workflows useful, consider giving the repository a star.
