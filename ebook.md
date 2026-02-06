# THE AI FORM ARCHITECT

## Build Smart Systems with Google Sheets & AI

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
8. Chapter 3: Smart Logic (Timers & Deadlines)
9. Chapter 4: The Wow Factor (API Integration)
10. Chapter 5: Hosting on Google Sites
11. Bonus: Advanced Features
12. Prompt Engineering Secrets
13. Real-World Use Cases
14. Troubleshooting & FAQs
15. Glossary for Non-Coders
16. About the Author
17. Copyright & Legal
18. Companion Cheat Sheet

---

## Preface

For years, software development was a walled garden. Only those who spent years mastering syntax, logic, and debugging could build useful tools. If you had an idea—a better attendance system, a smarter registration form, an automated workflow—you had two choices: hire an expensive developer or watch your idea die.

**Artificial Intelligence has shattered that wall.**

We have entered a new era where *English is the new programming language*. You no longer need to memorize semicolons and brackets. You simply need to articulate your logic clearly—and the AI translates your intent into working code.

I wrote this guide for Educators, Small Business Owners, Operations Managers, Students, and Dreamers who want to build professional software without coding.

> *"The best code is the code you never had to write yourself."*

Welcome to the revolution. Let's build something amazing.

— *Nilesh Vijay Sabnis*, February 2026

---

## Quick Start Guide

Get your first form live in 5 minutes:

| Step | Action |
|------|--------|
| 1 | Open sheets.new in your browser |
| 2 | Go to Extensions then Apps Script |
| 3 | Create index.html file (click + then HTML) |
| 4 | Copy Chapter 1 prompts into ChatGPT/Claude |
| 5 | Paste AI output into Apps Script files |
| 6 | Click Deploy then New Deployment then Web App |

Done! Share your live form URL with the world!

### Time Investment by Chapter

| Chapter | Time Required | Difficulty |
|---------|---------------|------------|
| Chapter 1: Basic Form | 15 minutes | Beginner |
| Chapter 2: Admin Panel | 10 minutes | Beginner |
| Chapter 3: Timers and Deadlines | 15 minutes | Intermediate |
| Chapter 4: API Integration | 20 minutes | Intermediate |
| Chapter 5: Custom Hosting | 10 minutes | Beginner |
| Bonus Features | 10-15 min each | Advanced |

---

## Introduction

Welcome to the future of development. You are no longer just a user of software; you are an Architect.

This guide is the official companion to the Smart Form System workshop. It contains the exact Magic Prompts used during the live session to turn AI models like ChatGPT, Claude, or Gemini into your personal software engineer.

### Why Google Sheets + Apps Script?

| Feature | Benefit |
|---------|---------|
| 100% Free | No hosting costs, no subscriptions |
| Cloud-Based | Access from anywhere, automatic backups |
| Shareable | Easy collaboration with team members |
| Built-in Database | Your data lives in familiar spreadsheets |
| Secure | Google enterprise-grade security |
| Mobile-Ready | Works on any device automatically |

---

## What You'll Build

Frontend (index.html) connects to Backend (Code.gs) which connects to Database (Google Sheet)

### Features You'll Implement

| Feature | Chapter | Description |
|---------|---------|-------------|
| Mobile-Responsive Design | 1 | Beautiful forms using Tailwind CSS |
| Admin Settings Panel | 2 | Change titles/rules without touching code |
| Auto-Locking Deadlines | 3 | Forms close automatically at set time |
| Countdown Timers | 3 | Cheat-proof timers using localStorage |
| Smart Dropdowns | 4 | Country then State then City cascading menus |
| Auto Phone Codes | 4 | Dial codes update based on country |
| File Uploads | Bonus | PDFs/images saved to Google Drive |
| Custom Domain Hosting | 5 | Professional URL for your form |

---

## The Golden Workflow

| Step | Action | Details |
|------|--------|---------|
| 1 | Select a Chapter | Choose the specific feature you want to build |
| 2 | Copy the Prompt | Copy the text inside the code blocks exactly |
| 3 | Paste into AI | Open ChatGPT, Claude, or Gemini |
| 4 | Review and Refine | Read the AI output carefully |
| 5 | Paste into Apps Script | Copy to Code.gs and index.html files |
| 6 | Deploy | Click Deploy then New Deployment then Web App |

### The Golden Rule

CRITICAL: Always create a New Version when deploying updates.

Clicking Save alone will NOT update your live web app!

Correct Process:
1. Save your code (Ctrl+S)
2. Click Deploy then Manage Deployments
3. Click the Pencil Edit icon
4. Change Version dropdown to New Version
5. Click Deploy

---

## Chapter 1: The Foundation

Goal: Create a professional HTML form connected to a Google Sheet database.

### Learning Outcomes

