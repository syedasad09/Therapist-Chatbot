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
