# marcellas-n8n-chatbot
AI-powered chatbot built with n8n to automate customer interactions, answer questions, and support guests for Marcella's Italian Kitchen.

# Marcellas n8n RAG Chatbot

An embedded AI chatbot built to power intelligent conversations on the Marcellas website.
This system uses Retrieval-Augmented Generation (RAG) to provide accurate responses grounded in business documents stored in Google Drive.

The project combines modern LLM tooling, vector databases, and workflow automation to create a scalable, maintainable support assistant.

---

# Overview

The Marcellas Chatbot is designed to answer customer questions using real company knowledge rather than generic AI responses.

Instead of relying solely on a language model, the system retrieves relevant documents from a vector database and injects them into the model’s context before generating a response.

This results in:

• More accurate answers
• Business-specific knowledge
• Reduced hallucinations
• Easy knowledge updates through Google Drive

---

# Architecture

User → Website Chat Widget → n8n Workflow → Pinecone Vector Search → OpenAI Response → User

Core pipeline:

1. User sends a message from the website
2. n8n receives the request via webhook
3. Query embedding is generated
4. Pinecone searches the knowledge base
5. Relevant context is injected into the prompt
6. OpenAI generates the final response
7. Response is returned to the website chat UI

---

# Tech Stack

Frontend
• Embedded HTML chatbot widget

AI / LLM
• OpenAI

Vector Database
• Pinecone

Automation / Orchestration
• n8n

Data Source
• Google Drive

Embeddings
• OpenAI Embeddings API

---

# Key Features

Retrieval-Augmented Generation (RAG)
Responses grounded in real company documents.

Live Knowledge Updates
Updating files in Google Drive refreshes the assistant’s knowledge base.

Website Embedding
Chatbot integrates directly into the Marcellas website.

Automated Workflow
n8n handles orchestration, retrieval, prompting, and response delivery.

Scalable Architecture
Vector search enables fast retrieval even with large knowledge bases.

---

# Project Structure

```
marcellas-n8n-chatbot
│
├── architecture.png        # System architecture diagram
├── workflows/              # n8n workflow exports
├── prompts/                # Prompt templates
├── embeddings/             # Embedding utilities
└── README.md
```

---

# How It Works

Document Ingestion

1. Documents are uploaded to Google Drive
2. Text is extracted and chunked
3. Embeddings are generated
4. Vectors are stored in Pinecone

User Query

1. User sends a question
2. Query embedding is generated
3. Pinecone retrieves relevant context
4. Context is passed to OpenAI
5. AI generates grounded answer

---

# Example Use Cases

• Customer support automation
• Restaurant information assistant
• FAQ automation
• Menu or event inquiries
• Internal knowledge assistant

---

# Deployment

1. Deploy n8n instance
2. Configure environment variables
3. Connect Google Drive
4. Initialize Pinecone index
5. Add OpenAI API key
6. Embed chatbot script into website

---

# Environment Variables

```
OPENAI_API_KEY=
PINECONE_API_KEY=
PINECONE_ENVIRONMENT=
GOOGLE_DRIVE_CREDENTIALS=
N8N_WEBHOOK_URL=
```

---

# Future Improvements

• Conversation memory
• Analytics dashboard
• Admin panel for document management
• Multi-language support
• Streaming responses
• Fine-tuned prompt optimization

---

# Why This Project Matters

This project demonstrates practical AI engineering by combining LLMs, vector search, and workflow automation into a real production-style system.

It showcases skills in:

• AI application architecture
• Retrieval-Augmented Generation
• API orchestration
• vector databases
• automation pipelines

---

# Author

Jason
Data Scientist / AI Builder

