# Multi-Agent AI Research Assistant

An AI-powered research assistant built using **Python, LangChain, Groq, Tavily and Streamlit**. The application uses multiple AI agents to search the web, extract relevant information, generate detailed research reports and evaluate the generated reports.

## Features

- **Web Search Agent:** Searches the web for recent and relevant information using Tavily.
- **Reader Agent:** Scrapes web pages and extracts useful information from selected URLs.
- **Writer Chain:** Generates structured and detailed research reports using Groq LLM.
- **Critic Chain:** Evaluates the generated report and provides a score, strengths and areas for improvement.
- **Streamlit Interface:** Provides an interactive interface to enter research topics and view generated reports.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | Agent creation and LLM orchestration |
| Groq | Large Language Model inference |
| GPT-OSS-120B | Language model used through Groq |
| Tavily | Web search API |
| BeautifulSoup | Web scraping and HTML parsing |
| Requests | Sending HTTP requests |
| Streamlit | Web application interface |
| Python-dotenv | Environment variable management |

## Project Architecture

The application follows a four-step research workflow:

1. **Search Agent**
   - Accepts a research topic.
   - Searches the web using Tavily.
   - Collects relevant titles, URLs and snippets.

2. **Reader Agent**
   - Selects relevant web resources.
   - Scrapes web pages using the scraping tool.
   - Extracts useful research information.

3. **Writer Chain**
   - Processes the collected research.
   - Generates a structured report containing an introduction, key findings, conclusion and sources.

4. **Critic Chain**
   - Reviews the generated report.
   - Provides a score out of 10.
   - Identifies strengths and areas for improvement.

## Project Structure

```text
MultiAgent_Research_Assistant/
│
├── agents.py
├── app.py
├── pipeline.py
├── tools.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Phoenix3164/MultiAgent_Research_Assistant.git
```

### 2. Navigate to the project directory

```bash
cd MultiAgent_Research_Assistant
```

### 3. Create a virtual environment

```bash
python -m venv .venv
```

### 4. Activate the virtual environment

**Windows:**

```bash
.venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure API keys

Create a `.env` file in the root directory and add your API keys:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Get your API keys from:

- Groq: https://console.groq.com/keys
- Tavily: https://app.tavily.com/

### 7. Run the application

```bash
streamlit run app.py
```

The application will open in your browser, usually at:

```text
http://localhost:8501
```

## How It Works

```text
       User Research Topic
               |
               v
         Search Agent
               |
               v
         Tavily Web Search
               |
               v
          Reader Agent
               |
               v
          Web Scraping
               |
               v
          Writer Chain
               |
               v
        Research Report
               |
               v
          Critic Chain
               |
               v
       Evaluation & Feedback
```

## Future Improvements

- Support multiple research sources and more robust URL extraction.
- Improve scraping reliability for websites that block automated requests.
- Add PDF and document export functionality.
- Introduce report history and research topic management.
- Improve source verification and factual accuracy.

## Author

**Yash Kunjir**

GitHub: [Phoenix3164](https://github.com/Phoenix3164)

---

If you find this project useful, consider giving the repository a ⭐ on GitHub!
