# 🤖 Saudi Labor Law AI Legal Assistant

A local-first, document-aware AI assistant trained on Saudi Arabian labor policy. Designed for lawyers, HR teams, and business owners needing quick legal insights without relying on cloud-based LLMs. Built in Python with calendar management, logging, and automated email alerts.

---

## 🧠 Features

- ✅ Natural language Q&A under **Saudi Arabian Labor Law**
- 📄 Policy-aware: reads from official `labor_law.pdf`
- 📅 Integrates with **Google Calendar** (view, create, delete events)
- 📊 Logs all interactions to **Google Sheets**
- 📧 Notifies your legal team via **email**
- 🔐 Local execution, no backend, **privacy-respecting**

---

## ⚙️ Requirements

Install dependencies:

```bash
pip install -q openai google-api-python-client google-auth google-auth-oauthlib \
google-auth-httplib2 gspread oauth2client PyMuPDF dateparser
```
---

📂 Setup
Upload required files:

service_account.json (for Sheets access)

credentials.json (for Calendar access)

labor_law.pdf (your legal document or policy)

Run in Google Colab or locally

You'll be prompted for:

Your OpenRouter API key

Google OAuth authorization code (once)

Your Gmail app password (for alerts)

---

🔐 Security Notes
Gmail notifications use App Passwords — never hardcode real passwords.

All policy data and chat history remain local and private.

The OpenRouter model used is deepseek-r1, but you can change it.

---

🗂️ Usage
Start the assistant:
python ai_legal_agent.py

Then interact:
Ask your legal question (or type 'quit agent' to exit): What are the working hours under Saudi law?

🤖 Response:
The standard working hours in Saudi Arabia are...

🔄 Auto-detects calendar intents
Add Events:

"Schedule a meeting titled 'Contract Review' tomorrow at 3 PM"

Delete Events:

"Cancel the 'HR Meeting' at 1 PM today"

---

📡 Architecture
[User Input]
     ↓
[LLM via OpenRouter] ← embeds policy PDF
     ↓
[Intent Detection]
  ↙        ↘
[Calendar]  [Logging + Email Alerts]

---

🧪 Example Output
🧠 Question: What’s the minimum age to work in Saudi Arabia?
🤖 Answer: Under Saudi Labor Law, the minimum working age is...

---

📌 Roadmap
 Refactor the entire agent into a class-based architecture

 Encapsulate each tool (calendar, email, logging) as modular APIs/services

 Improve abstraction and reusability for deployment or expansion to other legal domains

---

🛡️ License
MIT License — feel free to modify or extend for your legal practice.

---

👨‍💻 Author
Made by Ahmad Fares Mzayek
