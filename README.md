# 🤖 JobFit Auto-Apply Agent  
An AI-powered workflow built using **n8n** that automatically analyzes resumes, extracts job description requirements, performs skill gap analysis, generates application materials (summary, resume bullet points, cover letter, HR email), and directly emails the result in a professional format.

---

## 🚀 Features

✔ Upload Resume (PDF) and Job Description via Form  
✔ Cleans and extracts text using JavaScript  
✔ Uses Gemini AI to parse both resume and JD into structured JSON  
✔ Skill Gap Analyzer – detects missing, matched, and under-emphasized skills  
✔ Automatically generates:
- Resume summary
- Role-specific bullet points
- Cover Letter
- HR Email Template  
✔ Formats final output in HTML and Markdown  
✔ Sends final application pack via Gmail — ready to send to HR  

---

## 🛠 Tech Stack

| Component | Technology |
|-----------|------------|
| Workflow Automation | n8n |
| AI Processing | Gemini AI Model (Google AI) |
| Resume & JD Extraction | Extract From File (PDF to Text) |
| Logic & Structuring | JavaScript Function Nodes |
| Email Service | Gmail API Integration |
| Data Handling | Merge, HTML, JSON nodes |

---

## 📌 Workflow Overview

1️⃣ **On Form Submission** – User uploads Resume PDF and pastes Job Description text  
2️⃣ **Extract From File** – Extracts text content from PDF resume  
3️⃣ **Text Cleaning** – Prepares both resume and JD text for AI processing  
4️⃣ **Basic LLM (Gemini AI)** – Parses JD into structured JSON (skills, responsibilities, keywords)  
5️⃣ **JD Extraction & Storage** – Validates and stores structured JD and cleaned resume  
6️⃣ **Skill Gap Analyzer** – Compares resume with job requirements  
7️⃣ **Application Pack Generator** – Creates summary, bullet points, cover letter, HR email  
8️⃣ **Formatter Node (HTML)** – Formats everything beautifully  
9️⃣ **Gmail Node** – Sends final formatted application pack to user via email  

---

## 📩 Email Format & Output

The email sent contains:

✨ **Job Description Summary**  
📄 **Resume Bullet Points (Job-Aligned)**  
📝 **Personalized Cover Letter**  
📧 **HR Application Email Draft**  
📎 *Ready to be copied, refined, and sent to recruiters*

---

## 🧠 Skill Gap Analyzer Output Example

```json
{
  "matched_skills": ["Content Writing", "Research", "Communication"],
  "missing_skills": ["SEO", "AI Blog Writing", "Market Analysis"],
  "resume_weak_areas": [
    "SEO optimization not clearly mentioned",
    "Job-relevant content writing missing"
  ],
  "extra_points_to_add": ["Content Strategy", "Tech Blog Writing"]
}
