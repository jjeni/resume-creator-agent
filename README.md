
# 🧠 Resume Editor AI Agent

**Resume Editor AI Agent** is an AI-powered automation workflow built using **n8n**, **Google Gemini (PaLM)**, and **Google Workspace APIs**.  
It automatically edits a resume template based on a given **Job Title** and **Job Description**, generating customized summaries, skills, experience, certificates, and projects.

---

<img width="884" height="741" alt="image" src="https://github.com/user-attachments/assets/906d3a91-6a66-496b-b3bc-7f1252c4d43a" />


## 🚀 Key Features

- **AI-Generated Summary** – Creates a professional summary aligned with the target job.  
- **Smart Skill Extraction** – Lists both technical and soft skills relevant to the role.  
- **AI-Written Experience Section** – Generates realistic work experience lines.  
- **Certificates & Projects Generator** – Adds role-related certificates and creative projects.  
- **Automated Resume Editing** – Replaces placeholders in Google Docs automatically.  
- **End-to-End Automation** – Reads job data, generates AI output, and exports the resume to Google Drive.

---

## 🧩 Workflow Overview

1. **Trigger Node** – Manually starts the workflow in n8n.  
2. **Google Sheets** – Reads Job Title & Job Description.  
3. **Google Drive** – Copies the base resume template.  
4. **Gemini AI** – Generates summary, skills, experience, certificates, and projects.  
5. **Google Docs** – Replaces placeholders in the document with AI-generated text.  
6. **Google Drive Download** – Saves or exports the final resume as a `.pdf`.

---

## ⚙️ Tech Stack

| Tool / API | Purpose |
|-------------|----------|
| 🧩 **n8n** | Orchestrates workflow automation |
| 🤖 **Google Gemini (PaLM)** | AI model for text generation |
| 📄 **Google Docs API** | Edits resume template |
| 📊 **Google Sheets API** | Fetches job input |
| ☁️ **Google Drive API** | Stores the final resume |
| 💡 **JavaScript Node (Code)** | Parses and maps project placeholders |

---

## 📂 Folder Structure

```
resume-editor-ai-agent/
│
├── Resume_Editor_Agent_Public.json    # Sanitized n8n workflow
├── README.md                          # Project documentation
│
├── assets/
│   └── workflow-diagram.png           # Optional visual workflow
│
├── templates/
│   └── resume_template.docx           # Resume template with placeholders
│
└── examples/
    └── sample-output.pdf              # Example generated resume
```

---

## ⚙️ Setup Instructions

### 1️⃣ Requirements

- n8n (self-hosted or [n8n.cloud](https://n8n.cloud))
- Google Cloud project (for Drive, Docs, and Sheets APIs)
- Gemini (PaLM) API key

### 2️⃣ Environment Setup

In n8n, create the following environment variables (**Settings → Variables**):

```env
GOOGLE_EMAIL=your_service_account_email
GOOGLE_PRIVATE_KEY=your_private_key
GEMINI_API_KEY=your_gemini_api_key
```

### 3️⃣ Import Workflow

1. Open n8n → Click **Import from File**  
2. Upload `Resume_Editor_Agent_Public.json`  
3. Connect your **Google Sheets**, **Google Docs**, **Google Drive**, and **Gemini** credentials.

### 4️⃣ Resume Template Setup

Create a **Google Docs** resume template with placeholders:

```
{{summary_placeholder}}
{{skills_placeholder}}
{{experience_placeholder}}
{{certificate_placeholder}}
{{PROJECT_TITLE1_PLACEHOLDER}}
{{project1_placeholder}}
```

### 5️⃣ Run the Workflow

1. Enter Job Title & Description in the connected Google Sheet.  
2. Execute the workflow in n8n.  
3. A new resume will be generated and saved to your Google Drive — ready to share! 🚀

---

## 🧾 Example Output

| Section | Example Output |
|----------|----------------|
| **Summary** | “Creative Frontend Developer skilled in React.js and TypeScript…” |
| **Skills** | React.js, Tailwind CSS, API Integration, Collaboration |
| **Experience** | Worked as a Frontend Developer at Techigen… |
| **Certificates** | “Advanced Frontend Development, by Coursera” |
| **Projects** | “Smart Portfolio – A React-based portfolio builder.” |

---

## 🧠 Future Enhancements

- [ ] Add **email automation** to send resumes directly.  
- [ ] Integrate **LinkedIn job scraping** for auto-fetching descriptions.  
- [ ] Support **multiple templates** for different roles.  
- [ ] Create a **web dashboard** for easier control.

---

## 👩‍💻 Author

**Jeni J.**  
AI Workflow Engineer | Web Developer | Automation Builder  

- 🌐 [GitHub](https://github.com/jjeni)  
- 💼 [LinkedIn](https://linkedin.com/in/jeni-j)  

