# Local RAG Chatbot Suite with Ollama & Streamlit

An enterprise-grade, fully local Retrieval-Augmented Generation (RAG) chatbot system that processes documents (PDFs), performs semantic text chunking, generates high-fidelity embeddings, and handles conversational QA[cite: 5, 6]. The entire system runs locally on your machine for 100% data privacy—no external API keys or cloud services required.

---

## 📂 Architecture & Directory Structure

The repository contains the following core files and experimental toolkits:

1. **`chatbot_app.py`**: The production-ready **Streamlit web application**. It provides a sleek UI for uploading files (`.pdf`), visualizes processing logs (like the number of text chunks generated), and maintains interactive, stateful chat conversations using locally-hosted large language models.
2. **`RAG-Chatbot.ipynb`**: An interactive **Jupyter Notebook** used for step-by-step experimentation, testing text extraction, tuning semantic chunk sizes, downloading local models, and validating the retrieval pipeline before production deployment[cite: 5, 6].

---

## 🛠️ Tech Stack & Model Backends

This suite utilizes high-performance open-source models executed completely on your device via **Ollama**[cite: 5, 6]:
* **LLM Engine:** `vicuna:7b-v1.5-q5_1` (A parameter-optimized, high-fidelity conversational model optimized for precise instruction-following and context-driven synthesis).
* **Embedding Model:** `bge-m3` (A state-of-the-art multi-lingual, multi-functional embedding model by BAAI optimized for dense semantic retrieval).
* **Frontend UI Framework:** `Streamlit` (Provides modern reactive widgets, session state chat memory, and efficient file upload processing).
* **Environment Management:** `Conda` (Ensures isolated, reproducible Python dependency tracking).

---

## 🚀 Step-by-Step Installation & Local Setup

Follow these precise steps to configure your local environment, install prerequisites, resolve system dependencies, and run the system on Windows/Linux/macOS.

### 1. Pre-requisite: Install and Launch Ollama
1. Download Ollama for your operating system from [ollama.com](https://ollama.com).
2. Run the installer application and follow the defaults.
3. Open your system applications menu, launch **Ollama**, and verify its service icon is running active in your taskbar/system tray.

### 2. Configure Your Conda Environment
Open a terminal (or **PowerShell** / **Anaconda Prompt** on Windows) and execute the following:

```powershell
# Create an isolated Conda environment named 'AI' using Python 3.10
conda create --name AI python=3.10 -y

# Activate your newly created environment
conda activate AI
