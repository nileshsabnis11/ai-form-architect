# THE AI FORM ARCHITECT

## Build Smart Systems with Google Sheets &amp; AI
### The Ultimate Prompt Engineering Guide for Non-Coders

---

**Author:** Mr. Nilesh Vijay Sabnis  
**Edition:** Batch 5 Special Release  
**Date:** February 2026  
**License:** Educational Use Only

---

## Table of Contents

1. Preface
2. Quick Start Guide
3. Introduction
4. What You'll Build
5. The Golden Workflow
6. Chapter 1: The Foundation (Basic Form)
7. Chapter 2: The Admin Panel (Dynamic Settings)
8. Chapter 3: Smart Logic (Timers &amp; Deadlines)
9. Chapter 4: The Wow Factor (API Integration)
10. Chapter 5: Hosting on Google Sites
11. Bonus: Advanced Features
12. Prompt Engineering Secrets
13. Real-World Use Cases
14. Troubleshooting &amp; FAQs
15. Glossary for Non-Coders
16. About the Author
17. Version History
18. Copyright &amp; Legal
19. Companion Cheat Sheet

---

## Preface

For years, software development was a walled garden. Only those who spent years mastering syntax, logic, and debugging could build useful tools. If you had an idea—a better attendance system, a smarter registration form, an automated workflow—you had two choices: hire an expensive developer or watch your idea die.

**Artificial Intelligence has shattered that wall.**

We have entered a new era where *English is the new programming language*. You no longer need to memorize semicolons and brackets. You simply need to articulate your logic clearly—and the AI translates your intent into working code.

I wrote this guide for:

| Who You Are | What You'll Build |
|-------------|-------------------|
| **Educators** | Automated attendance, assignment portals, exam registrations |
| **Small Business Owners** | Custom order forms, customer databases, booking systems |
| **Operations Managers** | Data collection tools, approval workflows, inventory forms |
| **Students** | Portfolio projects, event registrations, survey tools |
| **Dreamers** | Any idea you've been sitting on for years |

This book is not about teaching you how to code. It is about teaching you how to **think like an Architect** and command AI to do the heavy lifting.

&gt; *"The best code is the code you never had to write yourself."*

Welcome to the revolution. Let's build something amazing.

— *Nilesh Vijay Sabnis*  
February 2026

---

## Quick Start Guide

**Get your first form live in 5 minutes:**

| Step | Action |
|------|--------|
| 1 | Open sheets.new in your browser |
| 2 | Go to Extensions → Apps Script |
| 3 | Create index.html file (click + → HTML) |
| 4 | Copy Chapter 1 prompts into ChatGPT/Claude |
| 5 | Paste AI output into Apps Script files |
| 6 | Click Deploy → New Deployment → Web App |

**Done! Share your live form URL with the world!**

### Time Investment by Chapter

| Chapter | Time Required | Difficulty |
|---------|---------------|------------|
| Chapter 1: Basic Form | 15 minutes | Beginner |
| Chapter 2: Admin Panel | 10 minutes | Beginner |
| Chapter 3: Timers &amp; Deadlines | 15 minutes | Intermediate |
| Chapter 4: API Integration | 20 minutes | Intermediate |
| Chapter 5: Custom Hosting | 10 minutes | Beginner |
| Bonus Features | 10-15 min each | Advanced |

---

## Introduction

Welcome to the future of development. You are no longer just a user of software; you are an **Architect**.

In the traditional world, building a web application required months of learning HTML, CSS, JavaScript, Backend Languages, and Database Management.

**Today, that barrier has collapsed.**

This guide is the official companion to the "Smart Form System" workshop. It contains the exact "Magic Prompts" used during the live session to turn AI models (like ChatGPT, Claude, or Gemini) into your personal software engineer.

### Why Google Sheets + Apps Script?

| Feature | Benefit |
|---------|---------|
| **100% Free** | No hosting costs, no subscriptions |
| **Cloud-Based** | Access from anywhere, automatic backups |
| **Shareable** | Easy collaboration with team members |
| **Built-in Database** | Your data lives in familiar spreadsheets |
| **Secure** | Google's enterprise-grade security |
| **Mobile-Ready** | Works on any device automatically |

---

## What You'll Build

**Frontend (index.html)** → **Backend (Code.gs)** → **Database (Google Sheet)**

### Features You'll Implement

