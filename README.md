# **n8n-Automated-Resume-Screening-Workflow**

🚀 **AI-Powered Resume ATS Checker (n8n Workflow)**
An automated resume-screening system built using **n8n**, **Telegram Bot**, **Google Sheets**, and **LLM (AI)**.
This workflow processes uploaded **PDF** resumes or **ZIP files** containing multiple PDFs, analyzes them using AI, generates ATS scores, and automatically updates the results in Google Sheets.

---

## 📸 **Workflow Snapshot**

<img width="1916" height="923" alt="resume shortlisting" src="https://github.com/user-attachments/assets/3c5d9095-fbad-4e2b-afbe-ba864840e886" />



## 🔥 **Key Features**

* 📤 Upload resumes via **Telegram** (supports **PDF** + **ZIP**).
* 🤖 **AI-powered ATS Scoring** using Gemini/LLM.
* 🧠 Auto-classifies:

  * **Accepted** (Score ≥ 70)
  * **Rejected** (Score < 70)
* 📊 Saves structured results into **Google Sheets**.
* 📩 Automatically sends Accepted/Rejected messages back to the user.
* 📦 ZIP support: extracts and processes multiple resumes inside ZIP files.
* ⚡ Fully automated end-to-end workflow.

---

## 📌 **Workflow Steps**

1. **Telegram Trigger**

   * Bot receives file (PDF/ZIP) from the user.

2. **File Type Switch**

   * If **PDF →** Direct ATS evaluation
   * If **ZIP →** Extract & loop through all PDFs

3. **Text Extraction**

   * Extracts text from PDF files.

4. **AI Resume Analysis**

   * Generates:

     * ATS Score
     * Keyword match
     * Skills match
     * Strengths
     * Weak sections

5. **Result Classification**

   * Score ≥ 70 → Added to **Accepted Sheet**
   * Score < 70 → Added to **Rejected Sheet**

6. **Google Sheets Update**

   * Appends structured row containing:

     * Name
     * Email
     * Score
     * Status
     * Date/Time

7. **Auto Reply to User**

   * Sends appropriate message with summary.

---

## 🛠️ **Tech Stack**

* **n8n Workflow Automation**
* **Telegram Bot API**
* **Google Sheets API**
* **Gemini / LLM (AI Model)**
* **PDF & ZIP File Handling**

---

## ▶️ **How to Use**

1. Download the provided **workflow JSON**.
2. Import it into **n8n**.
3. Add credentials:

   * Telegram Bot API Key
   * Google Sheets OAuth Credentials
4. Start the workflow.
5. Send a PDF/ZIP to your Telegram bot.
6. Watch automation do the rest automatically 🚀

---
