<!--
Title: Customer Support Email Automation System | Langchain/Langgraph Integration
Description: Automate customer support emails with our system built using Langchain/Langgraph. Features include email categorization, query synthesis, draft email creation, and email verification.
Keywords: Customer support automation, email automation, Langchain, Langgraph, AI email agents, Gmail API, Python email automation, email categorization, email verification, AI agents, AI tools
Author: jibitesh jena
-->

# 🚀 Customer Support Email Automation with AI Agents and RAG

> Build AI-Powered Email Automation Using AI Agents + RAG!

---

## 📑 Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [How It Works](#how-it-works)
- [System Flowchart](#system-flowchart)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Contact](#contact)

---

## Introduction

In today's fast-paced environment, customers demand quick, accurate, and personalized responses. Managing large volumes of emails, categorizing them, crafting appropriate replies, and ensuring quality consumes significant time and resources, often leading to delays or errors.

**Customer Support Email Automation** is an AI solution designed to enhance customer communication for businesses. Leveraging a Langgraph-driven workflow, multiple AI agents collaborate to efficiently manage, categorize, and respond to customer emails. The system also implements RAG (Retrieval-Augmented Generation) technology to deliver accurate responses to any business or product-related questions.

---

## Features

### 📧 Email Inbox Management with AI Agents
- Continuously monitors the agency's Gmail inbox
- Categorizes emails into customer complaint, product inquiry, customer feedback, or unrelated
- Automatically handles irrelevant emails to maintain efficiency

### 🤖 AI Response Generation
- Quickly drafts emails for customer complaints and feedback using Langgraph
- Utilizes RAG techniques to answer product/service-related questions accurately
- Creates personalized email content tailored to each customer's needs

### ✅ Quality Assurance with AI
- Automatically checks email quality, formatting, and relevance
- Ensures every response meets high standards before reaching the client

---

## How It Works  

1. **Email Monitoring** - The system constantly checks for new emails in the agency's Gmail inbox using the Gmail API
2. **Email Categorization** - AI agents sort each email into predefined categories
3. **Response Generation**
   - For complaints or feedback: The system quickly drafts a tailored email response
   - For service/product questions: The system uses RAG to retrieve accurate information from agency documents and generates a response
4. **Quality Assurance** - Each draft email undergoes AI quality and formatting checks
5. **Sending** - Approved emails are sent to the client promptly, ensuring timely communication





---

## Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Langchain & Langgraph** | AI agents workflow development |
| **Langserve** | API development & deployment (FastAPI) |
| **Groq and Gemini APIs** | LLMs access |
| **Google Gmail API** | Email integration |

---

## Getting Started

### Prerequisites

- Python 3.7 or higher
- Groq API key
- Google Gemini API key (for embeddings)
- Gmail API credentials
- Python libraries (see `requirements.txt`)

### Setup

1. **Clone the repository:**

   ```sh
   git clone https://github.com/jibitesh/langgraph-email-automation.git
   cd langgraph-email-automation
   ```

2. **Create and activate a virtual environment:**

   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required packages:**

   ```sh
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**

   Create a `.env` file in the project root with your API keys:

   ```env
   MY_EMAIL=your_email@gmail.com
   GROQ_API_KEY=your_groq_api_key
   GOOGLE_API_KEY=your_gemini_api_key
   ```

5. **Ensure Gmail API is enabled:**

   Follow [this guide](https://developers.google.com/gmail/api/quickstart/python) to enable Gmail API and obtain your credentials.

### Running the Application

**Start the workflow:**

```sh
python main.py
```

The system will monitor your Gmail inbox, categorize emails, and generate responses.

**Deploy as API:**

```sh
python deploy_api.py
```

Access the API at `localhost:8000`, with documentation at `/docs` and a playground at `/playground`.


### Customization

Customize agent behavior by modifying methods in the `Nodes` class or prompts in the `src` directory.

To add your own agency data:

1. Place data files in the `data` folder
2. Create the vector store:

   ```sh
   python create_index.py
   ```

3. Update the data path in the configuration

### Contributing

We welcome contributions! Feel free to:
- Open issues for bugs or feature requests
- Submit pull requests with improvements

---

## Contact

For questions or suggestions, reach out at **jibitesh.jena@gmail.com**
