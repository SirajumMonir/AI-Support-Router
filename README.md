<img width="1905" height="900" alt="Screenshot 2026-04-08 092956" src="https://github.com/user-attachments/assets/4ae6a0d9-daf7-4edb-9acf-ef31b74f1ad0" />
🧠 Smart Customer Support Router (n8n + AI)

An intelligent, fully automated AI workflow that acts as a Level 1 Support triage agent. It intercepts incoming customer messages, uses Meta's Llama 3 to analyze the intent, and dynamically routes the ticket to the correct department.

🚀 Features

Omnichannel Input: Receives messages via a Telegram Bot (easily adaptable to Email or Slack).

AI-Powered Triage: Uses Groq API (Llama 3) to read unstructured natural language and output clean, structured JSON.

Dynamic Routing: Utilizes n8n's Switch node to route messages to Sales, Support, or Spam pipelines based strictly on the AI's analysis.

Zero-Cost Architecture: Runs locally on n8n with ngrok tunnels and the free-tier Groq API.

🛠️ Tech Stack

Workflow Engine: n8n (Localhost)

AI/LLM: Meta Llama 3 via Groq API

Trigger/Interface: Telegram API

Data Parsing: Custom JavaScript (JSON.parse)

💡 How it Works

A customer sends a message: "I want to buy your premium plan. What is the cost?"

The Telegram Trigger in n8n catches the webhook instantly.

The AI node processes the text and categorizes it: {"category": "Sales", "reason": "User is asking about pricing."}.

The Switch node parses the JSON and evaluates the condition, routing the data exclusively to the "Sales Team" branch for immediate follow-up.

💻 Setup Instructions

Install n8n locally via npm (npx n8n).

Expose your local server using ngrok (ngrok http 5678).

Import the workflow JSON file into your n8n instance.

Add your Telegram Bot Token and Groq API credentials.

Activate the workflow and test via Telegram!

Built as a portfolio project for AI Automation Engineering roles.
