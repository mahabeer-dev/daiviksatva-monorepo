# Requirements

What the website has to do. Derived from the 2026-10-17 meeting and the earlier calls; every
item traceable to something asked for, not invented. Page count is deliberately presented as a
decision, not an assumption — see [05-scope-options.md](05-scope-options.md).

## The core tension

They asked for **a separate page per therapy**. The Clinic tier covers **up to five pages**.
Those two things do not both fit unless the therapy list is very short. Everything in this
document is written so the content model works either way: therapies are authored as discrete
blocks, which can render as sections of one services page now and split into their own pages
later without rewriting the content.

## Sitemap — five-page shape

Assumes Clinic tier. The flex page is whichever of the alternatives matters most to them.

1. **Home** — what the practice is, the therapies at a glance, practitioners, hours, location,
   and the appointment call-to-action repeated at top and bottom.
2. **About** — the practice and the team. Tenure line only if C1 is evidenced.
3. **Services / Therapies** — every therapy as its own titled, anchor-linked block, with its
   own description and "request an appointment" action. Anchors mean a therapy can be linked
   directly (`/services#panchakarma`) even before it has a page of its own.
4. **Contact & Appointments** — hours, address, map, phone, WhatsApp, and the request form.
5. **Flex** — one of: _Diet & Yoga guidance_, _Our medicines_, or the single flagship therapy
   as a full page. Pawan picks.

A blog or articles section is not in the five. It is the usual next thing a clinic wants, and
it is the right vehicle for the content a Google Business Profile rewards, so the build should
leave room for it rather than design it out.

## Appointment requests — how this works, and why

**The visitor requests; the clinic confirms.** There is no calendar, no slot picker, no
confirmed booking, and no account.

Primary action: **a WhatsApp deep link** (`wa.me`) with a short pre-filled message naming the
service of interest. It opens their own WhatsApp, where the clinic already works, and it
carries no data through anything Webgrove runs.

Secondary action: **tap to call**, during published hours.

Tertiary: **a short form** — name, phone, service of interest, preferred day and time window.
Submissions are emailed to the clinic. The site stores nothing.

Explicitly absent, by design:

- **No symptom, condition or medical-history field.** Not even an optional free-text box — a
  free-text box is where health data arrives.
- **No file uploads.** No reports, prescriptions or images.
- **No database of enquiries**, no CRM, no patient records.

This is the same shape as the design recorded in `decisions/no-patient-data-on-a-website.md`:
the marketing site and the enquiry sit on the Webgrove build, the conversation happens on the
clinic's own WhatsApp and phone, and any records live with the practitioners as controllers.
Webgrove never becomes custodian of patient data. The reasoning is in
[04-compliance-constraints.md](04-compliance-constraints.md).

## Content model

Each **therapy** is one authored record, whatever it renders as:

| Field               | Required | Note                                                                 |
| ------------------- | -------- | -------------------------------------------------------------------- |
| Name                | yes      | As the clinic calls it                                               |
| One-line summary    | yes      | For cards and the home page                                          |
| Description         | yes      | What it involves, what to expect in a session                        |
| Suited to           | optional | **Described in terms of what the therapy addresses — never "cures"** |
| Duration / sessions | optional | Practical expectation-setting                                        |
| Image               | optional | Falls back to a typographic card if absent                           |

Each **practitioner**: name, role, qualifications, photo, short bio. All blocked on B5.

## Non-functional

- **Mobile first.** A local clinic's traffic arrives on a phone from Google or a shared
  WhatsApp link. The phone layout is the design, not an adaptation of it.
- **Fast on a mid-range Android on mobile data.** Images sized and compressed; no heavy
  carousels or video backgrounds.
- **Typography: Poppins** — 400 body, 500 nav and labels, 600 section headings and buttons,
  700 headlines. Devanagari is covered if C7 goes bilingual.
- **Palette: the clinic's own**, established from their approved assets once C5 lands. The
  Webgrove navy/blue is Webgrove's identity, not theirs.
- **Accessible by default** — real heading order, labelled form fields, visible focus states,
  text contrast that passes on the phone in daylight. A clinic's audience skews older than
  average.
- **Discoverable** — per-page titles and descriptions, local business structured data, a
  sitemap, and a Google Business Profile that matches the site's name, address and hours
  exactly. This is the channel that has actually produced leads.
- **No analytics or third-party script without Mahabeer's explicit yes**, and none that needs
  a new paid account.

## Out of scope for the website build

Named here so they cannot drift in:

- Patient-record CRM of any kind — appointments, sessions, history, reminders, medicine
  catalogue, payments, audit. **Not a deliverable, not a prototype, not a quote.**
- Online payments or fee collection.
- Video consultation hosting or scheduling.
- Patient intake forms, questionnaires or document uploads.
- Social-media production or management — separate decision, see B7.
- Practo profile setup — a directory listing the clinic owns and controls, not a website
  feature.
