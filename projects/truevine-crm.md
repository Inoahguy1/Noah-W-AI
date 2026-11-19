# Truevine CRM

## At a glance

- **What it is:** the CRM I built for Truevine Automation, my freelance AI automation business. It tracks prospects through a pipeline, shows meetings on a calendar, and takes bookings straight from the form on my website.
- **Tech:** Supabase (Postgres, row-level security, sign-in, and an Edge Function in TypeScript), a vanilla JavaScript front end that installs like an app on a phone, Netlify-ready hosting, and n8n webhooks.
- **How AI is used:** a new booking can fire an n8n webhook, which is where AI follow-up (calls, texts, emails) plugs in. An Edge Function fills in missing contact details from a lead-data service (Apollo.io) while keeping the key on the server, only filling blank fields, and capping how many credits it can use each month.
- **Skills it shows:** database-level security for a public booking form, keeping API keys off the page, safe data enrichment, and wiring a CRM into automation tools.
- **How I built it:** I designed this and built it with Claude Code as my pair programmer. I set the goals and the rules, worked through the code and tests with Claude, and reviewed and tested every change myself.
- **Tests:** database rule checks on a local Postgres, plus Node tests for the enrichment logic.

All data in the tests is made up.

## How a website booking flows

1. A visitor picks a time on truevineautomation.com. The page calls `submit_booking` in Supabase
   with the public key. That function is the only thing the public key can do, besides seeing
   which times are taken (`booked_slots`).
2. The database checks the time is a real open slot, creates or updates the prospect, saves the
   meeting, moves the prospect to "Meeting booked" and, if set, sends the booking to n8n.
3. Noah signs in to the CRM (email + password, only allowlisted emails) and sees it on the
   dashboard, calendar and pipeline.

---

**Source code:** private. I'm happy to walk through it or give a live demo. All sample data is fictional (example.com emails, 555 phone numbers).

[Back to all projects](../README.md)
