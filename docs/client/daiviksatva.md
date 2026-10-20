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
- **Discipline: holistic health** (encompassing Ayurveda). **Settled 2026-10-20 by Mahabeer** —
  **not** homeopathy; the "homeopathic" description from the 2026-09-30 call was wrong. All
  client-facing copy describes the practice as holistic health, consistent with the clinic name.

## What exists today

- **Prototype sent 2026-10-03:** https://daiviksatva.webgrove.in/ — photos, reviews and team
  details are placeholders. Explicitly flagged as such to Pawan.
- **Domains confirmed 2026-10-20** (registrar screenshot from Pawan): `daiviksatva.com`
  (expires 5 Jul 2027), `daiviksatva.in` (10 Jul 2027), `daiviksatva.org` (26 Jul 2027),
  `daiviksatva.co.in` (26 Jul 2027). Spelling is **daiviksatva**, matching the prototype
  subdomain. Registrar not visible in the screenshot and still needed for DNS. One must be
  primary, the other three redirecting — recommended primary is `.com`.
- **No Google presence found 2026-10-20.** A search by clinic name returns no listing or
  reviews. Getting the Google Business Profile claimed is likely the highest-value free action
  available to them.
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

## Commercials — priced 2026-10-20

- **Website: ₹40,000**, 20% (₹8,000) upfront. Against the ₹50,000 Custom tier quoted in the
  meeting and Pawan's stated ~₹30,000 budget. The reduction is tied to a **scope change** —
  online appointment booking moves out of the website into the CRM stage — so the client docs
  present it as smaller scope, not a discount.
- **Social media: ₹35,000/month** against a ₹45,000 standard rate, justified by the long-term
  relationship. This one **is** a straight reduction with no scope change, and pricing was never
  discussed in the meeting, so the docs present it as a fresh proposal.
- Both supersede the standing "no discounting" line in `business/webgrove.md` for this client.
  Mahabeer's decision, made with the budget gap in front of him.
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
  obligations — Ayurveda in India sits under NCISM, not the NMC.
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

- [x] ~~Confirm whether the practice is homeopathy, Ayurveda or both~~ — holistic health, settled
      2026-10-20. Exact clinic name for publication still to confirm.
- [ ] Confirm practitioner names, spellings and roles.
- [x] ~~Confirm the domain they hold~~ — four confirmed 2026-10-20; registrar and primary still open.
- [ ] Get the approved service list, clinic timings, address, contact number, logo and photos
      — over WhatsApp, from Pawan.
- [ ] Settle Clinic ₹29,999 vs a Custom quote, and whether any social service is being offered.

## Scheduling constraint

Mahabeer works weekdays 09:00–19:00 IST at indiit solution. Do not propose or confirm meetings
in those hours without an explicit exception. Replies and follow-ups move on a short clock —
clients in India expect speed — but no urgency theatre toward the client.
