

---

# AI Chat with LangGraph & Streamlit

This project is an **AI-powered conversational application** built using **LangGraph**, **FastAPI**, and **Streamlit**.
It integrates **Groq’s Llama 3.1-8B model** with tool support (web search via Tavily) and provides a chat interface for interactive conversations.

---

## 🚀 Features

* **LangGraph-powered conversation flow** with state management.
* **Groq Llama 3.1-8B model** as the core LLM.
* **Tool integration** using Tavily Search API for real-time web lookups.
* **FastAPI backend** with streaming responses (SSE).
* **Streamlit frontend** with a chat-like UI.
* **Multi-threaded conversation support** (switch between chats).

---

## 📂 Project Structure

```
├── app.py       # FastAPI backend (LLM + tools + streaming endpoint)
├── client.py    # Streamlit frontend (chat interface)
```

---

## ⚙️ Installation

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd <your-repo>
   ```

2. **Create and activate virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scripts\activate      # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   Example dependencies (ensure these are in `requirements.txt`):

   ```
   fastapi
   uvicorn
   streamlit
   sseclient-py
   langchain
   langgraph
   langchain-groq
   langchain-community
   python-dotenv
   ```

---

## ▶️ Running the Application

1. **Start the FastAPI backend**

   ```bash
   uvicorn app:app --reload --host 127.0.0.1 --port 8000
   ```

2. **Run the Streamlit frontend**

   ```bash
   streamlit run client.py
   ```

3. **Access the app**

   * Streamlit UI → [http://localhost:8501](http://localhost:8501)
   * Backend API → [http://127.0.0.1:8000/chat\_stream/{message}](http://127.0.0.1:8000/chat_stream/{message})

---

## 💡 Usage

* Type a message in the chat box.
* The assistant responds using the LLM.
* If a search query is needed, the Tavily tool is triggered, and results are shown with clickable links.
* You can start new chats or switch between saved conversations from the sidebar.

---

## 🛠️ Environment Variables

Create a `.env` file in the root directory with the required API keys (example):

```
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

---

## 🔮 Future Improvements

* Add support for more tools (e.g., database queries, code execution).
* Improve UI/UX with message formatting and memory visualization.
* Deploy backend (FastAPI) and frontend (Streamlit) to cloud platforms.



