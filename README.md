# adk-vertexai-cloudrun-deployment

## Project Structure
adkui/
├── Agent0/          # Base agent
├── Agent1/          # Agent with Google Search tool
│   └── root_agent.yaml
├── deploycloudrun.py
└── .gitignore

## Setup & Run Locally
#Clone the repo
git clone https://github.com/vamshiiyer/adk-agent-codevipassana.git
cd adk-agent-codevipassana

#Create virtual environment
pip install uv
uv venv
source .venv/bin/activate

#Install dependencies
uv pip install google-adk==1.22.1 python-dotenv

#Create .env file
cat <<ENV > .env
GOOGLE_GENAI_USE_VERTEXAI=1
GOOGLE_CLOUD_PROJECT=your-project-id
GOOGLE_CLOUD_LOCATION=us-central1
IMAGEN_MODEL=imagen-3.0-generate-002
GENAI_MODEL=gemini-2.5-flash
ENV

#Run locally
adk web

## Deploy to Cloud Run
python3 deploycloudrun.py

## Credits
Built during Code Vipassana Season 14 
