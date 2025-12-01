FRED Economic Analyst 📈A sophisticated economic analysis tool that integrates Google Gemini AI with the Federal Reserve Economic Data (FRED) API. This application allows users to query complex economic data using natural language, visualizing trends with interactive charts and providing AI-generated context.✨ FeaturesNatural Language Querying: Ask questions like "How has inflation changed over the last decade?" or "Show me the 30-year mortgage rate."AI-Powered Analysis: Uses Google's Gemini model to interpret data trends, explain economic context, and identify key shifts.Interactive Visualizations: Renders dynamic, responsive charts using Chart.js.Data Export: Instantly download any dataset as a CSV file for local analysis.Source Transparency: Direct links to the official FRED data sources for verification.Dark Mode: Fully responsive UI with a toggleable dark/light theme.🛠️ Tech StackBackend: Python, FlaskAI/LLM: Google Gemini 2.0 FlashData Source: St. Louis Fed Web Services (FRED API)Data Processing: PandasFrontend: HTML5, Tailwind CSS, Chart.js🚀 Installation & SetupPrerequisitesPython 3.8 or higherA Google Cloud API Key (for Gemini)A FRED API Key (from St. Louis Fed)1. Clone the Repositorygit clone [https://github.com/yourusername/fred-analyst.git](https://github.com/yourusername/fred-analyst.git)
cd fred-analyst

2. Set Up Virtual Environment (Recommended)# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate

3. Install Dependenciespip install -r requirements.txt

4. Configure Environment VariablesCreate a .env file in the root directory and add your API keys:GEMINI_API_KEY=your_google_api_key_here
FRED_API_KEY=your_fred_api_key_here

5. Run the Applicationpython app.py

Visit http://127.0.0.1:5000 in your browser.📂 Project Structurefred-analyst/
├── app.py               # Main Flask application and AI logic
├── requirements.txt     # Python dependencies
├── .env                 # API Keys (Excluded from Git)
├── .gitignore           # Git ignore rules
└── templates/
    └── index.html       # Frontend user interface

🌍 Deployment (Render)This project is configured for deployment on Render.Push your code to GitHub.Create a new Web Service on Render connected to your repo.Set the Build Command to: pip install -r requirements.txtSet the Start Command to: gunicorn app:appAdd your GEMINI_API_KEY and FRED_API_KEY in the Render Environment Variables settings.Disclaimer: This tool uses AI to interpret economic data. While it aims for accuracy, always verify critical financial information with official sources.