By the end of this chapter, you will be able to:
- Understand the basic architecture of a Google Apps Script Web App
- Set up a development environment connecting Google Sheets to a code editor
- Deploy a live, mobile-responsive web form that captures data instantly

### The Concept

We are building a Serverless application. This means you don't need to rent a server or worry about infrastructure—Google handles everything.

| Component | What It Is | Real-World Analogy |
|-----------|------------|-------------------|
| Google Sheet | Your Database | A filing cabinet for all responses |
| Code.gs | Backend Logic | The office worker who files papers |
| index.html | Frontend UI | The reception desk where visitors fill forms |

How Data Flows:
1. User fills form
2. index.html captures data
3. Code.gs processes submission
4. Google Sheet stores the data
5. User sees Success message

### Step 1: Initial Setup

| Step | Action | Details |
|------|--------|---------|
| 1 | Open browser | Type sheets.new in address bar |
| 2 | Name the sheet | Click Untitled spreadsheet then Type Smart Form System |
| 3 | Open Apps Script | Menu: Extensions then Apps Script |
| 4 | Wait for editor | A new tab opens with Code.gs file |
| 5 | Create HTML file | Click (+) next to Files then Select HTML then Name it index |
| 6 | Verify setup | You should see Code.gs and index.html in the file list |

### Step 2: The Prompt

Copy and paste this entire prompt into ChatGPT, Claude, or Gemini:

---
I need to create a web app using Google Apps Script and HTML.

BACKEND (Code.gs)

Create the following functions:

1. initialSetup(): 
   - Connect to the active Google Spreadsheet
   - Create a sheet named Submissions if it does not exist
   - Add these headers to row 1: Timestamp, Name, Phone, Gender, Email, Country, State, City, Birthdate, Address
   - Do NOT duplicate headers if they already exist

2. doGet(): 
   - Serve the index.html file as a web app
   - Use HtmlService.createHtmlOutputFromFile()

3. processForm(formData): 
   - Receive form data as a parameter
   - Add a timestamp automatically
   - Append the data as a new row in the Submissions sheet
   - Return a success/error message

FRONTEND (index.html)

Create a modern, professional form with these requirements:

1. Styling: 
   - Use Tailwind CSS via CDN
   - Centered card layout with shadow
   - Clean white background with subtle borders
   - Mobile-responsive design

2. Form Fields (all required):
   - Full Name (text input)
   - Phone Number (tel input)
   - Gender (radio buttons: Male, Female, Other)
   - Email (email input)
   - Country (text input for now)
   - State (text input for now)
   - City (text input for now)
   - Birthdate (date picker)
   - Address (textarea)

3. Submit Button:
   - Professional styling with hover effect
   - Shows Submitting... while processing
   - Disabled during submission to prevent double-clicks

4. User Feedback:
   - Show success message after submission
   - Show error message if something fails
   - Clear form after successful submission

5. Form Submission:
   - Use google.script.run to call the backend
   - Handle success and failure callbacks

Please provide the complete Code.gs and index.html files.
---

### Step 3: Execution

| Step | Action |
|------|--------|
| 1 | Copy the Code.gs output from AI |
| 2 | Paste it into your Apps Script Code.gs file (replace everything) |
| 3 | Copy the index.html output from AI |
| 4 | Paste it into your Apps Script index.html file (replace everything) |
| 5 | Save both files (Ctrl+S or Cmd+S) |
| 6 | Select initialSetup from the function dropdown (top toolbar) |
| 7 | Click Run (play button) |
| 8 | Grant permissions when prompted (click Advanced then Go to project) |
| 9 | Check your Google Sheet—Submissions tab should appear with headers |

### Step 4: Deploy Your Web App

| Step | Action |
|------|--------|
| 1 | Click Deploy (blue button, top-right) |
| 2 | Select New Deployment |
| 3 | Click the gear icon then Select Web App |
| 4 | Description: Version 1 - Basic Form |
| 5 | Execute as: Me |
| 6 | Who has access: Anyone |
| 7 | Click Deploy |
| 8 | Copy the Web App URL |
| 9 | Open the URL in a new tab—your form is live! |

### Chapter 1 Checkpoint

Before moving on, verify:
- Your form loads at the Web App URL
- You can fill out all fields
- Clicking Submit shows a success message
- Data appears in your Google Sheet Submissions tab
- Timestamp is automatically added

---

## Chapter 2: The Admin Panel

Goal: Control your form's title, deadlines, and rules directly from the spreadsheet without touching code ever again.

### Learning Outcomes

- Transform a static Google Sheet into a dynamic Content Management System (CMS)
- Update your live web application's title and rules without touching code
- Understand the flow of data from the Settings tab to the frontend

### The Concept

Hardcoding is bad practice. If you write text directly into your code, you'll need to edit code and redeploy every time you want to change it.

