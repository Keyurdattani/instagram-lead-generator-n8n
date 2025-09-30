# Instagram Lead Generator (n8n Automation)

This project is an end-to-end Instagram lead generation automation built on n8n.  
It integrates Telegram, AI-powered query handling (OpenAI), Apify Instagram scraping, and Airtable to automate the process of finding, parsing, and storing Instagram leads.

---

## Features
- Telegram Integration – Request leads directly via Telegram chat  
- AI Agent (OpenAI GPT) – Understands natural language lead requests (e.g., "Find gyms in Mumbai")  
- Instagram Scraper (Apify) – Collects Instagram profiles using Google Search scraping  
- Lead Parsing – Extracts name, username, profile URL, description, and follower count  
- Airtable Storage – Automatically saves leads for further CRM or marketing workflows  
- Scalable & Modular – Workflows separated for maintainability:  
  - Lead generator instagram scraper.json → Telegram + AI interface  
  - Instagram_scrapper.json → Scraping + Airtable integration  

---

## Tech Stack
- n8n.io (workflow automation)  
- Telegram Bot API  
- OpenAI GPT (AI Agent)  
- Apify (Google Search Scraper)  
- Airtable (Lead Database)  

---

## Example Workflow

User on Telegram → "Get me salons in Delhi"
↓
AI Agent (OpenAI GPT) parses → { lead_type: "salon", location: "Delhi" }
↓
Instagram_scrapper workflow runs → Scrapes data from Apify
↓
Airtable stores results
↓
Telegram sends formatted leads back to the user

##Example Output

Name: cloud9.gym

Username: cloud9.gym

Instagram handle: https://www.instagram.com/cloud9.gym/

Description: Managed by @digijarindia Gym|Cardio|Zumba|Yoga/Power Yoga|Steam|Dance|Functional Training|Diet|GroupX 📍Malad/Chembur/Dadar/Sion/Mahim/Andheri/Mulund

Followers: 9,700
