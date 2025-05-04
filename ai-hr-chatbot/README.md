# AI-Driven HR Knowledge Base using RAG Architecture

## 🔍 Summary
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

+------------------+       +------------------+       +-------------------------+
|   React Frontend | <---> |    Flask Backend | <---> |   LangChain RAG Engine  |
+------------------+       +------------------+       +-------------------------+
                                                          |            |
                                                          |            |
                                                          v            v
                                               +----------------+  +------------------+
                                               | Azure Cognitive|  | OpenAI GPT Model |
                                               |    Search       |  |  (via API)       |
                                               +----------------+  +------------------+
                                                        ^
                                                        |
                                               +------------------+
                                               | HR Document Store |
                                               | (PDFs, Policies)  |
                                               +------------------+

                         [Auth Layer: Azure AD SSO Enforced on Frontend & Backend]
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
