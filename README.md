
# 📊 SWOT Analysis MCP Tool

A Python-based tool for performing SWOT (Strengths, Weaknesses, Opportunities, and Threats) analysis using a Flask API, integrated with [FastMCP](https://www.npmjs.com/package/@modelcontextprotocol/inspector) to enable tool execution via MCP-compatible environments.

![SWOT Banner](images/swot_banner.png)

---

## 🔍 Overview

This project allows users to perform a structured SWOT analysis on a given product or entity via a RESTful API. The backend is powered by Flask, while `main.py` uses FastMCP to expose the tool to LLM agents. This can be especially useful for automated reasoning and market analysis workflows.

---

## 🚀 Features

- 🧠 AI-assisted SWOT analysis from user input
- 🌐 Flask-based API with `/analyze` endpoint
- 🔧 FastMCP integration for tool invocation in agent environments
- 🧪 Automatic testing and endpoint validation using Python subprocess
- 📤 Modular file structure for scalability and debugging

---

## 📂 Project Structure

```
.
├── app.py              # Flask application exposing the /analyze endpoint
├── mcp_swot.py         # Script to launch Flask app and test the endpoint
├── main.py             # FastMCP integration file to run the swot_analysis tool
├── images/             # Folder for screenshots and architecture images
└── README.md
```
# 🛒 E-commerce Product SWOT Analysis API

This project provides an automated **SWOT (Strengths, Weaknesses, Opportunities, Threats) analysis** tool for e-commerce products using **Natural Language Processing (NLP)**.

It combines:
- 🔎 **Google Custom Search API** to fetch reviews from Amazon and Flipkart.
- 🧠 **Hugging Face Transformers** to analyze sentiment.
- ⚙️ **Flask REST API** to provide an `/analyze` endpoint.
- 📄 **FPDF** to generate downloadable SWOT PDF reports.

Useful for **market researchers**, **e-commerce analysts**, and **product managers** to understand consumer sentiment and gain insights into products.

---

## 🚀 Features

- 🔍 Scrapes product reviews from e-commerce sites.
- 💬 Analyzes sentiment using DistilBERT.
- 📊 Visualizes sentiment distribution with charts.
- ✅ Categorizes reviews into SWOT components.
- 📄 Generates downloadable PDF reports.
- 🔗 REST API integration.

---

## 🧰 Tech Stack

- Python 3
- Flask
- Hugging Face Transformers
- Google Custom Search API
- Matplotlib & Pandas
- FPDF

---

## 📁 Project Structure

```
.
├── app.py             # Flask app exposing the /analyze endpoint
├── swot.py            # CLI tool or script to call the /analyze API
├── analysis_results/  # JSON files storing analysis data
├── pdf_reports/       # SWOT analysis PDF reports
├── test_swot.py       # Test script to validate API response
├── requirements.txt   # Dependencies
└── README.md          # Documentation
```

---

## 📦 Installation & Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/ecommerce-swot-analyzer.git
cd ecommerce-swot-analyzer

# (Optional) Create and activate virtual environment
python -m venv .env
source .env/bin/activate  # On Windows: .env\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🔐 Configuration

Replace placeholders in `app.py` with your actual credentials:
```python
GOOGLE_API_KEY = "your_google_api_key"
SEARCH_ENGINE_ID = "your_search_engine_id"
```

---

## 📸 Screenshots

### 1. Swagger Endpoint Test  
![MCP Test](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/mcp1.png)
![MCP Test2](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/mcp2.png)
![MCP Test3](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/mcp3.png)

### 2. Console Output  
![output](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/result1.png)
![output2](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/result2.png)

### 3. Claude Output
![claude1](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/claude-result1.png)
![claude2](https://github.com/Tanujkumar24/SWOT-ANALYSIS/blob/main/swot_server/screenshots/claude-result2.png)

---

## 🧰 Installation & Usage

### Step 1: Clone the Repo
```bash
git clone https://github.com/your-username/swot-analysis-mcp.git
cd swot-analysis-mcp
```

### Step 2: Setup Virtual Environment
```bash
conda create -n swot_env python=3.9
conda activate swot_env
pip install -r requirements.txt
```

### Step 3: Run the Tool with FastMCP
```bash
npx @modelcontextprotocol/inspector python main.py
```

---

## 📬 API Endpoint

- **POST** `/analyze`  
    ```json
    {
      "product_name": "redmi note10"
    }
    ```

    **Response**
    ```json
    {
      "strengths": [...],
      "weaknesses": [...],
      "opportunities": [...],
      "threats": [...]
    }
    ```

---

## ⚙️ Error Handling

If you encounter this error:
```
'charmap' codec can't encode character '\u20b9'
```
Add this to the top of your Python file:
```python
import sys
sys.stdout.reconfigure(encoding='utf-8')
```

---

## ✍️ Author

Tanujkumar Mangalapally  
*Data Scientist | MLOps Engineer | AI Enthusiast*

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
