# 🌐 Web Data Extraction and Summarization Tool (WDEST)

### 🚀 Overview

**Web Data Extraction and Summarization Tool (WDEST)** is an AI-powered application that extracts meaningful content from web pages and automatically generates concise summaries using a Large Language Model (LLM) hosted on **Groq**.  

It provides a simple, interactive **Streamlit** interface where users can input a URL, extract the page data, and instantly view a summarized version of its content.  

This project aims to simplify research and save time for students, journalists, and professionals who deal with large amounts of online information.

---

## 🧠 Project Motivation

There’s too much unstructured information on the internet. Finding relevant data quickly and understanding it takes time.  
Our tool automates this process — it **scrapes**, **processes**, and **summarizes** web data into an easy-to-digest summary.

---

## 🏗️ System Architecture

The system consists of three main modules:

1. **Web Scraper** – Extracts readable content from the given URL using `Selenium` and `BeautifulSoup`.
2. **Summarizer** – Sends the extracted content to an **OpenAI OSS model hosted on Groq** for summarization.
3. **User Interface (UI)** – Built with `Streamlit` to provide a clean, simple, and interactive experience.

---

## ✨ Features

- 🔍 **Automatic Web Content Extraction**  
  Extracts readable text from a given web page.
  
- 🧩 **Smart AI Summarization**  
  Uses Groq-hosted LLMs (OpenAI OSS models) to summarize content.

- 🖥️ **Interactive Web Interface**  
  Simple and clean interface using Streamlit.

- 🔒 **Secure Configuration**  
  Environment variables managed via `.env` for API keys.

---

## ⚙️ Tech Stack

| Component | Technology Used |
|------------|----------------|
| **Frontend / UI** | Streamlit, HTML, CSS, JS |
| **Backend Logic** | Python |
| **Libraries** | BeautifulSoup4, Selenium, LXML, HTML5lib |
| **Summarization** | LLaMA / OpenAI OSS model via Groq API |
| **Configuration** | python-dotenv |
| **Deployment** | Docker / Virtual Environment |

---
## 🧩 Project Structure
- **app.py** Main Streamlit Application 
- **scraper.py**  Handles web scraping logic 
- **summarizer.py**  Handles summarization using Groq API 
- **requirements.txt**  Python dependencies 
- **.env.example**  Example environment file 
- **Dockerfile**  Docker image setup 
- **docker-compose.yml**  Docker service configuration 
- **README.md**  Project documentation 
- **assets/**  (Optional) UI assets like logos or icons 
---

## 🪄 Installation & Setup

You can set up the project in **two ways**:

---

### 🧱 Option 1: Using Virtual Environment

#### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/web-data-extraction-summarization.git
cd web-data-extraction-summarization






---

✅ **Ready to use:**  
You can now copy-paste this into a `README.md` file — GitHub will render all sections (headers, tables, and code blocks) perfectly.  

Would you like me to add **optional screenshots / example output** placeholders (like `/assets/screenshot1.png`) right before the “Testing” section? That can make it visually appealing for your repo’s landing page.



