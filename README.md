AI Knowledge Base Chatbot (RAG) for Telegram

An AI-powered Telegram chatbot that answers customer questions using information stored in a business knowledge base.

Built with n8n, Google Gemini, Telegram, Google Drive, and Supabase Vector Store, this system uses Retrieval-Augmented Generation (RAG) to retrieve relevant business information and generate accurate responses.

---

Overview

This project demonstrates an AI-powered Knowledge Base / RAG chatbot for businesses.

Business information is first loaded from a document stored in Google Drive. The document is processed, split into smaller sections, converted into vector embeddings using Google Gemini, and stored in a Supabase Vector Store.

When a customer asks a question through Telegram, the AI Agent searches the knowledge base for relevant information and generates a response using Google Gemini.

---

Workflow

Knowledge Base Workflow

Google Drive → Data Loader → Text Splitter → Gemini Embeddings → Supabase Vector Store

Telegram AI Chatbot Workflow

Telegram Trigger → AI Agent → Supabase Vector Store → Google Gemini → Code (JavaScript) → Telegram

---

How It Works

1. 📚 Load Business Knowledge

Business information is stored in a document and downloaded from Google Drive.

2. ⚙️ Process the Document

The document is loaded and split into smaller sections so the information can be efficiently searched.

3. 🔤 Generate Embeddings

Google Gemini Embeddings convert the document information into vector embeddings.

4. 🗄️ Store Knowledge

The embeddings are stored in the Supabase Vector Store, creating the searchable business knowledge base.

5. 💬 Receive Customer Question

The customer sends a question through Telegram.

6. 🔎 Retrieve Relevant Information

The AI Agent searches the Supabase Vector Store to find information related to the customer's question.

7. 🤖 Generate AI Response

Google Gemini uses the retrieved information to generate a relevant response.

8. 💾 Maintain Conversation Context

Simple Memory helps maintain context during the conversation.

9. 📤 Send Response

The processed response is formatted using JavaScript and sent back to the customer through Telegram.

---

Features

- 🤖 AI-powered customer support
- 📚 Business knowledge base
- 🔎 Retrieval-Augmented Generation (RAG)
- 💬 Telegram chatbot integration
- 🧠 Google Gemini AI
- 🔤 Gemini embeddings
- 🗄️ Supabase Vector Store
- 💾 Conversation memory
- 📄 Google Drive document integration
- ⚙️ JavaScript response processing
- ⚡ Automated customer responses
- 🔄 Knowledge-based AI answers

---

Technologies Used

Technology| Purpose
n8n| Workflow automation
Google Gemini| AI chat model and embeddings
Supabase| Vector database / knowledge storage
Telegram| Customer chatbot interface
Google Drive| Business document storage
JavaScript| Response processing and formatting
RAG| Knowledge retrieval

---

Workflow Nodes

Knowledge Base Workflow

- Google Drive – Download File
- Default Data Loader
- Text Splitter
- Google Gemini Embeddings
- Supabase Vector Store – Insert Documents

Telegram AI Chatbot Workflow

- Telegram Trigger
- AI Agent
- Google Gemini Chat Model
- Simple Memory
- Supabase Vector Store – Retrieve Information
- Google Gemini Embeddings
- Code – JavaScript
- Telegram – Send Text Message

---

Use Case

This automation can help businesses provide automated customer support using their own business information.

It can be adapted for:

- 💄 Beauty salons
- 💍 Bridal makeup businesses
- 🏥 Clinics and hospitals
- 🏠 Real estate businesses
- 🍽️ Restaurants
- 🛒 E-commerce businesses
- 🎓 Education and training businesses
- 💼 Service-based businesses
- 📞 Customer support teams

Businesses can add their own service information, prices, FAQs, policies, opening hours, product information, and other documentation to the knowledge base.

---

Example Customer Query

Customer

«What is the price of bridal makeup?»

AI Chatbot

«The bridal makeup service is available at the price listed in our knowledge base. We also provide home service for bridal makeup. The approximate service duration is around 1.5 hours.»

The response is generated using information retrieved from the business knowledge base stored in the Supabase Vector Store.

---

Why RAG?

Traditional AI chatbots may rely primarily on the model's general knowledge.

With RAG, the AI Agent first retrieves relevant information from the business's own knowledge base before generating a response.

This allows businesses to provide information such as:

- Service prices
- Service details
- FAQs
- Business policies
- Opening hours
- Appointment information
- Product information
- Company documentation

The knowledge base can also be updated as business information changes.

---

🎥 Demo Video

The demo shows a customer asking a question through Telegram.

The AI Agent receives the question, searches the Supabase Vector Store for relevant business information, and generates a response using Google Gemini.

AI Knowledge Base Chatbot Demo

"Add your demo video link here"

---

Project Status

Status: ✅ Completed

Project Type: AI Automation / RAG Chatbot

Platform: n8n + Telegram

Database: Supabase Vector Store

AI Model: Google Gemini

---

Repository Structure

AI-Knowledge-Base-Chatbot-RAG/
│
├── workflow/
│   ├── knowledge-base-workflow.json
│   └── telegram-rag-chatbot.json
│
├── demo/
│   ├── demo-video.mp4
│   └── screenshots/
│
└── README.md

---

🔐 Security

No API keys, passwords, bot tokens, or other private credentials are stored in this repository.

Credentials should be configured securely inside n8n.
