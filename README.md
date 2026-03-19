## Live Demo 
https://agent1service-1085233822951.us-central1.run.app

## About

Agent1 Service is a cloud-deployed conversational AI agent built on Google's **Agent Development Kit (ADK)**. It exposes an interactive **Dev UI** for real-time agent testing and a REST API for programmatic access — all running serverlessly on **Google Cloud Run**.

The project demonstrates how to build, wrap, and ship a production-ready AI agent with minimal infrastructure overhead, leveraging Google's managed cloud services for scalability and reliability.

## Features

- 🧠 **Conversational AI Agent** — Powered by Google Gemini via the ADK framework
- 🖥️ **Dev UI** — Browser-based interface at `/dev-ui` for testing and debugging the agent interactively
- ☁️ **Serverless Deployment** — Hosted on Google Cloud Run with automatic scaling and zero idle cost
- 🔌 **REST API** — Clean HTTP endpoints for integrating the agent into any application
- 🔄 **Session Management** — Stateful multi-turn conversations via ADK's built-in session handling
- 📦 **Containerized** — Fully Dockerized for consistent, reproducible builds and deployments

## Tech Stack

| Layer | Technology |
| **AI Model** | Google Gemini (via ADK) |
| **Language** | Python 3.11+ |
| **Serving** | ADK API Server (FastAPI-based) |
| **Containerization** | Docker |
| **Cloud Platform** | Google Cloud Platform (GCP) |
| **Deployment** | Google Cloud Run |
| **Region** | `us-central1`|


 Project Structure
adkui/
├── Agent0/          # Base agent
├── Agent1/          # Agent with Google Search tool
│   └── root_agent.yaml
├── deploycloudrun.py
└── .gitignore

⚙️ Setup & Run Locally

# Clone the repo
git clone https://github.com/vamshiiyer/adk-agent-codevipassana.git
cd adk-agent-codevipassana

# Create virtual environment
pip install uv
uv venv
source .venv/bin/activate

# Install dependencies
uv pip install google-adk==1.22.1 python-dotenv

# Create .env file
cat <<ENV > .env
GOOGLE_GENAI_USE_VERTEXAI=1
GOOGLE_CLOUD_PROJECT=your-project-id
GOOGLE_CLOUD_LOCATION=us-central1
IMAGEN_MODEL=imagen-3.0-generate-002
GENAI_MODEL=gemini-2.5-flash
ENV

# Run locally
adk web
☁️ Deploy to Cloud Run
python3 deploycloudrun.py



## Credits 
Build during Google [Code Vipassana](https://rsvp.withgoogle.com/events/cv) Season 14 
