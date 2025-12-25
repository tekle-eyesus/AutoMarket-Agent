# AutoMarket Agent

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C1C1C?style=flat-square)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square)
![Tavily](https://img.shields.io/badge/Tavily-4285F4?style=flat-square)

> **An autonomous AI investment analyst that researches, analyzes financials, and writes reports without human intervention.**

###  Overview
**AutoMarket Agent** is an advanced "Agentic Workflow" built with **LangGraph**. Unlike standard chatbots, this system orchestrates multiple AI workers (Researcher, Analyst, Writer) to perform deep market research. It autonomously scrapes web news, retrieves live stock data, and compiles a professional investment report in Markdown.

### 🚀 Features
*   **Autonomous Research:** Scrapes real-time news and competitor data using the Tavily Search API.
*   **Financial Analysis:** Fetches live stock data (P/E, Market Cap, Price) via `yfinance`.
*   **Multi-Agent Orchestration:** Uses a state graph to pass information between specialized AI nodes.
*   **Blazing Fast:** Powered by **Llama 3 (70b)** running on **Groq** for sub-second inference.

### 🛠️ Tech Stack
*   **Orchestration:** LangGraph (Stateful multi-agent workflows)
*   **LLM:** Llama 3-70b via Groq API
*   **Tools:** Tavily (Search), YFinance (Market Data)
*   **Environment:** Google Colab / Python

### ⚡ Quick Start (Google Colab)
The easiest way to run this project is via Google Colab.

1.  **Clone or Download** this repository.
2.  Open the `AutoMarket_Agent.ipynb` file in Google Colab.
3.  **Set Secrets:** In the Colab sidebar (Key icon), add the following secrets:
    *   `GROQ_API_KEY`
    *   `TAVILY_API_KEY`
4.  **Run All Cells:** The agent will ask for a company name and generate the report.

### 📦 Local Installation
If you prefer running it locally:

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/AutoMarket-Agent.git
cd AutoMarket-Agent

# 2. Install dependencies
pip install langgraph langchain langchain_groq tavily-python yfinance

# 3. Export API Keys
export GROQ_API_KEY="your_groq_key"
export TAVILY_API_KEY="your_tavily_key"

# 4. Run the script
python main.py
```

