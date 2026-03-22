# 🏛️ CivicMind
> **Transforming political transparency from theory into practice through AI and Civic Tech.**

CivicMind is an application developed to combat misinformation and simplify how citizens track political activity. Through a multi-agent architecture and automated data pipelines, the app extracts, simplifies, and personalizes legislative decisions in Romania.

---

## 🚀 Core Features (Epics)

The project is divided into 4 main pillars, each managing a critical stage of the data flow and user interaction.

### 🗄️ EPIC 1: Data Infrastructure (Data Pipeline)
The engine that automatically extracts raw data from government platforms (Chamber of Deputies, Senate, Just.ro).
* **Story 1:** Automated extraction of new project IDs (Source: `cdep.ro`).
* **Story 2:** Roll-call vote scraper using Firecrawl (JSON format extraction of voting options: YES/NO/Abstain).
* **Story 3:** Integration with the `legislatie.just.ro` SOAP API to access the consolidated forms of laws.

### 🧠 EPIC 2: Artificial Intelligence Engine (Agentic Workflow)
The system that "translates" bureaucratic jargon into useful information using advanced AI models.
* **Story 4: Legislative Scout** – Processes explanatory memorandum PDFs and generates summaries (3 key ideas) + impact categorization.
* **Story 5: Critique Extraction** – Analyzes the opinions of the Economic and Social Council to generate "CON" arguments.
* **Story 6: Political Auditor** – Calculates a personalized *Impact Score*, correlating electoral promises with actual votes (Fact-checking).

### 📱 EPIC 3: User Experience (Mobile App/Web)
The citizen's interface, built for clarity and accessibility.
* **Story 7:** User profile creation (Onboarding with county and interest selection: Education, IT, Freelance/PFA, etc.).
* **Story 8:** Smart Push notification system, triggered only by laws relevant to the user's customized profile.

### 📣 EPIC 4: Action Module (Civic Engagement)
Transforming information into direct action.
* **Story 9:** Generation of email templates (via AI) and sending them to the representative deputy, directly from within the app.

---

## 📋 Product Backlog & Roadmap

Here we manage planned features for future iterations (beyond the current MVP) and ideas currently in the "Icebox".

### 🟢 Current Sprint (To Do)
- [ ] Configure daily Firecrawl script for `cdep.ro`.
- [ ] Setup PostgreSQL/Supabase database for metadata storage.
- [ ] Define System Prompts for the Scout Agent.

### 🟡 Short-Term Backlog (Ready for Dev)
- [ ] Create Figma design for Onboarding screens.
- [ ] Implement backend endpoint for the Impact Score calculation.
- [ ] Integrate push notifications via Firebase/OneSignal.

### 🔵 Icebox / Future Vision (Future Epics)
* **Epic 5: Social Sharing & Gamification** - Adding the ability to share a politician's "track record" on social media.
* **Epic 6: Local Level Expansion** - Integrating a scraper for decisions made at the Local Council / City Hall level (e.g., Bucharest, Cluj).
* **Feature:** Data visualization through charts (e.g., an interactive map of MP voting attendance in a specific county).

---

## 🛠️ Tech Stack (Proposal)
* **Scraping & Extraction:** Firecrawl API, Python
* **AI & Agents:** OpenAI/Anthropic API, LangChain / CrewAI
* **Database:** PostgreSQL (Supabase) + Vector DB (Pinecone)
* **Frontend:** React Native / Flutter

---
