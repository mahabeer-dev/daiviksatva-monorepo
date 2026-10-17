# Client — Daiviksatva

Source of truth for who this client is and what was agreed. Imported 2026-10-17 from
`webgrove-brain/leads/daiviksatva.md` (plus `business/webgrove.md`,
`decisions/no-patient-data-on-a-website.md`, `decisions/poppins-font-identity.md`,
`me/working-style.md`). The brain vault stays the canonical log of the _relationship_;
this file is the canonical brief for the _build_. When something here changes, update the
brain note too and say why.

Facts below are split into **confirmed** and **unconfirmed** on purpose — the lead note is
explicit that several details were heard in a meeting and never verified. Nothing in the
"unconfirmed" list may appear in client-facing copy until it is checked.

## Who

- **Primary contact:** Pawan — owner. First contact 2026-09-30 ~13:00 IST, by phone.
- **Practice (per clinic WhatsApp welcome message):** Daiviksatva Holistic Health and
  Ayurveda Clinic, Sector 78, Mohali. Clinic phone 9988042121.
- **Published visiting hours (same message):** Monday–Saturday, 10:30–13:00 and 16:00–19:00.
- **Others met at the clinic 2026-10-17:** Anurag and Kriti (as reported). A further
  practitioner name sounded like "Preeti" and a holistic specialist like "deepavan" —
  spellings and roles are **not** confirmed.
- **Discipline:** Pawan first described a homeopathic clinic; the clinic name says Ayurveda;
  the meeting described a holistic practice encompassing Ayurveda. Not yet reconciled — ask.

## What exists today

- **Prototype sent 2026-10-03:** https://daiviksatva.webgrove.in/ — photos, reviews and team
  details are placeholders. Explicitly flagged as such to Pawan.
- They say they hold an existing domain; the spelling in the rough notes is unclear and must
  be confirmed before any DNS or deployment planning.
- No active website of their own. A website is their stated immediate priority because people
  keep asking for one.

## Requested scope

1. **Now — website.** Multi-page, with separate therapy/service pages and a way for visitors
   to _request_ an appointment (a request, not a booking system holding patient data).
2. **Later — social presence.** They mentioned Instagram, Facebook, YouTube, LinkedIn, Practo.
   Social-media production/management is **not** a listed Webgrove service; it needs separate
   discovery and approval, and separate pricing if it is offered at all.
3. **Later still — a CRM concept** covering appointments, sessions, history, reminders, a
   medicine catalogue, payments and audit functions.

### Hard line on item 3

A CRM holding identifiable patient records is **out of scope and must not be quoted, promised
or prototyped.** See `webgrove-brain/decisions/no-patient-data-on-a-website.md`: storing
patient data makes the operator a Data Fiduciary under India's DPDP Act, and health data
cannot leave India without explicit consent while the stack runs on Vercel. The safe shape is:
marketing site + enquiry on our build, consultation requests over WhatsApp/phone, intake and
any records in the clinic's own Google Workspace with the practitioner as controller. CRM
feature _names_ may appear only as future discovery, never as a deliverable.

## Commercials — unsettled

- Mahabeer floated the **Custom tier (from ₹50,000)**; Pawan stated a budget around
  **₹30,000**. Mahabeer said he would review the budget _after_ discussing the plan. **No
  discount was offered and none may be implied.**
- Standard tiers: Starter ₹14,999 · **Clinic ₹29,999 (up to five pages)** · Custom from
  ₹50,000 · optional care plan ₹999/month.
- Open decision: does a five-page Clinic build meet the need, or is a Custom quote required?

## Timeline — discussed, not agreed

A website "within three weeks" and social work "around day 15" were meeting conversation,
subject to review. They are **not** a committed schedule. Any client-facing plan must make
scope, price, compliance checks and dates conditional on approval.

## Content rules — non-negotiable

- **Do not publish** the reported "99% success" claim, any disease-cure language, or patient
  testimonials / testimonial videos. Indian medical-council advertising rules bar practitioner
  endorsement of services; asking for a patient testimonial asks the client to breach their own
  professional code. They may offer videos anyway — do not request, store or process them, and
  keep them out of this repo and out of Slack.
- **Tenure claims conflict** ("since 2004" vs "14 years"). Publish neither without evidence.
- No superlatives, no "best" / "No. 1", no scarcity or urgency framing, no discounting.
- Do not warrant their regulatory compliance, and do not advise on their teleconsultation
  obligations — homeopathy in India sits under NCISM/CCH, not the NMC.
- Voice is **first person singular** ("I design and build"), never "we" or "our team".

## Brand / implementation defaults

- **Typeface: Poppins** (Webgrove's primary). 400 body · 500 nav and labels · 600 section
  headings and buttons · 700 headlines and wordmark. Supports Devanagari, OFL-licensed.
- Navy/blue Webgrove palette for Webgrove-owned surfaces; the clinic's own palette is still
  to be established from their approved assets.

## Status and next steps

**Status: discovery meeting completed 2026-10-17 at the Mohali clinic. Three draft documents
prepared for Mahabeer's review the same day — not sent to Pawan.** They cover a budget-fit
five-page Clinic website option, a separate non-committed social outline, and a kickoff-input
checklist.

Blocking items before build work starts:

- [ ] Confirm the exact clinic name, and whether the practice is homeopathy, Ayurveda or both.
- [ ] Confirm practitioner names, spellings and roles.
- [ ] Confirm the domain they hold (exact spelling).
- [ ] Get the approved service list, clinic timings, address, contact number, logo and photos
      — over WhatsApp, from Pawan.
- [ ] Settle Clinic ₹29,999 vs a Custom quote, and whether any social service is being offered.

## Scheduling constraint

Mahabeer works weekdays 09:00–19:00 IST at indiit solution. Do not propose or confirm meetings
in those hours without an explicit exception. Replies and follow-ups move on a short clock —
clients in India expect speed — but no urgency theatre toward the client.
