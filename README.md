
AI Chatbot using LangGraph, ChatCerebras & Streamlit
This project is a streaming AI chatbot built using LangGraph, LangChain, Cerebras (Qwen model), and Streamlit.

It demonstrates:

Agentic AI workflow using LangGraph

Stateful chat with memory

Streaming responses in Streamlit UI

Secure API key handling using Streamlit Secrets

Features

🔁 LangGraph-based workflow

🧠 Chat memory using checkpointer

⚡ Fast inference via Cerebras (Qwen model)

💬 Streaming chat UI with Streamlit


🏗️ Project Structure
ai-chatbot/
│
├── frontend.py          # Streamlit UI
├── backend.py           # LangGraph + ChatCerebras logic
├── requirements.txt     # Python dependencies
├── .gitignore           # Ignore secrets & venv
├── .env.example         # Example environment variables
└── README.md            # Project documentation

🧩 Tech Stack

Python 3.11

Streamlit – frontend UI

LangChain – LLM interface

LangGraph – agent workflow & memory

ChatCerebras – LLM (Qwen)

Cerebras Cloud SDK

🔑 Environment Variables
Required
Variable	Description
CEREBRAS_API_KEY	Your Cerebras Cloud API key
🔐 API Key Setup (IMPORTANT)
🔹 Local Development

Create a .env file:

CEREBRAS_API_KEY=your_api_key_here

🔹 Streamlit Cloud Deployment

Go to Streamlit App → Settings → Secrets

Add:

CEREBRAS_API_KEY = "your_api_key_here"

📦 Installation (Local)
1️⃣ Create virtual environment
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

2️⃣ Install dependencies
pip install -r requirements.txt

▶️ Run the App Locally
streamlit run frontend.py


App will start at:

http://localhost:8501

🧠 How It Works
🔹 Backend (backend.py)

Uses LangGraph StateGraph

Maintains message history

Calls ChatCerebras (Qwen model)

Stores memory using InMemorySaver

🔹 Frontend (frontend.py)

Streamlit chat interface

Stores messages in st.session_state

Streams assistant responses in real time

🔄 LangGraph Workflow
START → chat_node → END


chat_node receives messages

Sends them to Cerebras LLM

Returns updated state with AI response

📄 requirements.txt (Recommended)
streamlit>=1.52.0
langchain>=1.2.0,<2.0.0
langchain-community>=0.4.0
langgraph>=1.0.0
cerebras-cloud-sdk>=1.59.0
python-dotenv>=1.0.0

👨‍💻 Author

Built by Pratik Naik
B.Tech AI/ML | LangGraph | Agentic AI
