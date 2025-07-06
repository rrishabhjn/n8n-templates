
# 🤖 n8n Automation Workflows

A collection of five powerful and intelligent workflows built using [n8n](https://n8n.io). These automations help streamline email communication, manage calendars, classify tasks, retrieve weather data, and build a voice-enabled Telegram assistant—all powered by AI.

![n8n](https://img.shields.io/badge/built%20with-n8n-blue)
![AI-Powered](https://img.shields.io/badge/AI-GPT--4.5%20%2F%20Whisper-critical)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

---

## 📁 Workflows

### 1. `email_auto_responder_with_goals_and_calendar.json`
**Summary**:  
Automatically replies to incoming Gmail messages by checking your Google Calendar availability and an Airtable-based goals database. Categorizes emails into five types (Meetings, Spam, Promos, Sponsorships, Check Later) and applies the right Gmail label.

**Tech stack**:
- Gmail API
- Google Calendar
- Airtable
- GPT-4.5 (LangChain agent)

---

### 2. `smart_google_calendar_agent.json`
**Summary**:  
Understands natural language queries like “Reschedule Monday’s call to Friday” or “Add yoga class tomorrow at 6 AM” and converts them into structured Google Calendar actions (create/update/search). Supports timezone handling and validation.

**Tech stack**:
- Google Calendar
- GPT-4.1 (LangChain agent)

---

### 3. `calendar_email_task_classifier_router.json`
**Summary**:  
Acts as a middleware agent that reads user queries and classifies them as email-related or calendar-related. Then routes the request to the correct agent workflow. Enables seamless orchestration between multiple sub-agents.

**Tech stack**:
- LangChain classifier
- Modular architecture (router → tools)

---

### 4. `weather_data_logger_to_airtable.json`
**Summary**:  
Fetches current weather for a selected city (e.g., Chicago, New York, New Delhi, Dubai) using the Open-Meteo API, extracts high/low temperatures for the day, and stores the data in Airtable for further use or analysis.

**Tech stack**:
- Open-Meteo API
- Airtable
- JavaScript Function Node (for temp parsing)

---

### 5. `telegram_gpt_bot_with_voice_transcription.json`
**Summary**:  
Telegram chatbot with text + voice input support. It transcribes voice messages using OpenAI Whisper, then responds with GPT-generated replies. Works both with Telegram messages and webhook calls.

**Tech stack**:
- Telegram Bot API
- OpenAI Whisper (voice → text)
- GPT-4.1 (LangChain agent)
- Memory buffer for context

---

## 🚀 Getting Started

1. Clone this repo
2. Import `.json` files into your n8n instance
3. Set up the required credentials (Gmail, Google Calendar, Airtable, Telegram, OpenAI)
4. Activate the workflows you need!

---

## 📜 License

This repository is licensed under the MIT License.

---

## 🙌 Contributions

Feel free to fork, improve, or extend these workflows. PRs are welcome!
