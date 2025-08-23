AI Chat Application with LangGraph and FastAPI
Overview
This project is a sophisticated AI chat application that combines LangGraph for state management, Groq's Llama model for AI responses, and Tavily search for real-time information retrieval. The application features a FastAPI backend with streaming capabilities and a Streamlit frontend for an interactive chat experience.

Key Features
Real-time Streaming: Server-Sent Events (SSE) for live chat responses

Conversation Memory: Persistent chat history using in-memory checkpoints

Web Search Integration: Tavily search tool for retrieving current information

Modular Architecture: Clean separation between backend API and frontend client

State Management: LangGraph for managing complex conversation flows

Technical Stack
Backend (FastAPI)
FastAPI with streaming responses

LangGraph for state management and workflow

Groq Llama 3.1 8B Instant model

Tavily search API integration

In-memory conversation checkpoints

Frontend (Streamlit)
Interactive chat interface

Conversation history sidebar

Real-time message display

SSE client for streaming responses

Installation & Setup
Clone the repository

bash
git clone <repository-url>
cd <project-directory>
Install dependencies

bash
pip install -r requirements.txt
Set up environment variables
Create a .env file with your API keys:

text
GROQ_API_KEY=your_groq_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here
Run the backend server

bash
uvicorn app:app --reload --port 8000
Run the frontend client

bash
streamlit run client.py
Usage
Open the Streamlit application in your browser (typically http://localhost:8501)

Start a new conversation or load an existing one from the sidebar

Type your message in the chat input

Watch as the AI responds in real-time, with optional web search integration

API Endpoints
GET /chat_stream/{message}: Main streaming endpoint for chat interactions

Parameters: message (required), checkpoint_id (optional for continuing conversations)
