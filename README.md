# 🧠 AI Therapist Chatbot (Flask, ML & RAG Architecture)

> An AI and Machine Learning powered virtual therapist application that uses Retrieval-Augmented Generation (RAG) and predictive ML models to analyze user profiles and provide context-aware mental health support.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation & Setup](#installation--setup)
- [Usage Guide](#-usage-guide)
- [API Endpoints](#-api-endpoints)
- [Future Roadmap](#-future-roadmap)
- [Disclaimer](#-disclaimer)
- [Contributing](#-contributing)
- [License & Contact](#-license--contact)

---

## 📖 Overview

**Therapist Chatbot** is a web-based mental health support assistant built with **Python**, **Flask**, **Machine Learning**, and **RAG (Retrieval-Augmented Generation)**. By combining user demographics (**Name, Age, Gender**) and textual feelings/descriptions with a specialized mental health knowledge base, the system screens for conditions like anxiety and depression while returning grounded, empathetic, and therapeutically relevant responses.

---

## ✨ Key Features

* 👤 **Demographic & Profile Context:** Evaluates queries using user parameters (Name, Age, Gender) for personalized interactions.
* 📚 **Retrieval-Augmented Generation (RAG):** Fetches verified therapeutic knowledge and coping mechanisms from a clinical document index to prevent hallucinations.
* 🤖 **AI & ML Classification Engine:** Analyzes input text to identify emotional indicators such as Anxiety, Depression, Stress, and Burnout.
* 🔌 **Flask REST API Architecture:** Modular RESTful API backend handling data pre-processing, vector search, and model inference.
* 💻 **Interactive HTML/CSS Frontend:** Simple, clean, and empathetic web user interface for real-time conversation.

---

## 🏗️ System Architecture

```text
 [ User Profile Input: Name, Age, Gender, Description ]
                           │
                           ▼
                 [ HTML / JS Frontend ]
                           │
                           ├── JSON REST Request
                           ▼
                  [ Flask Backend API ]
                           │
        ┌──────────────────┴──────────────────┐
        ▼                                     ▼
 [ ML Classifier ]                 [ RAG Retrieval Engine ]
 (Predicts: Anxiety,               (Vector DB / Document Index
  Depression, Normal, etc.)         Retrieves Therapeutic Advice)
        │                                     │
        └──────────────────┬──────────────────┘
                           ▼
               [ Contextual Response Generator ]
                           │
                           ▼
              [ User Output & Chat Interface ]
🛠️ Tech StackCategoryTechnologyFrontendHTML5, CSS3, JavaScriptBackend FrameworkFlask (Python REST API)AI / RAG PipelineLangChain / LlamaIndex / Vector Store (FAISS / Chromadb)Machine Learning & NLPScikit-Learn, NLTK / Pandas / NumPyModel PersistenceJoblib / Pickle🚀 Getting StartedFollow these instructions to set up and run the AI Therapist Chatbot locally.PrerequisitesPython 3.8 or higher installed on your system.Installation & SetupClone the RepositoryBashgit clone [https://github.com/syedasad09/Therapist-Chatbot.git](https://github.com/syedasad09/Therapist-Chatbot.git)
cd Therapist-Chatbot
Create and Activate Virtual EnvironmentBashpython -m venv venv
source venv/bin/activate        # On Linux/Mac
# venv\Scripts\activate          # On Windows
Install DependenciesBashpip install -r requirements.txt
Run the Flask ApplicationBashpython app.py
Access in BrowserOpen your browser and navigate to:HTTP[http://127.0.0.1:5000/](http://127.0.0.1:5000/)
💡 Usage GuideUser Profile: Fill in your basic details (Name, Age, and Gender).Describe Feelings: Type out how you are feeling or describe your thoughts/mood in the input text box.Analyze / Chat: Submit the query. The ML engine classifies the emotional state while the RAG module retrieves relevant therapeutic guidance to form the final answer.📡 API EndpointsMethodEndpointDescriptionPayload ExampleGET/Serves the HTML web interfaceN/APOST/api/predictAccepts user details, retrieves RAG context, and returns ML classification & guidance{"name": "John", "age": 22, "gender": "Male", "description": "I feel constantly overwhelmed..."}⚠️ DisclaimerThis application is an educational AI project and is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of a qualified mental health provider with any questions regarding a medical condition.🗺️ Future Roadmap[ ] Integration with advanced LLMs (e.g., Llama 3 / GPT-4) as the RAG generation backend.[ ] Emergency support hotlines & immediate crisis intervention triggers.[ ] User sentiment tracking & history visualization over time.[ ] Multi-language support.🤝 ContributingContributions are welcome! If you'd like to improve model accuracy, update the RAG knowledge base, or enhance the UI design:Fork the ProjectCreate your Feature Branch (git checkout -b feature/NewTherapyFeature)Commit your Changes (git commit -m 'Add new feature')Push to the Branch (git push origin feature/NewTherapyFeature)Open a Pull Request✉️ License & ContactDistributed under the MIT License. See LICENSE for more information.GitHub: @syedasad09Project Link: https://github.com/syedasad09/Therapist-Chatbot
