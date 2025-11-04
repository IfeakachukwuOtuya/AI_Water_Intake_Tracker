💧 AI Water Tracker

AI-powered hydration tracker with FastAPI backend, Streamlit dashboard, and a smart water-intake agent.
Log daily intake, visualize progress, and get AI-based hydration advice.

✨ Features

Log & store water intake per user

AI hydration feedback

Streamlit dashboard & charts

FastAPI REST endpoints

SQLite storage

Simple logging system

📂 Project Structure
.
├── app.py               # Streamlit UI
├── api.py               # FastAPI backend
├── .env                 # Environment variables
├── scr/
│   ├── agent.py         # AI hydration agent
│   ├── database.py      # DB functions
│   ├── logger.py        # Activity logs
│   └── __init__.py
├── requirements.txt
└── README.md

⚙️ Environment Variables (.env)

Create a .env file in project root:

DB_PATH=water_tracker.db
LOG_FILE=tracker.log


Adjust paths if needed.

🚀 Setup
1️⃣ Install dependencies
pip install -r requirements.txt

2️⃣ Run API server
uvicorn api:app --reload


API Docs → http://127.0.0.1:8000/docs

🧠 API Endpoints
Method	Endpoint	Description
POST	/log-intake	Log water intake
GET	/history/{user_id}	Get intake history
Example Request
POST /log-intake
{
  "user_id": "user_123",
  "intake_ml": 500
}

✅ Roadmap

User auth

Daily goal system

Notifications / reminders

Docker support

🤝 Contributing

PRs welcome — feel free to improve and build on this!

📄 License

MIT License.

Drink smarter 💧🤖
If you like this project, ⭐ star the repo!

3️⃣ Run Streamlit dashboard
streamlit run app.py
