# 🧠 CyberSnark Desktop Agent

A local automation agent designed to post CyberSnark briefings (MP3 + TXT) to platforms like TikTok and YouTube Studio, and commit logs to GitHub — even when those platforms have no usable public API.

---

## 🚀 Purpose

This tool eliminates manual steps in the CyberSnark 2.0 pipeline by:
- Watching a `/pending/` folder for new content
- Automatically posting videos via GUI automation
- Committing markdown logs to GitHub
- Preparing for advanced trigger options (voice, hotkey, schedule)

Built to run on a high-performance local machine with access to full desktop GUI.

---

## 🔧 Features (Phase 1 - MVP)

- ✅ Watches a local `pending/` folder
- ✅ Matches `.mp3` and `.txt` files by name
- ✅ Simulates upload to TikTok or YouTube Studio *(GUI automation to come)*
- ✅ Commits `.txt` as versioned changelog to GitHub
- ✅ Moves files to `posted/` after processing

---

## 📁 Folder Structure

cybersnark-desktop-agent/
│
├── pending/ # Drop .mp3 and .txt files here
├── posted/ # Files are moved here after processing
├── logs/ # Markdown copies of logs for GitHub commits
│
├── watcher.py # Watches /pending/ for new files
├── agent.py # Core agent logic (processes and uploads)
├── utils.py # Helpers: matching, GitHub push, file move
├── .env # API keys and repo info (not tracked)
└── README.md # You're here!

yaml
Copy
Edit

---

## 🔐 Setup

1. **Install Python 3.10+**

2. **Clone this repo** or create it locally:
   ```bash
   git clone https://github.com/yourusername/cybersnark-desktop-agent.git
   cd cybersnark-desktop-agent
Set up Python environment:

bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
Create .env file:

ini
Copy
Edit
OPENAI_API_KEY=sk-...
GITHUB_TOKEN=github_pat_...
GITHUB_REPO=yourusername/cybersnark-desktop-agent
🧪 Usage
Run the agent watcher:

bash
Copy
Edit
python watcher.py
Leave it running in the background. It will:

Detect matching .mp3 + .txt pairs

Simulate uploading

Push the .txt to GitHub

Move both files to posted/

🗺️ Roadmap
🔄 Phase 2 – Logic Layer
Add OpenAI changelog summaries to GitHub commits

Add file-based skip/post conditions

🧠 Phase 3 – Smart Triggering
Hotkey or “Hey CyberSnark” voice activation

Scheduled posting (CRON-style or task-based)

Slack or webhook trigger

🎬 Phase 4 – GUI Posting
TikTok upload via Puppeteer/Selenium

YouTube Studio automation

Instagram Reels automation

🤝 Credits
Built by Christian Wentz
Netrock Custom Cybersecurity — Protecting your business since 2002

📜 License
MIT License# cybersnark-desktop-agent
