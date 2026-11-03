#  AI-Powered Coach Practice System

![AI](https://img.shields.io/badge/AI-Interview%20Coaching-7B61FF?style=flat)
![n8n](https://img.shields.io/badge/Automation-n8n-FF6D5A?style=flat&logo=n8n&logoColor=white)
![Next.js](https://img.shields.io/badge/Frontend-Next.js-000000?style=flat&logo=next.js&logoColor=white)
![OpenAI](https://img.shields.io/badge/AI%20Processing-OpenAI-412991?style=flat&logo=openai&logoColor=white)
![LlamaParse](https://img.shields.io/badge/Document%20Parsing-LlamaParse-6B4EFF?style=flat)

---

## 📺 System Walkthrough

🎥 Watch the complete demonstration of the AI Coach Practice System:

https://www.loom.com/share/ce6077592a2e4ce585092d8268c05152

---

## 🚀 Project Overview

The **AI-Powered Coach Practice System** helps candidates prepare for job interviews through personalized AI-generated questions, voice-based practice sessions, and instant AI feedback.

Candidates upload their resume, enter their personal details, and begin an interactive coaching session. The system processes their resume to generate targeted, experience-based interview questions, allowing candidates to practise speaking their answers and improve their interview readiness.

The platform combines an interactive AI coaching interface with automated n8n workflows for resume processing, candidate verification, question generation, and AI-powered evaluation.

---

## 🎯 System Purpose

The primary objective is to help candidates prepare for real interviews by providing a personalized practice environment based on their resume and experience.

**Key capabilities include:**

- 📄 Resume / CV Upload
- 🎯 Resume-Based Interview Questions
- 🤖 AI-Powered Interview Coaching
- 🎙️ Voice-Based Practice
- 💬 Interactive Conversation Interface
- ⏱️ Interview Session Time Tracking
- 🧠 AI-Powered Answer Evaluation
- 💡 Instant Feedback and Improvement Insights
- 🔄 Automated Resume Processing
- 🚫 Duplicate Candidate Checks

---

## 🖥️ Application Interface

### 1️⃣ AI Coach Landing Page & Resume Submission

Candidates begin by visiting the AI Coach application and entering their details.

**Required information:**
- Full Name
- Email Address
- Resume / CV Upload (PDF or DOCX)

The system uses the uploaded resume to generate targeted, experience-based interview questions.

The landing page introduces three main features:

- **🎯 Targeted Questions:** Questions based on the candidate's resume and role goals.
- **🎙️ Voice Practice:** Practise speaking naturally and build confidence.
- **💡 Instant Feedback:** Receive AI-powered insights to improve answers before the actual interview.

<div align="center">
  <img src="ai-coach-landing-page.jpeg" width="100%" alt="AI Coach Landing Page and Resume Submission"/>
</div>

---

### 2️⃣ Interactive AI Coaching Session

After submitting their details and resume, candidates enter the AI coaching session.

The interface provides an interactive practice environment with an AI coach avatar and a live conversation area.

**Session interface includes:**

- AI Coach Video Interface
- Live Conversation Panel
- Candidate Information
- Total Question Counter
- Interview Session Timer
- Start Interview Control
- End Interview Control

The displayed practice session includes **5 questions** and a **12-minute session duration**.

Candidates can practise answering questions through voice interaction in a simulated interview environment.

<div align="center">
  <img src="ai-coach-practice-session.jpeg" width="100%" alt="AI Coach Live Practice Session"/>
</div>

---

## 🔄 Complete System Workflow

The system connects candidate registration, resume processing, AI question generation, and coaching preparation through automated workflows.

```text
Candidate Opens AI Coach Application
                ↓
         Enters Personal Details
                ↓
          Uploads Resume / CV
                ↓
         Application Webhook
                ↓
       Candidate Record Lookup
                ↓
       Existing Candidate Check
                ↓
       Candidate Status Validation
                ↓
        Resume Upload Processing
                ↓
          LlamaParse Processing
                ↓
         Resume Text Extraction
                ↓
          Resume Validation
                ↓
       OpenAI Structured Processing
                ↓
       AI Question & Answer Data
                ↓
         Coaching Session Setup
                ↓
       Interactive Voice Practice
                ↓
          AI-Powered Feedback
```

---

## ⚙️ Backend Automation with n8n

The backend automation is managed through n8n workflows, connecting candidate submissions, resume processing, AI services, and data management.

### 3️⃣ Resume Ingestion & Candidate Processing

When a candidate submits their information, the application sends the data to an n8n webhook.

The workflow handles:

- Receiving candidate submission data.
- Retrieving existing candidate records.
- Checking candidate status.
- Identifying existing submissions.
- Managing candidate processing paths.
- Responding to the application through webhooks.

### 4️⃣ Resume Parsing & Validation

The uploaded resume is processed using LlamaParse.

The workflow handles:

- Uploading the resume for parsing.
- Waiting for the parsing process to complete.
- Retrieving extracted resume text.
- Checking parsing status.
- Validating extracted resume content.
- Checking whether the extracted text meets the required length.

This prepares structured resume information for the AI processing stage.

### 5️⃣ AI-Powered Question Generation & Processing

After successful resume processing, the extracted information is sent to an OpenAI-powered workflow.

The workflow uses structured JSON processing to organize AI-generated question and answer information for the coaching system.

This supports personalized interview practice based on the candidate's resume and experience.

<div align="center">
  <img src="n8n-ai-coach-workflow.jpeg" width="100%" alt="Complete n8n AI Coach Workflow"/>
</div>

---

### 6️⃣ Candidate Duplicate Prevention

The system includes a separate candidate validation workflow to check whether a candidate has already completed or submitted an existing coaching session.

The workflow:

- Receives candidate information through a webhook.
- Retrieves existing candidate records.
- Checks the candidate's status.
- Merges and evaluates candidate information.
- Routes records based on their status.
- Separates duplicate and non-duplicate submissions.

This helps prevent duplicate candidate processing.

<div align="center">
  <img src="n8n-duplicate-check-workflow.jpeg" width="100%" alt="n8n Candidate Duplicate Prevention Workflow"/>
</div>

---

## 🧠 Core Technical Pillars

- **🤖 AI Interview Coaching:** Provides an AI-powered environment for interview preparation.
- **📄 Resume-Based Personalization:** Uses uploaded resumes to generate targeted practice questions.
- **🎙️ Voice Practice:** Allows candidates to practise speaking their answers.
- **💡 AI Feedback:** Provides AI-powered insights to help candidates improve their responses.
- **⚙️ Workflow Automation:** Uses n8n to coordinate candidate submissions and processing.
- **📑 Resume Parsing:** Uses LlamaParse to extract information from uploaded documents.
- **🧠 Structured AI Processing:** Uses OpenAI to process resume information and generate structured question and answer data.
- **🔍 Candidate Validation:** Checks existing records and candidate status.
- **🚫 Duplicate Prevention:** Identifies existing submissions before processing candidates again.

---

## 🛠️ Technical Stack

| Layer | Technology |
|---|---|
| **Frontend Application** | Next.js |
| **Programming Language** | TypeScript / JavaScript |
| **Workflow Automation** | n8n |
| **AI Processing** | OpenAI |
| **Resume Parsing** | LlamaParse |
| **Backend Integration** | Webhooks & APIs |
| **Candidate Processing** | Automated n8n Workflows |
| **Interview Experience** | Voice-Based AI Coaching Interface |

---

## 🔄 System Architecture

```text
             AI COACH APPLICATION
                      ↓
             Candidate Registration
                      ↓
               Resume Upload
                      ↓
                n8n Webhook
                      ↓
           Candidate Data Validation
                      ↓
             Duplicate Check
                      ↓
             Resume Processing
                      ↓
                 LlamaParse
                      ↓
            Extracted Resume Text
                      ↓
              Resume Validation
                      ↓
            OpenAI AI Processing
                      ↓
         Structured Questions & Answers
                      ↓
             AI COACH INTERFACE
                      ↓
          Interactive Practice Session
                      ↓
             Voice-Based Answers
                      ↓
              AI-Powered Feedback
```

---

## 🚀 Business Impact

The system transforms traditional interview preparation into a personalized AI-powered practice experience.

### Before Automation

**Search Interview Questions → Read Generic Questions → Prepare Answers Manually → Practise Without Feedback → Identify Weaknesses Independently**

### After Automation

**Upload Resume → Generate Targeted Questions → Start AI Coaching Session → Practise Through Voice → Receive AI Feedback → Improve Interview Answers**

### Key Benefits

- **🎯 Personalized Preparation:** Generates questions based on individual resume information.
- **🎙️ Speaking Practice:** Helps candidates practise verbal responses.
- **💡 Immediate Insights:** Provides AI-powered feedback to support improvement.
- **⏱️ Structured Sessions:** Organizes practice around a defined question count and session duration.
- **⚙️ Automated Processing:** Reduces manual work involved in resume preparation and question generation.
- **🚀 Interview Readiness:** Helps candidates prepare more effectively for actual job interviews.

---

## 📌 Key Result

The AI-Powered Coach Practice System connects resume parsing, personalized question generation, voice-based practice, and AI-powered feedback in one automated platform.

**Resume Upload → Resume Parsing → AI Question Generation → Interactive Voice Practice → AI Feedback → Interview Preparation**

The result is an AI-powered coaching experience that helps candidates practise with questions relevant to their experience and improve their confidence before real interviews.

---

## ✍️ Author

**Muneeb Ali Khan**

**AI Automation & GTM Engineer**

- **LinkedIn:** [Muneeb Ali Khan](https://www.linkedin.com/in/muneeb-ali-khan-2a1675365)
