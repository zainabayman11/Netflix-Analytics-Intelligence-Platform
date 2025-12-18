# 🎬 Netflix Analytics Intelligence Platform

An end-to-end **AI-powered analytics platform** that connects structured data with an LLM, allowing users to ask **natural language questions** and get meaningful insights from Netflix data.

This project is built as a **learning-focused implementation** to understand how to:
- Connect data sources to LLMs
- Build AI agents that reason over data
- Translate natural language into SQL
- Visualize insights in an interactive dashboard

---

## 🚀 Key Features

- 🤖 **AI SQL Agent**
  - Ask questions in plain English
  - Automatically generates and executes SQL queries
- 📊 **Interactive Dashboard**
  - Built with Streamlit
  - Real-time analytics and metrics
- 📈 **Automated Visualizations**
  - Interactive charts using Plotly
- 🧠 **Local LLM (Privacy-first)**
  - Powered by Ollama + Llama 3.1
- 💾 **Netflix Dataset Analysis**
  - 8,800+ Movies & TV Shows
- 🔍 **Explainable Results**
  - Insights + reasoning, not just raw numbers

---

## 🛠️ Tech Stack

- **Python**
- **LangChain & LangGraph** – AI agent orchestration
- **Ollama + Llama 3.1 (8B)** – Local LLM
- **SQLite** – Structured data storage
- **Pandas** – Data processing
- **Plotly** – Interactive visualizations
- **Streamlit** – Web application UI

---

## 📊 Dataset

- **Netflix Movies and TV Shows Dataset**
- ~8,800 titles
- Source: Kaggle  
- Includes:
  - title, type, director, cast
  - country, rating, genres
  - release year & date added

---

## 💡 Example Questions You Can Ask

- “What are the top 5 countries producing Netflix content?”
- “What is the distribution between Movies and TV Shows?”
- “Which directors have directed the most movies?”
- “Show the trend of content added per year.”
- “What are the most common genres on Netflix?”

---

## ⚙️ How It Works (High Level)

1. User asks a question in natural language  
2. LLM reasons about the schema  
3. Generates a **safe SQL SELECT query**  
4. Executes it on the SQLite database  
5. Returns:
   - Results
   - Insights
   - Optional visualizations

---

## ▶️ Running the Project

### Option 1: Google Colab (Recommended)
1. Open the notebook in Colab  
2. Run all cells in order  
3. Start Streamlit + Ngrok  
4. Access the public dashboard link  

### Option 2: Local Setup
```bash
git clone https://github.com/YOUR_USERNAME/netflix-analytics-platform
cd netflix-analytics-platform

pip install -r requirements.txt

# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama3.1:8b

streamlit run app/streamlit_app.py

