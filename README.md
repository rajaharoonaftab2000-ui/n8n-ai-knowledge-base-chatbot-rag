AI Knowledge Base Chatbot (RAG) for Telegram

An AI-powered Telegram chatbot that answers customer questions using information stored in a business knowledge base.

Built with n8n, Google Gemini, Telegram and Supabase Vector Store, this system uses Retrieval-Augmented Generation (RAG) to provide accurate answers based on previously stored business documents.

---

📌 Project Overview

This project demonstrates a complete AI Knowledge Base / RAG chatbot for businesses.

Business information is first loaded from a document stored in Google Drive. The document is processed, split into smaller pieces, converted into embeddings using Google Gemini, and stored in a Supabase Vector Store.

When a customer asks a question on Telegram, the AI Agent searches the stored knowledge and generates a relevant answer using Google Gemini.

---

⚙️ How It Works

The automation consists of two main workflows.

1️⃣ Knowledge Base / Data Ingestion Workflow

The first workflow prepares the business knowledge for the AI chatbot.

1. A business document is downloaded from Google Drive.
2. The Default Data Loader processes the document.
3. The document is split into smaller sections.
4. Google Gemini Embeddings convert the information into vector embeddings.
5. The embeddings are stored in the Supabase Vector Store.
6. The knowledge base is now ready for customer queries.

2️⃣ Telegram AI RAG Chatbot Workflow

The second workflow handles customer questions.

1. Customer sends a message on the Telegram Bot.
2. The Telegram Trigger receives the question.
3. The AI Agent processes the customer's request.
4. The agent searches the Supabase Vector Store for relevant information.
5. Google Gemini Chat Model generates the response.
6. Simple Memory helps maintain the conversation context.
7. A Code node (JavaScript) formats the response.
8. The final answer is sent back to the customer through Telegram.

---

✨ Key Features

- 🤖 AI-powered customer support
- 📚 Business knowledge base
- 🔎 RAG-based information retrieval
- 💬 Telegram chatbot integration
- 🧠 Google Gemini AI
- 🗄️ Supabase Vector Store
- 🔤 Google Gemini Embeddings
- 💾 Conversation memory
- ⚡ Automated responses using n8n
- 📄 Knowledge loaded from business documents
- 🔐 No API keys stored in the repository

---

🧩 Workflow Nodes

Knowledge Base Workflow

- Google Drive – Download File
- Default Data Loader
- Google Gemini Embeddings
- Supabase Vector Store – Insert Documents

Telegram Chatbot Workflow

- Telegram Trigger
- AI Agent
- Google Gemini Chat Model
- Simple Memory
- Supabase Vector Store – Retrieve Information
- Google Gemini Embeddings
- Code – JavaScript
- Telegram – Send Text Message

---

🛠️ Technologies Used

Technology| Purpose
n8n| Workflow automation
Google Gemini| AI chat model and embeddings
Supabase| Vector database / knowledge storage
Telegram| Customer chatbot interface
Google Drive| Business document storage
JavaScript| Response formatting
RAG| Knowledge retrieval and AI responses

---

💼 Use Case

This system can be adapted for many types of businesses, including:

- Beauty salons
- Bridal makeup businesses
- Clinics and hospitals
- Real estate businesses
- Restaurants
- E-commerce businesses
- Education and training businesses
- Service-based businesses
- Customer support teams

A business can provide its own documents, service information, pricing, FAQs and other knowledge, which can then be used by the AI chatbot.

---

💬 Example Customer Query

Customer:

«What is the price of bridal makeup?»

AI Chatbot:

«The bridal makeup service is available at the price listed in our knowledge base. We also provide home service for bridal makeup. The approximate service duration is around 1.5 hours. If you would like to book an appointment or make a payment, please contact the business using the provided booking details.»

The response is generated using information retrieved from the business knowledge base stored in Supabase Vector Store.

---

🎯 Why RAG?

Instead of relying only on the AI model's general knowledge, this chatbot retrieves relevant information from the business's own knowledge base.

This allows businesses to provide information such as:

- Service prices
- Service details
- FAQs
- Business policies
- Opening hours
- Appointment information
- Product information
- Company documentation

The knowledge base can be updated without rebuilding the entire chatbot.

---

🎥 Demo Video

The demo shows a customer asking a question through Telegram and the AI Agent retrieving the relevant information from the Supabase knowledge base before sending the response.

AI Knowledge Base Chatbot Demo

"Watch the Demo" (./AI-Knowledge-Base-Chatbot-RAG_Demo.mp4)

---

📊 Project Status

Completed portfolio project.
