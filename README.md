<div align="center">

# 🩺 DoctorConnectAI

**A RAG chatbot that recommends doctors in Pakistan by city, condition, budget and gender preference.**

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain"> <img src="https://img.shields.io/badge/Groq%20%C2%B7%20Llama%203-F55036?style=for-the-badge" alt="Groq · Llama 3"> <img src="https://img.shields.io/badge/Chroma-FF6446?style=for-the-badge" alt="Chroma"> <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=white" alt="Hugging Face"> <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">

</div>

## 📌 Overview

Patients describe where they are, what they need treatment for, their budget and whether they prefer a male or female doctor. DoctorConnectAI retrieves matching doctor profiles from a vector database and uses an LLM to recommend the best options in a conversational way.

## ✨ Features

- **Conversational search:** history-aware retrieval, so follow-up questions keep their context
- **Doctor knowledge base:** profiles from `data.json`, embedded with `all-MiniLM-L6-v2` into a local Chroma DB
- **LLM:** Llama 3 70B served by Groq for fast responses
- **Filters by:** city or region, disease or concern, fee range, doctor gender
- **UI:** Streamlit chat interface

## 🚀 Getting Started

```bash
git clone https://github.com/KamranUmer/DoctorConnectAI.git
cd DoctorConnectAI
pip install -r requirements.txt
cp .env.example .env      # add your GROQ_API key
python ingest.py          # builds the Chroma DB from data.json
streamlit run main.py
```

## 📁 Project Structure

```
DoctorConnectAI/
├── main.py           # Streamlit chat app + retrieval chain
├── ingest.py         # embeds data.json into Chroma
├── data.json         # doctor profiles
├── prompt            # system prompt
├── RAG.ipynb         # prototype notebook
└── requirements.txt  # dependencies
```

---

<div align="center">

Built by <a href="https://github.com/KamranUmer"><b>Kamran Umer</b></a> · ⭐ Star the repo if you find it useful

</div>
