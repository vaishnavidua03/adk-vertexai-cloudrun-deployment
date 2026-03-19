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

| Technology | Purpose |
|---|---|
| Google ADK | Agent framework |
| Gemini 2.5 Flash | LLM model |
| Vertex AI | AI platform |
| Imagen 3.0 | Image generation |
| Cloud Run | Production deployment |
| Python | Custom tools |
| YAML | Agent configuration |

## Credits 
Build during Google [Code Vipassana](https://rsvp.withgoogle.com/events/cv) Season 14 