By creating a Settings tab, we turn your Google Sheet into a CMS (Content Management System). This allows you to change the website title just by typing in a cell—exactly like a WordPress admin panel.

### The Prompt

Copy and paste this prompt into AI:

---
Update my Google Apps Script form to make it dynamic based on a Settings tab.

BACKEND UPDATES (Code.gs)

1. Update initialSetup(): 
   - Create a Settings sheet if it does not exist
   - Add these rows to the Settings sheet:
     - Form Title: Registration Form
     - Form Subtitle: Please fill all fields
     - Last Date (IST): 2026-12-31 23:59
     - Timer (Minutes): 0
     - Primary Color: #3B82F6
   - Do NOT overwrite if Settings sheet already has data

2. Create getSettings() function:
   - Read all settings from the Settings sheet
   - Return them as a JavaScript object
   - Example: { formTitle: Registration Form, formSubtitle: ..., ... }

3. Update doGet():
   - Call getSettings()
   - Pass the settings to the HTML template
   - Use HtmlService.createTemplateFromFile() instead of createHtmlOutputFromFile()

FRONTEND UPDATES (index.html)

1. Receive settings from backend using scriptlet tag to inject settings

2. Display dynamic content:
   - Form title from settings
   - Form subtitle from settings
   - Primary button color from settings

3. Keep all existing functionality:
   - All form fields should still work
   - Form submission should still work

Please provide the complete updated Code.gs and index.html files.
---

### Execution Steps

| Step | Action |
|------|--------|
| 1 | Replace your Code.gs with the new AI output |
| 2 | Replace your index.html with the new AI output |
| 3 | Save both files |
| 4 | Select initialSetup from dropdown and click Run |
| 5 | Check Google Sheet—a new Settings tab should appear |
| 6 | Deploy New Version (remember the Golden Rule!) |

### Test the Admin Panel

| Test | Steps |
|------|-------|
| Change Title | Go to Settings tab then Change Form Title value then Refresh your form URL |
| Change Color | Go to Settings tab then Change Primary Color to #10B981 then Refresh |
| Change Subtitle | Go to Settings tab then Change Form Subtitle then Refresh |

Congratulations! You now have a no-code admin panel!

### Chapter 2 Checkpoint

- Settings tab exists with 5 rows of settings
- Changing Form Title updates the live form
- Changing Primary Color updates button colors
- Form submission still works correctly

---

## Chapter 3: Smart Logic and Urgency

Goal: Implement Logic Guards that automatically lock the form when a deadline passes or a timer runs out.

### Learning Outcomes

- Implement server-side validation to enforce strict deadlines
- Use localStorage to create persistent countdown timers
- Handle Time Zones (IST) correctly in web applications

### The Concept

Standard Google Forms require you to manually toggle Not Accepting Responses. Our system uses Server-Side Validation—it checks the current time against your deadline and refuses to load if time has passed.

Two Types of Time Limits:

| Type | Purpose | Example Use Case |
|------|---------|------------------|
| Deadline | Form closes at a specific date/time | Applications close Dec 31, 11:59 PM IST |
| Timer | Each user gets limited time to complete | Complete this quiz in 15 minutes |

Why localStorage for Timers?

Without localStorage, a sneaky user could:
1. Start the quiz (15 minutes begin)
2. Take 10 minutes answering
3. Refresh the page
4. Get a fresh 15 minutes! (Cheating!)

With localStorage, the timer state is saved in the browser. Refreshing does not reset it.

### The Prompt

---
Add deadline and timer functionality to my Google Apps Script form.

BACKEND UPDATES (Code.gs)

1. Update getSettings():
   - Read Last Date (IST) from settings
   - Handle both Date objects and String formats
   - Convert to Asia/Kolkata timezone
   - Compare against current IST time
   - Add isExpired boolean to returned settings (true if deadline passed)
   - Add deadlineFormatted string (human-readable deadline)

2. Time Zone Handling:
   - Use Utilities.formatDate() with Asia/Kolkata timezone
   - Current time example: Utilities.formatDate(new Date(), Asia/Kolkata, yyyy-MM-dd HH:mm)

FRONTEND UPDATES (index.html)

1. Deadline Handling:
   - Check isExpired flag from settings
   - If true: Hide the entire form, show a professional Applications Closed message
   - Show when the deadline was: This form closed on [date]

2. Timer Implementation (only if Timer > 0 in settings):
   - Display countdown timer in top-right corner (fixed position)
   - Format: MM:SS
   - Style: Red background when under 1 minute remaining
   
3. localStorage Logic (CRITICAL):
   - On page load, check if timer exists in localStorage for this form
   - If exists: Resume from saved time
   - If not: Start fresh timer from settings value
   - Save remaining time to localStorage every second
   - Use a unique key like formTimer_[timestamp] to prevent conflicts

