# meetmind

AI-powered meeting assistant that records, transcribes, summarizes discussions, and shares key decisions with your team.

---

## 🛠 Project Overview

MeetMind is a full-stack project with a Go backend and a frontend built using **HTML, CSS, and JavaScript**. It allows users to:

1. Upload meeting recordings
2. Automatically transcribe audio using **Whisper API**
3. Summarize discussions and extract tasks/decisions using **GPT API**
4. Store transcripts and summaries in a database
5. View meeting summaries on a web frontend

---

## 📂 Project Structure

```
/backend        # Go backend (API, DB interactions, Whisper/GPT integration)
    /cmd/app/main.go       # entry point
    /internal/handlers     # upload, process, list
    /internal/services     # ai_service.go, pdf_service.go, mail_service.go
    /internal/repository   # db process
    /internal/models       # Meeting, Task, Decision
    /db                    # PostgreSQL / migration / seed dosyaları
    /configs/config.yaml   # API keys, DB path (gitignore)
/frontend       # HTML, CSS, JS frontend
```

---

## ⚡ Features

* **Upload & Transcribe** – Upload meeting audio and generate transcripts automatically.
* **Summarize & Extract** – Use GPT to create concise summaries and task lists.
* **Database Storage** – Save meetings, transcripts, summaries, and task info.
* **Frontend Interface** – View, select, and manage meetings and summaries.
* **Secure & Local** – API keys managed via `.env`, no raw audio stored externally.

---

## 📝 Getting Started

1. Clone the repository:

```bash
git clone https://github.com/yourusername/meetmind.git
cd meetmind
```

2. Initialize Go module:

```bash
cd backend
go mod init github.com/yourusername/meetmind
```

3. Set environment variables in `.env`:

```
OPENAI_API_KEY=sk-XXXXXX...
DB_PATH=./db/meetmind.db
```

4. Run backend:

```bash
go run main.go
```

5. Open `frontend/index.html` in your browser to interact with the app.

---

## 🧩 Next Steps

* Implement meeting upload and Whisper transcription
* Store transcripts in the database
* Create frontend views to select meetings and view summaries
* Integrate GPT API for generating summaries
* Optionally, add PDF generation and email notifications

---

## 📌 Notes

* Initially, audio processing and GPT usage will rely on **OpenAI APIs**.
* Later, you can implement **local Whisper and local LLMs** for offline usage.
