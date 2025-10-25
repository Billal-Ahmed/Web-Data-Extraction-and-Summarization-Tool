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
| **Frontend / UI** | Streamlit|
| **Backend Logic** | Python |
| **Libraries** | BeautifulSoup4, Selenium, LXML, HTML5lib |
| **Summarization** | LLaMA / OpenAI OSS model via Groq API |
| **Configuration** | python-dotenv |
| **Deployment** | Docker / Virtual Environment |

---
## Option 1: Using Virtural Env
<code>
### Create a virtual environment
python3 -m venv venv

### Activate it, On Linux/macOS:
source venv/bin/activate
### Activate it, On Windows:
venv\Scripts\activate
pip install -r requirements.txt
GROQ_API_KEY="your_groq_api_key_here"
streamlit run app.py
</code>
## Option 2: Using Docker