4. Timer Expiry:
   - When timer reaches 0:00:
     - Disable all form inputs
     - Disable submit button
     - Show Time's Up! message
     - Optionally auto-submit the form

5. Visual Countdown:
   - Show deadline date/time on the form
   - Example: Submit before: December 31, 2026 11:59 PM IST

Please provide the complete updated Code.gs and index.html files.
---

### Test Deadline Feature

| Test | Steps |
|------|-------|
| Test Expired | Set Last Date (IST) to yesterday's date then Refresh form then Should show Closed |
| Test Active | Set Last Date (IST) to next month then Refresh form then Should show form |

### Test Timer Feature

| Test | Steps |
|------|-------|
| Test Timer Display | Set Timer (Minutes) to 2 then Refresh form then Timer should appear |
| Test Persistence | With timer running, refresh the page then Timer should continue (not reset) |
| Test Expiry | Wait for timer to reach 0:00 then Form should disable |

### Chapter 3 Checkpoint

- Past deadlines show Applications Closed message
- Timer appears when Timer setting > 0
- Timer survives page refresh (localStorage working)
- Timer reaching 0 disables the form
- Deadline date displays on the form

---

## Chapter 4: API Integration

Goal: Replace manual text boxes with smart, searchable dropdowns that auto-populate based on location.

### Learning Outcomes

- Connect your frontend to an external Public API
- Handle JSON data responses to populate UI elements dynamically
- Implement cascading dropdown logic (Country then State then City)

### The Concept

An API (Application Programming Interface) is like a waiter in a restaurant:

Restaurant Analogy:
- YOU (Customer) says I want pasta
- WAITER (API) Takes order, Returns food
- KITCHEN (Database) Makes pasta

Your Form:
- YOUR FORM says Give me countries
- API Fetches data, Returns JSON
- EXTERNAL DATABASE Returns list

We will use the free CountriesNow API to get:
- List of all countries
- States/provinces for selected country
- Cities for selected state

Cascading Dropdown Flow:
1. Page Loads then Fetch ALL countries then Populate Country dropdown
2. User selects India then Fetch states of India then Populate State dropdown (now enabled)
3. User selects Maharashtra then Fetch cities of Maharashtra then Populate City dropdown (now enabled)
4. User selects Mumbai then Ready to submit!

### The Prompt

---
Upgrade the Location fields (Country, State, City) to use a public API with searchable dropdowns.

FRONTEND UPDATES (index.html)

1. Add Libraries (in head):
   - jQuery (for easier AJAX calls)
   - Select2 CSS and JS (for searchable dropdowns)
   
   CDN Links:
   - https://code.jquery.com/jquery-3.6.0.min.js
   - https://cdn.jsdelivr.net/npm/select2@4.1.0-rc.0/dist/css/select2.min.css
   - https://cdn.jsdelivr.net/npm/select2@4.1.0-rc.0/dist/js/select2.min.js

2. Replace Location Inputs:
   - Change Country from text input to select dropdown
   - Change State from text input to select dropdown
   - Change City from text input to select dropdown
   - Initialize all with Select2 for searchability

3. API Integration (use CountriesNow API):
   
   Base URL: https://countriesnow.space/api/v0.1
   
   Endpoints:
   - Get all countries: POST /countries/states (returns countries with their states)
   - Get cities: POST /countries/state/cities
     Body: { country: India, state: Maharashtra }

4. Cascading Logic:
   
   On Page Load:
   - Fetch countries list
   - Populate Country dropdown
   - State dropdown: disabled, shows Select Country first
   - City dropdown: disabled, shows Select State first
   
   On Country Select:
   - Clear State and City dropdowns
   - Fetch states for selected country
   - Enable and populate State dropdown
   
   On State Select:
   - Clear City dropdown
   - Fetch cities for selected state
   - Enable and populate City dropdown

5. Loading States:
   - Show Loading... as first option while API fetches
   - Handle API errors gracefully (show Error loading data)

6. Styling:
   - Make Select2 dropdowns match Tailwind styling
   - Ensure dropdowns are full-width
   - Mobile-responsive

Please provide the complete updated index.html file.
---

### Auto Phone Code Prompt

---
Add automatic phone dial code selection based on country.

FRONTEND UPDATES

1. Change API Endpoint for Countries:
   - Use: https://countriesnow.space/api/v0.1/countries/codes
   - This returns country name AND dial code (e.g., +91 for India)

2. Split Phone Input:
   - Left side: Fixed dial code display (read-only, e.g., +91)
   - Right side: Phone number input field
   - Style them as connected inputs (looks like one field)

3. Auto-Update Logic:
   - When user selects a Country, automatically update the dial code
   - Example: Select India then Dial code shows +91

