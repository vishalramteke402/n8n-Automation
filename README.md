🏡 AI Lead Qualification System (n8n + MCP)

An end-to-end AI-powered lead qualification and site visit booking system built using n8n, MCP (Model Context Protocol), and Google Sheets.

This system simulates a real estate sales assistant that chats with users, qualifies leads, schedules site visits, and stores confirmed leads automatically.

📌 Project Overview

This project consists of two interconnected n8n workflows:

MCP Client – Lead Qualification Agent

MCP Server – Lead Storage & Automation

Together, they create a seamless conversational sales pipeline from first contact → booking confirmation → CRM storage.

🧩 Architecture Overview
User Chat
   ↓
MCP Client (AI Agent)
   ↓
Lead Qualification & Booking
   ↓
MCP Server Trigger
   ↓
Google Sheets (CRM Storage)

🔹 Workflow 1: MCP Client – Lead Qualification
📁 Workflow Name

MCP_Client_Lead_Qualification

🎯 Purpose

Acts as an AI Sales & Lead Qualification Agent that:

Engages users in natural conversation

Collects requirements (e.g., 2BHK)

Offers property details

Schedules site visits

Collects customer details

Sends structured data to MCP Server

⚙️ Nodes Used
Node	Description
When Chat Message Received	Triggers workflow when user sends a message
AI Agent	Conversational AI handling sales logic
Google Gemini Chat Model	LLM used for responses
Simple Memory	Maintains chat context
MCP Client Tool	Sends structured lead data to MCP Server
🧠 AI Agent Responsibilities

Introduces itself as a real estate assistant

Asks qualifying questions (budget, configuration, interest)

Suggests property options

Schedules site visits

Confirms name and phone number

Sends finalized lead data to MCP Server

💬 Example Conversation Flow
User: hi
AI: Hello! I'm Sarah, a lead qualification agent...
User: 2bhk
AI: Our 2BHK apartments start at ₹50 Lakhs...
User: yes
AI: What time works best for a site visit?
User: 3PM
AI: Please confirm your name and mobile number
User: Vishal, 9168747489
AI: Your site visit is confirmed!

🔹 Workflow 2: MCP Server – Lead Storage
📁 Workflow Name

MCP_Server_Lead_Qualification

🎯 Purpose

Acts as a backend automation server that:

Receives structured lead data from MCP Client

Stores lead information in Google Sheets

Acts as a lightweight CRM

⚙️ Nodes Used
Node	Description
MCP Server Trigger	Receives lead data from MCP Client
Google Sheets – Append Row	Stores lead details in a sheet
📊 Stored Lead Fields (Example)

Name

Mobile Number

Property Type

Location

Site Visit Date

Site Visit Time

📂 Google Sheets as CRM

Acts as a centralized lead database

Automatically updated on every confirmed booking

Easy to connect with further automations:

WhatsApp follow-ups

Email reminders

Sales dashboards

🚀 Key Features

✅ AI-powered conversational lead qualification
✅ Automated site visit booking
✅ Persistent chat memory
✅ MCP-based client-server architecture
✅ Google Sheets CRM integration
✅ Scalable & reusable workflow design

🛠️ Tech Stack

n8n – Workflow automation

MCP (Model Context Protocol) – Tool communication

Google Gemini – Conversational AI

Google Sheets – Lead storage

AI Agent + Memory – Context-aware conversations

📈 Use Cases

Real Estate Lead Qualification

AI Sales Assistant

Appointment Booking Bots

CRM Automation

Conversational AI Demos

Portfolio / Client Proof-of-Concept

🔮 Future Enhancements

WhatsApp / SMS notifications

Email confirmation to customers

Calendar integration (Google Calendar)

Lead scoring logic

Multi-project property handling

👤 Author

Vishal Ramteke
