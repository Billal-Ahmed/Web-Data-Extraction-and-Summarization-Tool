# 🌐 Web Data Extraction and Summarization Tool

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

2. Create and Activate a Virtual Environment
# Create a virtual environment
python3 -m venv venv

# Activate it
# On Linux/macOS:
source venv/bin/activate

# On Windows:
venv\Scripts\activate

3. Install Dependencies
pip install -r requirements.txt

4. Configure Environment Variables

Create a file named .env in the project root:

GROQ_API_KEY=your_groq_api_key_here

5. Run the Application
streamlit run app.py


Then open your browser at:
👉 http://localhost:8501

🐳 Option 2: Using Docker
1. Build Docker Image
docker build -t wdest-app .

2. Run the Container
docker run -d -p 8501:8501 --env-file .env wdest-app

3. Access the Application

Open your browser at:
👉 http://localhost:8501

📜 Example .env File
# Environment configuration
GROQ_API_KEY=your_groq_api_key_here

requirements.txt
streamlit
selenium
beautifulsoup4
lxml
html5lib
python-dotenv
groq

Dockerfile
# Use an official lightweight Python image
FROM python:3.10-slim

# Set working directory
WORKDIR /app

# Copy files
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose Streamlit port
EXPOSE 8501

# Run Streamlit app
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]

docker-compose.yml
version: "3.8"
services:
  wdest:
    build: .
    container_name: wdest_container
    ports:
      - "8501:8501"
    env_file:
      - .env

🧪 Testing

Unit Testing: Test each module (scraper, summarizer) independently.

Integration Testing: Ensure modules work together.

System Testing: Test using real-world URLs.

User Acceptance Testing (UAT): Verify with different content and user scenarios.

🖥️ Hardware Requirements

Minimum 4 GB RAM

Stable internet connection (≥ 50 kbps)

Modern web browser for UI

👥 Team Members
Name	Reg. No	Role
Muhammad Imran	2022-UOBSAC-194	Team Leader
Zeeshan Abbas	2022-UOBSAC-210	Developer

Supervisor: Mr. Manzoor Hussain
Department: Computer Science, Government Degree College Skardu
Affiliation: University of Baltistan Skardu

📚 References

Groq API Docs

Selenium Documentation

BeautifulSoup Docs

Streamlit Documentation

📄 License

This project is licensed under the MIT License — you’re free to use, modify, and distribute it.

🌟 Acknowledgements

Special thanks to our supervisor Mr. Manzoor Hussain for his guidance,
and to the University of Baltistan Skardu for academic and technical support.



```