| Feature | Chapter | Description |
|---------|---------|-------------|
| Mobile-Responsive Design | 1 | Beautiful forms using Tailwind CSS |
| Admin Settings Panel | 2 | Change titles/rules without touching code |
| Auto-Locking Deadlines | 3 | Forms close automatically at set time |
| Countdown Timers | 3 | Cheat-proof timers using localStorage |
| Smart Dropdowns | 4 | Country → State → City cascading menus |
| Auto Phone Codes | 4 | Dial codes update based on country |
| File Uploads | Bonus | PDFs/images saved to Google Drive |
| Custom Domain Hosting | 5 | Professional URL for your form |

---

## The Golden Workflow

| Step | Action | Details |
|------|--------|---------|
| 1 | **Select a Chapter** | Choose the specific feature you want to build |
| 2 | **Copy the Prompt** | Copy the text inside the code blocks exactly |
| 3 | **Paste into AI** | Open ChatGPT, Claude, or Gemini |
| 4 | **Review &amp; Refine** | Read the AI output carefully |
| 5 | **Paste into Apps Script** | Copy to Code.gs and index.html files |
| 6 | **Deploy** | Click Deploy → New Deployment → Web App |

### The Golden Rule

**CRITICAL: Always create a New Version when deploying updates.**

1. Save your code (Ctrl+S)
2. Click "Deploy" → "Manage Deployments"
3. Click the Pencil (Edit) icon
4. Change "Version" dropdown to "New Version"
5. Click "Deploy"

---

## Chapter 1: The Foundation

**Goal:** Create a professional HTML form connected to a Google Sheet database.

### Learning Outcomes

- Understand Google Apps Script Web App architecture
- Set up development environment
- Deploy a live, mobile-responsive web form

### The Concept

| Component | What It Is | Analogy |
|-----------|------------|---------|
| **Google Sheet** | Your Database | Filing cabinet |
| **Code.gs** | Backend Logic | Office worker |
| **index.html** | Frontend UI | Reception desk |

### Step 1: Initial Setup

| Step | Action |
|------|--------|
| 1 | Type sheets.new in browser |
| 2 | Name it "Smart Form System" |
| 3 | Extensions → Apps Script |
| 4 | Click (+) → HTML → Name it index |

### Step 2: The Prompt

```
I need to create a web app using Google Apps Script and HTML.

## BACKEND (Code.gs)

1. **initialSetup()**: 
   - Connect to active Google Spreadsheet
   - Create "Submissions" sheet if doesn't exist
   - Headers: Timestamp, Name, Phone, Gender, Email, Country, State, City, Birthdate, Address

2. **doGet()**: 
   - Serve index.html as web app
   - Use HtmlService.createHtmlOutputFromFile()

3. **processForm(formData)**: 
   - Add timestamp automatically
   - Append data to "Submissions" sheet
   - Return success/error message

## FRONTEND (index.html)

1. **Styling**: Tailwind CSS, centered card, mobile-responsive
2. **Fields**: Name, Phone, Gender (radio), Email, Country, State, City, Birthdate, Address
3. **Submit Button**: Shows "Submitting..." while processing
4. **Feedback**: Success/error messages, clear form after success
5. **Submission**: Use google.script.run

Please provide complete Code.gs and index.html files.
```

### Step 3: Deploy

| Step | Action |
|------|--------|
| 1 | Click Deploy → New Deployment |
| 2 | Select Web App |
| 3 | Execute as: Me |
| 4 | Who has access: Anyone |
| 5 | Click Deploy |
| 6 | Copy the Web App URL |

---

## Chapter 2: The Admin Panel

**Goal:** Control form settings from spreadsheet without touching code.

### The Prompt

```
Update my form to use a "Settings" tab.

## BACKEND (Code.gs)

1. **Update initialSetup()**: Create "Settings" sheet with rows:
   - Form Title: Registration Form
   - Form Subtitle: Please fill all fields
   - Last Date (IST): 2026-12-31 23:59
   - Timer (Minutes): 0
   - Primary Color: #3B82F6

2. **Create getSettings()**: Read settings, return as object

3. **Update doGet()**: Use createTemplateFromFile(), pass settings

## FRONTEND (index.html)

1. Display dynamic title, subtitle, button color from settings
2. Keep all existing functionality

Please provide complete updated files.
```

---

