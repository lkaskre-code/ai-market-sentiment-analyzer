# AI Market Sentiment Analyzer

A Python project that evaluates the current market mood for any asset (e.g., Bitcoin, Tesla, Gold) by reading the latest news and scoring it using an LLM. 

## What this script does
1. **Fetches News:** Downloads recent articles about a specific market using the NewsAPI.
2. **AI Analysis:** Uses Groq's Llama-3 model to read the articles and score them based on **Sentiment** (1-10) and **Relevance** (1-10).
3. **Weighted Average:** Calculates a final market score. Highly relevant macroeconomic news impacts the score more than minor rumors or opinion pieces.
4. **Export:** Displays a clean UI dashboard with the final result and logs the data into a local `Sentiments_report.csv` for further tracking.

## How to get the free API Keys
To run this script, you need two free API keys. It takes 2 minutes to create the accounts:
* **NewsAPI Key:** Get it at [newsapi.org](https://newsapi.org/) (Used to fetch the articles).
* **Groq API Key:** Get it at [console.groq.com](https://console.groq.com/) (Used to run the Llama-3 AI model).

You can enter these keys directly into the UI popup when starting the script. Alternatively, create a `.env` file in the project folder to load them automatically:
```text
NEWS_API_KEY=your_news_key_here
GROQ_API_KEY=your_groq_key_here