4. Form Submission:
   - Combine dial code + phone number before sending
   - Example: +91 + 9876543210 = +91 9876543210

BACKEND UPDATES (Code.gs)

5. Phone Number Fix (CRITICAL):
   - In processForm(), prepend a single quote before the phone string
   - Example: +91 9876543210 becomes '+91 9876543210
   - This prevents Google Sheets from interpreting + as a formula

Please provide the updated code.
---

### Chapter 4 Checkpoint

- Countries load on page load (200+ options)
- Selecting country populates states
- Selecting state populates cities
- Dropdowns are searchable (can type to filter)
- Phone dial code updates when country changes
- Submitted data shows correctly in Google Sheet

---

## Chapter 5: Hosting on Google Sites

Goal: Hide the ugly script link and host your form on a professional, free website (or your own domain).

### Learning Outcomes

- Configure Google Apps Script security settings for embedding
- Integrate a Web App into Google Sites
- Map a custom domain for a professional look

### The Concept

Google Apps Script URLs look like this:

Ugly URL:
https://script.google.com/macros/s/AKfycbzX123abc456def789ghi/exec

Professional URL:
https://forms.yourcompany.com

We achieve this by embedding the script inside Google Sites, then connecting a custom domain.

### Prerequisite: Allow Embedding

Before embedding, you must tell the script it is allowed to be in an iframe (security feature).

Prompt for AI:

---
I want to embed this web app on a Google Site. 

Update the doGet() function in Code.gs to allow iframe embedding.

Add this line before returning the HTML:
.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)

Provide the updated doGet() function.
---

After getting the code:
1. Update your Code.gs
2. Save and deploy New Version

### Step 1: Create Your Google Site

| Step | Action |
|------|--------|
| 1 | Go to sites.google.com |
| 2 | Click + Blank to create a new site |
| 3 | Click Untitled Site (top-left) then Enter your site name |
| 4 | Delete the default header by clicking it then pressing Delete |

### Step 2: Embed Your Form

| Step | Action |
|------|--------|
| 1 | On the right sidebar, click Embed (looks like <>) |
| 2 | Select Embed URL |
| 3 | Paste your Apps Script Web App URL (ends in /exec) |
| 4 | Click Insert |
| 5 | Drag the corners to make it full width |
| 6 | Drag the bottom edge to make it full height (no scrollbars) |

### Step 3: Publish Your Site

| Step | Action |
|------|--------|
| 1 | Click Publish button (top-right) |
| 2 | Enter a web address name (e.g., smart-registration) |
| 3 | Your URL will be: sites.google.com/view/smart-registration |
| 4 | Click Publish |

### Step 4: Custom Domain (Optional)

| Step | Action |
|------|--------|
| 1 | Click the Settings gear icon |
| 2 | Select Custom Domains |
| 3 | Click Start Setup |
| 4 | Enter your domain name |
| 5 | Follow instructions to add DNS records |
| 6 | Wait for verification (can take up to 24 hours) |

### Chapter 5 Checkpoint

- Form loads inside Google Sites without errors
- No scrollbars appear (form fits the frame)
- You can submit data from the embedded form
- Site is accessible via the published URL

---

## Bonus: Advanced Features

These prompts take your application to the next level.

### Bonus 1: File Uploads to Google Drive

---
Add a file upload feature to save PDFs to Google Drive.

FRONTEND UPDATES (index.html)

1. Add File Input:
   - Label: Upload Resume (PDF only)
   - Accept only PDF files: accept=.pdf
   - Max file size: 5MB
   - Show file name after selection

2. File Conversion:
   - Use FileReader API to convert file to Base64 string
   - This is required because Apps Script cannot receive file objects directly

3. Validation:
   - Check file type (must be PDF)
   - Check file size (must be < 5MB)
   - Show error if validation fails

BACKEND UPDATES (Code.gs)

4. Update processForm():
   - Accept file data (Base64 string, filename, mimetype)
   - Use DriveApp to save the file

5. Create saveFileToDrive() function:
   - Check if folder Form_Uploads exists, if not create it
   - Decode the Base64 string
   - Create the file in the folder
   - Rename file to match user name (e.g., John_Doe_Resume.pdf)
   - Return the file URL

6. Update Submissions Sheet:
   - Add Resume Link column
   - Save the Drive file URL in this column

7. Update initialSetup():
   - Add Resume Link to headers if missing

IMPORTANT NOTE:
Add a code comment reminding me to:
1. Run the script manually once in the editor to authorize Google Drive permissions
2. Grant Drive access when prompted

Provide the complete updated Code.gs and index.html.
---

### Bonus 2: Email Notifications

---
Add automatic email notification when someone submits the form.

BACKEND UPDATES (Code.gs)

