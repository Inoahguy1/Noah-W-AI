# Truevine Systems

## At a glance

- **What it is:** ready-to-run AI systems I offer to small service businesses through Truevine Automation, my freelance automation business.
- **Tech:** Python 3.10+ standard library, SQLite, an Obsidian vault of Markdown notes as the knowledge store, free local speech-to-text (faster-whisper), Claude Code or a free local model through Ollama, and a small web dashboard.
- **How AI is used:** voice notes are transcribed on the computer and Claude turns them into a draft report that a person signs off. The company brain answers questions from the business's own notes and cites its sources. The intake system drafts follow-ups in the owner's voice. Claude runs with no tools, so a prompt can only make it write text, and every system has a no-AI fallback.
- **Skills it shows:** turning AI into products a non-technical owner can run, human sign-off steps, local-first design, and keeping costs at zero.
- **How I built it:** I designed this and built it with Claude Code as my pair programmer. I set the goals and the rules, worked through the code and tests with Claude, and reviewed and tested every change myself.
- **Tests:** 57, all offline.

## The systems

| | System | What it does |
|---|---|---|
| 1 | **Voice note to report** | A field worker records a voice note. It's transcribed on the computer, matched to the right job, and turned into a branded PDF report. A person reviews the draft and signs it off, then the PDF is filed in the client's folder and emailed to the job's contacts. |
| 2 | **Intake and follow-up** | Weekly social posts in the owner's voice, an interest form, a simple CRM, welcome email and text, intake questions, a signed agreement, booking with a calendar invite, and reminders at every step until it's done. |
| 4 | **Company brain** | Answers the team's questions from the company's own notes, documents, email, calendar, Asana and HubSpot, with sources. Daily briefing, project recaps, meeting notes filed in the right folder. |
| + | **First-client finder** | Its only job is landing the first client: it imports lead lists, ranks them, writes a daily plan (5 new contacts, follow-ups at 4 days), drafts every message, and keeps the scorecard. **It never sends anything.** |
| + | **Website hunt** | Give it a niche and regions. It finds the businesses on OpenStreetMap, checks each website (missing, broken or old) and lists rebuild candidates with the contact details they published themselves. |


## What's free, what isn't

Everything here runs free and locally. Where a paid service would usually do the job, a free
path is built in instead, and the paid one is a hook you can switch on later with your own key.
In short:

- **Texts**: no SMS service needed. Texts wait in the dashboard's Outbox with a "Text from my
  phone" button that opens your phone's messages app, filled in. Twilio is a placeholder hook.
- **Social posts**: written for you every week; you paste them into Meta Business Suite,
  LinkedIn or Google Business Profile (all free). Nothing posts by itself.
- **Payments**: not built yet, on purpose. There's a marked place for it in the funnel.
- **Google Docs** (`.gdoc`) have no text on disk; download them as `.docx` into the synced folder.

## Ground rules built into the code

- Nothing goes to a client until a person approves it (reports), and every message a lead gets
  has a one-click stop link.
- The finder and the first-client agent only draft. A person sends every outreach message.
- Contact details come only from what a business published itself. No people-search sites, no
  guessed emails.
- Secrets live only in environment variables named in the config. Never commit `.env`,
  `truevine-systems.json` or `data/`.
- Claude Code runs with no tools, no MCP servers and no personal settings, so a prompt can't
  make it do anything but write text.

---

**Source code:** private. I'm happy to walk through it or give a live demo. All sample data is fictional (example.com emails, 555 phone numbers).

[Back to all projects](../README.md)
