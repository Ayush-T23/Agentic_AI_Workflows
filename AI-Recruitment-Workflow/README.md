# AI Recruitment & Resume Screening Automation

## Overview
The AI Recruitment & Resume Screening Automation is an intelligent hiring workflow built using n8n that automates the complete initial recruitment process. The system collects candidate resumes from Google Sheets, extracts resume content, analyzes candidate profiles using AI, evaluates candidate suitability, schedules interviews for shortlisted candidates, and automatically sends email notifications to both candidates and HR teams.

This workflow significantly reduces manual HR effort by automating resume screening, candidate filtering, interview scheduling, and communication management.

---

# Workflow Architecture

## Workflow Screenshot

![Workflow](workflow.png)

---

# Objective

The main objective of this workflow is to:
- Automate resume collection and screening
- Reduce manual HR workload
- Improve candidate shortlisting efficiency
- Enable AI-based candidate evaluation
- Automate interview scheduling
- Send automated notifications and emails

---

# Technologies & Tools Used

| Tool / Service | Purpose |
|---|---|
| n8n | Workflow automation platform |
| Google Sheets | Candidate application trigger source |
| Google Drive | Resume storage and retrieval |
| Gemini AI / OpenAI | AI-powered resume analysis |
| Gmail | Candidate communication |
| Google Calendar | Interview scheduling |
| PostgreSQL | Candidate data storage |
| Slack | HR team notifications |

---

# Workflow Explanation

## 1. Google Sheets Trigger
The workflow starts automatically whenever a new candidate entry is added to Google Sheets.

### Purpose
- Detect new candidate applications
- Trigger automated recruitment pipeline

---

## 2. Download Resume
The workflow downloads the uploaded resume from Google Drive.

### Purpose
- Retrieve candidate resume file
- Prepare file for AI analysis

---

## 3. Extract Resume Text
The PDF resume is processed and converted into readable text.

### Purpose
- Extract candidate skills and experience
- Enable AI-based processing

---

## 4. Gemini Resume Analysis
Gemini AI analyzes the extracted resume content.

### AI Evaluation Includes
- Skills assessment
- Experience analysis
- Role matching
- Qualification validation
- Candidate scoring

### Purpose
- Perform intelligent resume screening
- Reduce manual HR evaluation effort

---

## 5. Parse Gemini Response
The AI response is converted into structured candidate data.

### Purpose
- Extract candidate score
- Prepare data for workflow conditions

---

## 6. Check Candidate Score
The workflow evaluates whether the candidate qualifies for the next recruitment stage.

### Conditions
- Qualified candidates proceed for interview scheduling
- Rejected candidates receive rejection email

---

# Qualified Candidate Flow

## 7. Store Candidate Data
Qualified candidate information is stored in PostgreSQL database.

### Stored Information
- Candidate name
- Email
- Resume score
- Skills
- Interview status

---

## 8. Get Availability in Calendar
The workflow checks available interview time slots from Google Calendar.

### Purpose
- Identify free interview timings
- Avoid scheduling conflicts

---

## 9. Free Time Slot Processing
Available slots are processed and selected for interview scheduling.

### Purpose
- Select optimal interview timing
- Automate slot management

---

## 10. Schedule Interview in HR Calendar
Interview event is automatically created in Google Calendar.

### Details Included
- Candidate name
- Interview date and time
- Meeting details
- HR attendees

---

## 11. Send Shortlist Email
A shortlist confirmation email is automatically sent to the candidate.

### Email Includes
- Interview confirmation
- Date and timing
- Instructions for interview

---

## 12. Notify HR
Slack notification is sent to HR team.

### Purpose
- Inform HR about shortlisted candidate
- Share interview details instantly

---

## 13. Wait Node
The workflow pauses temporarily before sending follow-up communication.

### Purpose
- Manage communication timing
- Avoid immediate email flooding

---

## 14. Send Follow-Up Message
Final follow-up email/message is sent to candidate.

### Purpose
- Confirm interview reminders
- Maintain communication consistency

---

# Rejected Candidate Flow

## 15. Send Rejection Email
Candidates who do not meet the score threshold automatically receive a rejection email.

### Purpose
- Automate candidate communication
- Improve recruitment experience

---

# Key Features

- AI-powered resume analysis
- Automated candidate filtering
- Intelligent candidate scoring
- Automated interview scheduling
- Calendar integration
- HR notification system
- Automated email communication
- Resume parsing automation
- Database storage integration
- End-to-end recruitment automation

---

# Business Benefits

## HR Efficiency
Reduces manual resume screening workload significantly.

## Faster Hiring
Speeds up candidate evaluation and interview scheduling.

## Improved Accuracy
AI-based screening improves candidate selection quality.

## Automation
Minimizes repetitive HR tasks.

## Scalability
Can handle large numbers of candidate applications efficiently.

---

# Workflow File

Download the exported n8n workflow JSON file below:

[Download Workflow JSON](workflow.json)

---

# Future Improvements

- ATS integration
- AI-based interview feedback analysis
- Candidate ranking dashboard
- Multi-role recruitment support
- Automated onboarding workflow
- Resume skill visualization
- Candidate analytics dashboard

---

# Conclusion

This AI Recruitment & Resume Screening Automation demonstrates how AI and workflow automation can modernize recruitment operations. By integrating AI analysis, automated scheduling, email communication, and HR notifications, the workflow creates a complete intelligent recruitment pipeline that improves efficiency, reduces manual work, and enhances candidate management processes.