## Chapter 3: Smart Logic and Urgency

**Goal:** Auto-lock form when deadline passes or timer expires.

### The Prompt

```
Add deadline and timer functionality.

## BACKEND (Code.gs)

1. **Update getSettings()**:
   - Convert "Last Date (IST)" to Asia/Kolkata timezone
   - Add 'isExpired' boolean
   - Add 'deadlineFormatted' string

## FRONTEND (index.html)

1. **Deadline**: If isExpired true, show "Applications Closed"
2. **Timer** (if Timer > 0):
   - Display countdown MM:SS in top-right
   - Red background when under 1 minute
   - Use localStorage to persist (survives refresh)
   - Disable form when timer reaches 0

Please provide complete updated files.
```

---

## Chapter 4: API Integration

**Goal:** Smart dropdowns for Country → State → City.

### The Prompt

```
Upgrade Location fields with API dropdowns.

## FRONTEND (index.html)

1. **Add Libraries**: jQuery, Select2

2. **API**: CountriesNow (https://countriesnow.space/api/v0.1)
   - /countries/states - Get countries with states
   - /countries/state/cities - Get cities

3. **Cascading Logic**:
   - Page load: Fetch countries
   - Country select: Fetch states
   - State select: Fetch cities

4. **Phone Code**: Auto-update dial code when country selected

## BACKEND (Code.gs)

5. **Phone Fix**: Prepend single quote before phone number

Please provide complete updated files.
```

---

## Chapter 5: Hosting on Google Sites

**Goal:** Professional URL for your form.

### Enable Embedding Prompt

```
Update doGet() to allow iframe embedding:
.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)
```

### Steps

| Step | Action |
|------|--------|
| 1 | Go to sites.google.com |
| 2 | Create blank site |
| 3 | Insert → Embed → By URL |
| 4 | Paste Apps Script URL |
| 5 | Publish |

---

## Bonus: Advanced Features

### Bonus 1: File Uploads

```
Add file upload to Google Drive.

## FRONTEND
- File input for PDF only, max 5MB
- Convert to Base64 using FileReader

## BACKEND
- Create saveFileToDrive() function
- Create "Form_Uploads" folder
- Save file URL to "Resume Link" column
```

### Bonus 2: Email Notifications

```
Add email notification on submission.

## BACKEND
- Add to Settings: Notification Email, Email Subject, Send Notification
- Create sendNotificationEmail() function
- Use GmailApp.sendEmail()
```

### Bonus 3: Duplicate Prevention

```
Prevent duplicate submissions by email.

## BACKEND
- Create checkDuplicate(email) function
- Return error if email already exists
```

### Bonus 4: Custom Fields Template

```
Add new field to form.

## FIELD DETAILS:
- Field Name: [NAME]
- Field Type: [text/dropdown/date/checkbox/radio/textarea/number]
- Required: [Yes/No]
- Options (if dropdown): [Option 1, Option 2, Option 3]
```

### Bonus 5: Success Redirect

```
Redirect to thank you page after submit.

## SETTINGS
- Redirect URL: https://yoursite.com/thank-you
- Redirect Delay: 3 seconds

## FRONTEND
- Show countdown before redirect
```

---

## Prompt Engineering Secrets

### 1. Be Specific, Not Vague

**Bad:** "Make a form"
**Good:** "Create an HTML form with Name, Email, Phone using Tailwind CSS with centered card layout"

### 2. Use Numbered Steps

```
## BACKEND (Code.gs)
1. Create function A
2. Create function B

## FRONTEND (index.html)
1. Add element A
2. Add logic for B
```

### 3. Specify Tech Stack

Always mention: Google Apps Script, Code.gs, index.html, Tailwind CSS

### 4. Ask for Edge Cases

- "Handle errors gracefully"
- "What if the cell is empty?"
- "Prevent double-clicking submit"

### 5. Debug with AI

```
Error: [PASTE ERROR]
Code: [PASTE CODE]
What's wrong and how to fix?
```

---

## Real-World Use Cases

### Education

| Use Case | Features |
|----------|----------|
| Exam Registration | Deadline + Timer + Duplicate Prevention |
| Assignment Portal | File Upload + Email Notification |
| Event RSVP | Dropdown Options + Custom Domain |
| Student Feedback | Anonymous + Data Validation |

### Business

