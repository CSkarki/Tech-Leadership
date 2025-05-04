# AI-Driven HR Knowledge Base using RAG Architecture

## Summary
This project demonstrates an enterprise-grade implementation of a **Retrieval-Augmented Generation (RAG)** powered chatbot designed to serve as a smart knowledge base for HR-related queries. It combines **Generative AI (OpenAI GPT)** with structured document retrieval using **LangChain** and **Azure Cognitive Search**. The solution significantly reduced HR workload and improved information accessibility for employees at scale.

---

## 🚨 Problem → 💡 Solution → 📈 Impact

### Problem
Employees frequently submitted repetitive HR-related queries, overwhelming support staff and leading to delays, low satisfaction, and inefficient knowledge discovery across systems. There was no intelligent, centralized access point for policy documents, procedures, or HR support content.

### Solution
- Led the design and development of an AI-based expert assistant using a **RAG (Retrieval-Augmented Generation)** approach.
- Built a secure microservice-based architecture using **Flask** and **ReactJS** as the frontend.
- Deployed on **Azure Cloud**, leveraging **Azure Cognitive Search** to index internal HR documents (PDFs, policy docs).
- Integrated **LangChain** for intelligent document chunking, embedding, and similarity search before invoking GPT-based natural language generation.

### Impact
- 📉 Reduced HR ticket volume by 60% within the first 90 days.
- ⚡ Average query response time under 3 seconds.
- 🔐 Ensured enterprise-grade security through Azure AD SSO and access controls.
- 📚 Created a reusable RAG-based framework for other internal use cases (Finance, IT, etc.).

---

## 🛠️ Technology Stack

| Component             | Technology                      |
|-----------------------|----------------------------------|
| Frontend              | ReactJS                         |
| Backend API           | Flask (Python)                  |
| AI Model              | OpenAI GPT                      |
| Retrieval Pipeline    | LangChain + Azure Cognitive Search |
| Embeddings            | OpenAI Embeddings               |
| Authentication        | Azure AD SSO                    |
| Hosting               | Microsoft Azure (App Service, Functions) |

---

## 📐 Architecture Diagram

graph TD
    subgraph Frontend
        F1[React UI (Material-UI)]
        F2[Redux State Management]
        F3[Azure AD Authentication (MSAL)]
        F4[Role-Based Sidebar Navigation]
        F5[Document Upload & Query Components]
        F6[REST API Integration via Axios]
    end

    subgraph Backend
        B1[Flask API Server]
        B2[Authentication Layer]
        B3[Document Processing Engine]
        B4[AI Processing Engine]
        B5[File Storage Handlers]
        B6[SQLite Metadata DB]
        B7[Vector Database (ChromaDB)]
    end

    subgraph Storage & External Services
        S1[Azure Blob Storage]
        S2[OpenAI API]
        S3[Microsoft Graph API]
    end

    F1 --> F2
    F1 --> F3
    F1 --> F4
    F1 --> F5
    F5 --> F6
    F6 --> B1
    F3 --> S3

    B1 --> B2
    B1 --> B3
    B1 --> B4
    B1 --> B5

    B3 --> S1
    B3 --> B6
    B3 --> B7

    B4 --> S2
    B5 --> S1
    B2 --> S3
---

## 📎 Highlights

- Modular codebase with reusable RAG pipeline
- Designed for enterprise-grade governance and privacy controls
- Documentation-first approach for stakeholder clarity
- Future-proofed for multi-domain knowledge base support

---

## 👤 Role & Leadership

Led the end-to-end technical architecture and implementation as **Director of Technology Programs**, collaborating with HR, InfoSec, and DevOps. Drove stakeholder alignment, architecture approval, and Agile execution with cross-functional teams.

---

## ✅ Status

🟢 Completed and operational in production with plans for future expansion into other departments (Finance, Operations).