1. Add Email Settings to initialSetup():
   Add these rows to Settings sheet:
   - Notification Email: your-email@gmail.com
   - Email Subject: New Form Submission
   - Send Notification: Yes

2. Create sendNotificationEmail() function:
   - Read email settings from Settings sheet
   - Only send if Send Notification is Yes
   - Use GmailApp.sendEmail()
   - Include all submitted data in email body
   - Format nicely with HTML

3. Update processForm():
   - Call sendNotificationEmail() after saving data
   - Pass form data to the function

4. Email Template:
   - Professional HTML formatting
   - Include timestamp
   - Include all form fields
   - Include link to Google Sheet

IMPORTANT NOTE:
Add a code comment reminding me to:
1. Run the script manually once to authorize Gmail access
2. The email will be sent from my Gmail account

Provide the updated Code.gs.
---

### Bonus 3: Duplicate Prevention

---
Prevent duplicate form submissions based on email address.

BACKEND UPDATES (Code.gs)

1. Create checkDuplicate(email) function:
   - Read all existing emails from Submissions sheet
   - Check if the submitted email already exists
   - Return true if duplicate, false if new

2. Update processForm():
   - Call checkDuplicate() before saving
   - If duplicate found, return error message:
     This email has already been registered
   - Only save if not a duplicate

FRONTEND UPDATES (index.html)

3. Handle Duplicate Error:
   - Display the error message from backend
   - Do not clear the form (so user can try different email)
   - Highlight the email field in red

Provide the updated Code.gs and index.html.
---

### Bonus 4: Custom Fields Template

Use this template to add any new field you want:

---
I need to add a new field to my form.

FIELD DETAILS:
- Field Name: [YOUR FIELD NAME, e.g., Company Name]
- Field Type: [text / dropdown / date / checkbox / radio / textarea / number]
- Required: [Yes / No]
- Options (if dropdown/radio): [Option 1, Option 2, Option 3]
- Placeholder Text: [e.g., Enter your company name]
- Validation: [e.g., Must be at least 3 characters]

UPDATES NEEDED:

1. Frontend (index.html):
   - Add the input field with proper styling
   - Match existing form design
   - Add validation if specified

2. Backend (Code.gs):
   - Update processForm() to receive this field
   - Update initialSetup() to add column header (check if exists first)

Please provide the updated code snippets.
---

### Bonus 5: Success Redirect

---
After successful form submission, redirect users to a thank you page.

SETTINGS UPDATE:
Add to Settings sheet:
- Redirect URL: https://yoursite.com/thank-you
- Redirect Delay: 3 (seconds)

FRONTEND UPDATES (index.html)

1. On Successful Submit:
   - Show success message: Form submitted successfully!
   - Show countdown: Redirecting in 3... 2... 1...
   - Redirect to the URL from settings

2. Handle No Redirect:
   - If Redirect URL is empty, just show success message
   - Do not redirect

Provide the updated index.html.
---

---

## Prompt Engineering Secrets

Master these techniques to get better code from AI every time:

### 1. Be Specific, Not Vague

Bad Prompt:
Make a form

Good Prompt:
Create an HTML form with fields for Name, Email, and Phone using Tailwind CSS with a centered card layout, shadow effect, and mobile-responsive design

### 2. Use Numbered Steps

Structure your prompts with clear sections so the AI does not miss anything:

BACKEND UPDATES (Code.gs)
1. Create function A that does X
2. Create function B that does Y

FRONTEND UPDATES (index.html)
1. Add element A with styling B
2. Add logic for C

IMPORTANT NOTES
- Remember to handle edge case X
- Do not forget about Y

### 3. Specify the Tech Stack

Always mention the technologies you are using:
- Google Apps Script
- Code.gs and index.html
- Tailwind CSS
- jQuery (if using)
- Select2 (if using)

### 4. Ask for Edge Cases

Add phrases that catch potential bugs:
- Handle errors gracefully with try-catch
- What if the cell is empty or undefined?
- Prevent double-clicking the submit button
- Show loading state while processing
- Handle API timeout or failure

### 5. Iterate and Refine

Your first prompt rarely produces perfect code. Use follow-ups:
- The timer resets when I refresh the page. Fix this using localStorage.
- Add a loading spinner while the API fetches country data.
- The submit button should be disabled until all required fields are filled.
- Add form validation—email must be valid format, phone must be 10 digits.

### 6. Debug with AI

When you encounter errors, use this template:

I am getting this error in Google Apps Script:

ERROR MESSAGE:
[Paste the exact error here]

MY CODE:
[Paste the relevant code section]

What is wrong and how do I fix it?

### 7. Request Explanations

Learn while you build:
- Add comments explaining what each section does.
- Explain why you chose this approach over alternatives.
- What are the potential issues with this code?

---

