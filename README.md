# FRED Economic Analyst 📈

A sophisticated economic intelligence tool that integrates **Google Gemini AI** with the **Federal Reserve Economic Data (FRED)** API. This application allows users to query complex economic data using natural language, visualizing trends with interactive charts and providing AI-generated context.

![Project Status](https://img.shields.io/badge/status-active-success)
![Python Version](https://img.shields.io/badge/python-3.9%2B-blue)

## ✨ Features

-   **Natural Language Querying:** Ask questions like "How has inflation changed over the last decade?" or "Show me the 30-year mortgage rate."
-   **AI-Powered Analysis:** Uses Google's Gemini 2.0 Flash model to interpret data trends, explain economic context, and explain *why* trends are happening.
-   **Interactive Visualizations:** Renders dynamic, responsive charts using Chart.js.
-   **Data Export:** Instantly download any dataset as a CSV file for local analysis.
-   **Source Transparency:** Direct links to the official FRED data sources for verification.
-   **Safety Guardrails:** Includes strict prompt injection handling to ensure the AI remains focused on economic data.
-   **Dark Mode:** Fully responsive UI with a toggleable dark/light theme.

## 🛠️ Tech Stack

* **Backend:** Python, Flask
* **AI/LLM:** Google Gemini 2.0 Flash
* **Data Source:** St. Louis Fed Web Services (FRED API)
* **Data Processing:** Pandas
* **Frontend:** HTML5, Tailwind CSS, Chart.js

## 🚀 Installation & Setup

### Prerequisites
* Python 3.8 or higher
* A Google Cloud API Key (for Gemini)
* A FRED API Key (from St. Louis Fed)

### 1. Clone the Repository
```bash
git clone [https://github.com/yourusername/fred-analyst.git](https://github.com/yourusername/fred-analyst.git)
cd fred-analyst
````

### 2\. Set Up Virtual Environment (Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3\. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4\. Configure Environment Variables

Create a `.env` file in the root directory and add your API keys:

```env
GEMINI_API_KEY=your_google_api_key_here
FRED_API_KEY=your_fred_api_key_here
```

### 5\. Run the Application

```bash
python app.py
```

Visit `http://127.0.0.1:5000` in your browser.

## 📂 Project Structure

```text
fred-analyst/
├── app.py               # Main Flask application and AI logic
├── requirements.txt     # Python dependencies
├── .env                 # API Keys (Excluded from Git via .gitignore)
├── .gitignore           # Git ignore rules
└── templates/
    └── index.html       # Frontend user interface
```

## 🌍 Deployment (Render)

This project is configured for seamless deployment on [Render](https://render.com).

1.  Push your code to GitHub.
2.  Create a new **Web Service** on Render connected to your repo.
3.  Set the **Build Command** to: `pip install -r requirements.txt`
4.  Set the **Start Command** to: `gunicorn app:app`
5.  **Crucial:** Add your `GEMINI_API_KEY` and `FRED_API_KEY` in the Render **Environment Variables** settings.

-----

*Disclaimer: This tool uses AI to interpret economic data. While it aims for accuracy, always verify critical financial information with official sources.*

```
```
