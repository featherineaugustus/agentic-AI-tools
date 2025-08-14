# Agentic AI + FAISS RAG & Spotify API Examples

This repository contains **two Jupyter notebooks** demonstrating:
1. An **Agentic AI** workflow using FAISS-based Retrieval-Augmented Generation (RAG) with Google Gemini as the LLM, capable of using tools for:
   - Math calculations
   - Web searches
   - Local RAG lookups
2. A **Spotify API** example to retrieve the **top tracks** of a specific artist.

---

## 📂 Notebooks

### 1. `main_rag.ipynb`
**Goal:**  
Implement an **Agentic AI system** that:
- Uses **FAISS** to store and retrieve document embeddings.
- Integrates with **Google Gemini API** for reasoning and tool orchestration.
- Supports **dynamic tool use**:
  - **Math tool** – solve mathematical expressions.
  - **Web search tool** – retrieve real-time online information.
  - **RAG tool** – fetch and summarize context from FAISS index.

**Workflow:**
1. **Setup** FAISS index and load sample documents.
2. **Embed** documents using an embedding model.
3. **Define tools** for math, web search, and RAG.
4. **Build the agent** using Gemini’s API to dynamically decide which tool to call.
5. **Run queries** and observe:
   - Direct math answers
   - Web search retrieval
   - Context-aware answers from FAISS

---

### 2. `main_spotify.ipynb`
**Goal:**  
Use the **Spotify Web API** to retrieve the **top tracks** for a given artist.

**Workflow:**
1. **Authenticate** with Spotify API (Client ID & Secret).
2. **Search for artist** by name to get `artist_id`.
3. **Fetch top tracks** using `GET /v1/artists/{id}/top-tracks`.
4. **Display results**:
   - Song title

---

## 🛠️ Requirements

Install dependencies:

```bash
pip install faiss-cpu google-generativeai requests pandas spotipy
```

## Environment
Create .env file and put the following in the file:

# Gemini API
GEMINI_API_KEY=your_gemini_api_key

# Spotify API
CLIENT_ID=your_spotify_client_id
CLIENT_SECRET=your_spotify_client_secret