## Real-World Use Cases

Here is what you can build using this system:

### Education

| Use Case | Features to Implement |
|----------|----------------------|
| Exam Registration | Deadline + Timer + Duplicate Prevention |
| Assignment Portal | File Upload + Email Notification |
| Event RSVP | Dropdown Options + Custom Domain |
| Student Feedback | Anonymous Submission + Data Validation |
| Workshop Signup | Seat Limits + Auto-Close When Full |
| Course Enrollment | Multi-Page Form + Payment Link |
| Alumni Registration | Conditional Fields + Photo Upload |
| Library Book Request | Dropdown Selection + Email Confirmation |

### Business

| Use Case | Features to Implement |
|----------|----------------------|
| Job Applications | File Upload (Resume) + Email Alerts |
| Customer Orders | Product Dropdowns + Order ID Generation |
| Vendor Registration | Multiple File Uploads + Approval Workflow |
| IT Support Tickets | Priority Dropdown + Auto-Assignment |
| Employee Surveys | Anonymous Mode + Department Filtering |
| Expense Claims | Receipt Upload + Manager Notification |
| Meeting Room Booking | Date/Time Picker + Conflict Check |
| Client Onboarding | Multi-Step Form + Document Collection |

### Events

| Use Case | Features to Implement |
|----------|----------------------|
| Conference Registration | Session Selection + Payment Link |
| Wedding RSVP | Meal Preferences + Plus-One Counter |
| Competition Entry | File Upload + Submission Timer |
| Webinar Signup | Calendar Integration + Reminder Emails |
| Volunteer Application | Skill Checkboxes + Availability Matrix |
| Concert Tickets | Seat Selection + QR Code Generation |
| Sports Tournament | Team Registration + Player List |
| Workshop Waitlist | Auto-Notify When Spot Opens |

---

## Troubleshooting Cheat Sheet

### Common Errors and Solutions

| Problem | Solution |
|---------|----------|
| Script function not found | Select the correct function (e.g., initialSetup) from the dropdown before clicking Run |
| Changes not showing on live form | You must deploy a New Version. Saving alone does not update the live app. |
| #ERROR! in Phone column | Add a single quote before the phone string in Code.gs to force text format |
| Images/logos not loading | Ensure Google Drive images are shared as Anyone with the link can view |
| Authorization required popup | Run the script once manually in the editor to grant permissions |
| Refused to connect on Google Sites | Add setXFrameOptionsMode(ALLOWALL) to doGet() function |
| API returns empty data | Check browser console (F12) for errors. API might be rate-limited or down. |
| Form submits but no data in sheet | Field names in HTML must match exactly (case-sensitive) with Code.gs |
| Timer resets on page refresh | localStorage is not working—check for typos in the key name |
| Dropdown shows undefined | API response structure changed—log the response to see actual format |
| Form does not submit | Check browser console for JavaScript errors (F12 then Console tab) |
| Cannot read property of null | An element ID is wrong or element does not exist in HTML |
| Settings not loading | Check Settings sheet has exactly matching row names |
| Deadline not working | Timezone mismatch—ensure using Asia/Kolkata consistently |
| Email not sending | Run script manually once to authorize Gmail access |

### Debug Prompt Template

When stuck, copy this template to AI:

I am building a Google Apps Script web form and encountering an error.

THE ERROR:
[Paste exact error message from browser console or Apps Script]

WHAT I EXPECTED:
[Describe what should happen]

WHAT ACTUALLY HAPPENS:
[Describe what is going wrong]

MY CODE:

Code.gs:
[Paste relevant section]

index.html:
[Paste relevant section]

Please identify the issue and provide the fix.

### Quick Fixes Checklist

When something breaks, check these first:
- Did you save both files? (Ctrl+S)
- Did you deploy a NEW version? (Not just save)
- Did you clear browser cache? (Ctrl+Shift+R)
- Is the correct function selected in dropdown?
- Did you grant all permissions when prompted?
- Are all your quotation marks straight not curly?
- Did you check browser console for errors? (F12)
- Are field names matching exactly (case-sensitive)?
- Is the Google Sheet tab named correctly?
- Did you run initialSetup after adding new features?

---

## Glossary for Non-Coders

