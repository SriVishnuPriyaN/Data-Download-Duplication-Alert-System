# 🛑 Data Download Duplication Alert System

A browser-based alert system that detects and prevents duplicate file downloads. This ensures efficient data management, storage optimization, and prevents accidental file redundancy.

---

## 📌 Features

- ✅ Tracks all downloaded file names and timestamps  
- 🚫 Prevents duplicate downloads  
- 🔔 Alerts users and requests confirmation for re-downloading  
- 🗂️ Supports various file types: `.pdf`, `.pptx`, `.docx`, `.xlsx`, etc.  
- 💾 Uses SQLite for local file tracking  

---

## ⚙️ Technology Stack

- **Python 3.x**  
- **SQLite**  
- **Browser download event listener (via browser extension or script injection)**  
- **Tkinter (for GUI alert, optional)**  

---

## 🚀 Installation and Setup

### 🔹 1. Clone the Repository

```bash
git clone https://github.com/your-username/data-duplication-alert.git
cd data-duplication-alert

2. Create & Activate a Python Virtual Environment
✅ Windows:
python -m venv venv
venv\Scripts\activate

✅ macOS / Linux:
python3 -m venv venv
source venv/bin/activate

3. Install Dependencies
pip install -r requirements.txt

If requirements.txt is not available, install manually:

pip install sqlite3 watchdog

(Optional: pip install tkinter if GUI alerts are used.)

💡 How It Works
The script monitors file downloads in a specific directory (like Downloads/).
Every downloaded file is logged in a local SQLite database with a hash or name + timestamp.
When a new download starts, the script checks the filename (or hash) against the database.
If a duplicate is detected:

The download is paused or blocked.

The user receives an alert:

Proceed: File is downloaded and logged again.

Cancel: Download is aborted.

🧪 Running the Code
Make sure your virtual environment is activated, then run:

python main.py

You may need to run this script in the background or integrate it with a browser event handler.

📂 File Structure
data-duplication-alert/
│
├── main.py                 # Core monitoring and alert logic
├── database.db             # SQLite file to store download history
├── config.py               # Path configuration and constants
├── utils.py                # Helper functions (hashing, validation)
├── requirements.txt
└── README.md

🛡️ Future Enhancements
Browser extension for Chrome/Firefox

File content hash comparison instead of just file names

Cross-platform support

Notification system integration

👨‍💻 Author
Developed by Vishnu Priya and Team – Student-led innovation project.
