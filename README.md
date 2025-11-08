🧠 **Resume Editor AI Agent**

Resume Editor AI Agent is an automated AI workflow built using n8n, Google Gemini (PaLM), and Google Workspace APIs.
It takes a Job Title and Job Description as input and generates a customized, professional resume updating the summary, skills, experience, certificates, and project sections automatically.

🚀 **Key Features**

✅ **AI-Generated Summary**
Creates a professional 4-5 line summary aligned with the provided job title and job description.

✅ **Smart Skill Extraction**
Analyzes the job post and lists relevant technical and soft skills.

✅ **AI-Written Experience Section**
Generates short, realistic work experiences to match the role.

✅ **Certificates & Projects Generator**
Adds fake yet relevant certificate titles and project ideas for resume enhancement.

✅ **Automated Resume Editing**
Updates placeholders (e.g., {{summary_placeholder}}, {{skills_placeholder}}, etc.) in your Google Docs resume template and saves it automatically to Google Drive.

✅ **No Manual Editing Needed**
The workflow handles everything — from reading job info to saving the final polished resume.

🧩 **Workflow Overview**

1. Trigger Node – Starts the workflow manually in n8n.

2. Google Sheets Node – Reads Job Title & Job Description from a Google Sheet.

3. Google Drive Node – Copies a base resume template into a new file.

4. LLM Chains (Gemini) –

5. Writes Summary

6. Suggests Skills

7. Generates Experience, Certificates, and Projects

8. Google Docs Nodes – Replace placeholders in the copied template with AI-generated content.

9. Google Drive Download Node – Saves or exports the updated resume as a .pdf.

⚙️**Tech Stack**
Tool / API	Purpose
🧩 n8n	Orchestrates workflow automation
🤖 Google Gemini (PaLM API)	AI model for text generation
📄 Google Docs API	Edits resume template
🧾 Google Sheets API	Fetches job input
☁️ Google Drive API	Stores final resume
💡 JavaScript Node (Code)	Parses and maps multiple project placeholders

🧱 **Folder Structure**
resume-creator-agent/
│
├── Resume_Editor_Agent_Public.json   # Sanitized n8n workflow
├── README.md                         # Project documentation
├── assets/
│   └── workflow-diagram.png           # Optional visual workflow
|   └── resume_template.docs           # Resume Template
└── examples/
    └── sample-output.pdf              # Example generated resume
    

⚙️ **Setup Instructions**
1️⃣ Requirements

n8n (self-hosted or n8n.cloud)

Google Cloud account (for Drive, Docs, and Sheets APIs)

Gemini (PaLM) API key

2️⃣ Environment Setup

In n8n, create these environment variables (Settings → Variables):

GOOGLE_EMAIL=your_service_account_email
GOOGLE_PRIVATE_KEY=your_private_key
OPENAI_API_KEY=your_gemini_api_key

3️⃣ Import the Workflow

Open n8n editor

Click Import from File

Choose Resume_Editor_Agent_Public.json

Configure credentials (Google Sheets, Docs, Drive, and Gemini)

4️⃣ Prepare Google Docs Template

Create a resume template with placeholders such as:

{{summary_placeholder}}
{{skills_placeholder}}
{{experience_placeholder}}
{{certificate_placeholder}}
{{PROJECT_TITLE1_PLACEHOLDER}}
{{project1_placeholder}}

5️⃣ Run the Workflow

Enter Job Title & Job Description in your linked Google Sheet

Click Execute Workflow

The AI agent generates a personalized resume and saves it to your Google Drive 🚀

📸 **Example Flow**

Section	Output Example
Summary	“Creative Frontend Developer skilled in React.js and UI optimization…”
Skills	React.js • TypeScript • Tailwind CSS • API Integration • Collaboration
Experience	Worked as Frontend Engineer at Techigen…
Certificates	“Advanced Frontend Development, by Coursera”
Projects	“Smart Portfolio – A React-based personal portfolio generator.”

🧠 **Future Enhancements**

 Add email automation to send resumes directly to recruiters.
 Integrate LinkedIn job scraping for auto-fetching descriptions.
 Support multiple templates per role.
 Create web dashboard to upload resumes and track edits.

👩‍💻 **Author**

Jeni J.
AI Workflow Engineer | Web Developer | Automation Builder

🌐 GitHub - https://github.com/jjeni/
💼 LinkedIn - https://www.linkedin.com/in/jeni-j/