| Term | Plain English Explanation |
|------|---------------------------|
| API | A messenger that fetches data from other websites. Like a waiter taking your order to the kitchen and bringing back food. |
| Backend | The behind the scenes logic that users do not see. Like the kitchen in a restaurant. |
| Frontend | What users actually see and interact with. Like the dining area of a restaurant. |
| Deploy | Publishing your code so it becomes a live website anyone can access. |
| Serverless | Your app runs without you managing a server—Google handles all the technical stuff. |
| localStorage | A small storage space in the user browser that remembers data even after refresh. |
| Tailwind CSS | A styling library that makes forms look modern using simple class names. |
| IST | Indian Standard Time (UTC+5:30). The timezone used for deadlines. |
| Base64 | A way to convert files (like images) into text so they can be sent through the internet. |
| CMS | Content Management System—a way to update your website without coding (like WordPress). |
| CDN | Content Delivery Network—a way to load libraries quickly from external servers. |
| JSON | JavaScript Object Notation—a format for storing and sending data (looks like organized text). |
| iframe | A way to embed one website inside another website. |
| Callback | A function that runs after another function completes (like call me back when you are done). |
| Dropdown | A menu that expands when clicked to show options. |
| Validation | Checking if user input is correct (e.g., email has @, phone has 10 digits). |
| Responsive | Design that automatically adjusts to look good on any screen size (phone, tablet, desktop). |

---

## About the Author

Mr. Nilesh Vijay Sabnis

Assistant Professor | Automation & Robotics Specialist

Nilesh is an educator and automation expert passionate about democratizing technology. He specializes in helping non-coders build professional software solutions using Artificial Intelligence.

Mission:
Make software development accessible to everyone, regardless of coding background.

Focus Areas:
- No-Code/Low-Code Solutions
- AI-Assisted Development
- Google Workspace Automation
- Educational Technology
- Prompt Engineering

Philosophy:
The best code is the code you never had to write yourself.

---

## Copyright and Legal Disclaimer

© 2026 Nilesh Vijay Sabnis. All Rights Reserved.

No part of this publication may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical reviews and certain other noncommercial uses permitted by copyright law.

### Disclaimer

The code snippets and prompts provided in this book are for educational purposes only. While every effort has been made to ensure the accuracy of the information, the author assumes no responsibility for errors or omissions, or for damages resulting from the use of the information contained herein.

### Trademarks

- Google, Google Sheets, Google Apps Script, Google Sites, and Google Drive are trademarks of Google LLC.
- ChatGPT is a trademark of OpenAI.
- Claude is a trademark of Anthropic.
- Gemini is a trademark of Google LLC.

This book is not endorsed by or affiliated with any of the above companies.

### License for Code

All code examples in this book are provided under the MIT License. You are free to use, modify, and distribute the code for personal and commercial purposes, with attribution.

---

## Acknowledgments

Special thanks to:
- The Batch 5 workshop participants for their enthusiasm and feedback
- The open-source community for the tools that make this possible
- Google for providing free, powerful development tools
- AI assistants for making coding accessible to everyone

---

Congratulations!

You have completed THE AI FORM ARCHITECT. You now have the skills to build professional web applications using nothing but natural language prompts.

Remember: English is the new programming language.

Now go build something amazing!

---

# COMPANION CHEAT SHEET

## Quick Reference Card for Building Google Sheets + AI Web Forms

Author: Nilesh Vijay Sabnis | Version: 1.0 | February 2026

---

## Quick Start (5 Minutes)

| Step | Action |
|------|--------|
| 1 | Open sheets.new then Name it Smart Form System |
| 2 | Extensions then Apps Script |
| 3 | Create index.html file (click + then HTML) |
| 4 | Copy prompts then Paste into ChatGPT/Claude/Gemini |
| 5 | Paste AI output into Apps Script files |
| 6 | Deploy then New Deployment then Web App then Anyone |

---

## The Golden Rule

Always deploy a NEW VERSION after making changes!

1. Save files (Ctrl+S)
2. Deploy then Manage Deployments
3. Click Pencil (Edit) icon
4. Version: New Version
5. Click Deploy

Saving alone does NOT update your live form!

---

## Architecture Overview

FRONTEND (index.html) connects to BACKEND (Code.gs) connects to DATABASE (Google Sheet)

User sees form then Processes data then Stores responses

---

## Essential Code Snippets

### Complete doGet() with Embedding

function doGet() {
  var template = HtmlService.createTemplateFromFile('index');
  template.settings = getSettings();
  return template.evaluate()
    .setTitle('Smart Form')
    .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL);
}

### Fix Phone Number Error

// In processForm(), before saving phone:
var phoneNumber = "'" + formData.phone; // Prepend single quote

### Timezone Handling

var now = Utilities.formatDate(new Date(), "Asia/Kolkata", "yyyy-MM-dd HH:mm");

### localStorage Timer

// Save timer
localStorage.setItem('formTimer', remainingSeconds);

// Load timer
var saved = localStorage.getItem('formTimer');
if (saved) {
  remainingSeconds = parseInt(saved);
}

### Check for Duplicates

function checkDuplicate(email) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName('Submissions');
  var data = sheet.getDataRange().getValues();
  for (var i = 1; i < data.length; i++) {
    if (data[i][4] === email) {
      return true;
    }
  }
  return false;
}

---