| Use Case | Features |
|----------|----------|
| Job Applications | File Upload + Email Alerts |
| Customer Orders | Product Dropdowns + Order ID |
| IT Support Tickets | Priority Dropdown + Auto-Assignment |
| Employee Surveys | Anonymous + Department Filtering |

### Events

| Use Case | Features |
|----------|----------|
| Conference Registration | Session Selection + Payment |
| Wedding RSVP | Meal Preferences + Plus-One |
| Competition Entry | File Upload + Timer |
| Volunteer Application | Skill Checkboxes + Availability |

---

## Troubleshooting Cheat Sheet

| Problem | Solution |
|---------|----------|
| "Script function not found" | Select correct function from dropdown |
| Changes not showing | Deploy NEW version |
| #ERROR! in Phone | Add single quote before phone string |
| "Refused to connect" | Add setXFrameOptionsMode |
| Timer resets on refresh | Check localStorage key name |
| API empty | Check browser console (F12) |
| Form won't submit | Check for JavaScript errors |
| Email not sending | Authorize Gmail access first |

### Debug Template

```
Error: [PASTE ERROR]
Expected: [WHAT SHOULD HAPPEN]
Actual: [WHAT'S HAPPENING]
Code: [PASTE CODE]
Please fix.
```

### Quick Fixes Checklist

- [ ] Save both files (Ctrl+S)
- [ ] Deploy NEW version
- [ ] Clear browser cache (Ctrl+Shift+R)
- [ ] Check browser console (F12)
- [ ] Run initialSetup after changes

---

## Glossary for Non-Coders

| Term | Meaning |
|------|---------|
| **API** | Messenger fetching data from other websites |
| **Backend** | Behind-the-scenes logic (Code.gs) |
| **Frontend** | What users see (index.html) |
| **Deploy** | Publish live |
| **localStorage** | Browser storage that survives refresh |
| **CMS** | Content management (Settings sheet) |
| **CDN** | External library hosting |
| **JSON** | Data format for APIs |
| **Validation** | Checking user input is correct |
| **Responsive** | Adjusts to any screen size |

---

## About the Author

**Mr. Nilesh Vijay Sabnis**
*Assistant Professor | Automation &amp; Robotics Specialist*

Nilesh is an educator passionate about democratizing technology. He helps non-coders build professional software using AI.

**Mission:** Make software development accessible to everyone.

**Philosophy:** "The best code is the code you never had to write yourself."

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | February 2026 | Initial Batch 5 Release |

---

## Copyright and Legal

© 2026 Nilesh Vijay Sabnis. All Rights Reserved.

Code examples provided under MIT License for educational purposes.

**Trademarks:** Google, ChatGPT, Claude, Gemini belong to their respective owners.

---

## Acknowledgments

Thanks to Batch 5 workshop participants, the open-source community, and Google for free development tools.

---

# COMPANION CHEAT SHEET

## Quick Start

| Step | Action |
|------|--------|
| 1 | sheets.new → Name it |
| 2 | Extensions → Apps Script |
| 3 | Create index.html |
| 4 | Copy prompts → AI → Paste code |
| 5 | Deploy → Web App → Anyone |

## Golden Rule

**Always deploy NEW VERSION after changes!**

## Essential Code

### doGet with Embedding
```javascript
function doGet() {
  return HtmlService.createTemplateFromFile('index')
    .evaluate()
    .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL);
}
```

### Fix Phone Error
```javascript
var phoneNumber = "'" + formData.phone;
```

### Timezone
```javascript
Utilities.formatDate(new Date(), "Asia/Kolkata", "yyyy-MM-dd HH:mm")
```

### localStorage Timer
```javascript
localStorage.setItem('formTimer', remainingSeconds);
var saved = localStorage.getItem('formTimer');
```

## Key URLs

| Resource | URL |
|----------|-----|
| Create Sheet | sheets.new |
| Google Sites | sites.google.com |
| CountriesNow API | countriesnow.space |
| Tailwind CSS | tailwindcss.com |

## Pre-Launch Checklist

- [ ] All fields save to sheet
- [ ] Form looks good on mobile
- [ ] Deadline works
- [ ] Timer persists on refresh
- [ ] Deployed as NEW version
- [ ] Tested in incognito

---

**© 2026 Nilesh Vijay Sabnis | Educational Use Only**

*"The best code is the code you never had to write yourself."*

---

# END OF EBOOK
