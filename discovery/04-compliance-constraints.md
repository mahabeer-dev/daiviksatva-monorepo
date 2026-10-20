# Compliance constraints

The lines this project does not cross, and the reasoning behind each one. A rule without its
reasoning gets reversed by whoever next finds it inconvenient, so the reasoning is the point.

**Nothing here is legal advice, and none of it is a warranty.** Webgrove can build sensibly
and explain where data sits. It cannot warrant anyone's compliance, and it does not advise the
clinic on their own professional obligations.

## 1. No patient data on anything Webgrove builds

**The rule.** The website stores no patient data. No intake questionnaires, no medical-history
fields, no report or image uploads, no stored enquiries, no patient records.

**Why.** The moment a site stores a patient's medical information, whoever runs it becomes a
**Data Fiduciary** under India's DPDP Act: consent notices, a registered consent manager,
retention limits, breach notification, and patient rights of access, correction and erasure.
Health data also cannot be transferred outside India without explicit consent — and the stack
runs on Vercel, which is not in India. A report uploaded to a form on that stack is a
cross-border transfer of health data on day one.

A solo developer holding other people's medical records is a liability that does not price.
Not at ₹50,000, not at ₹200,000.

**What replaces it.**

| Layer                               | Where it lives                          | Who holds the data                    |
| ----------------------------------- | --------------------------------------- | ------------------------------------- |
| Marketing site, appointment request | the Webgrove build, on Vercel           | no patient data at all                |
| The actual conversation             | the clinic's own WhatsApp, phone, email | the practitioners                     |
| Any intake, notes or records        | the clinic's own systems                | **the practitioners, as controllers** |

**Consequence for the requested CRM.** The appointment / session / history / reminders /
medicine-catalogue / payments / audit system discussed on 2026-10-17 is **out of scope**. Its
feature names may appear in a plan only as future discovery, never as a deliverable, a
prototype or a quote. This is not a negotiating position; it is the standing rule from
`decisions/no-patient-data-on-a-website.md`, established from the Blessings Homoeo Clinic
enquiry on 2026-10-11, where the same answer was given and was the right one.

A medicine _catalogue_ with no patient linkage is a content problem, not a data problem, and
could be revisited on its own. Anything that joins a medicine to a person cannot.

## 2. No cure claims, no success rates

**The rule.** The site does not claim to cure anything, and does not publish the "99% success"
figure mentioned in the meeting. Therapies are described by what they involve and what they
address.

**Why.** India's Drugs and Magic Remedies (Objectionable Advertisements) Act, 1954 restricts
advertisements that claim to cure specified conditions, and AYUSH advertising norms apply on
top. Whether any particular sentence falls foul of them is the clinic's own professional and
legal call — not Webgrove's to assess. The rule here is simply that such claims do not get
published on a site Webgrove builds, which keeps the question from arising.

A success percentage has a second problem independent of the law: it is unverifiable, and an
unverifiable number on a clinic's homepage reads as marketing to exactly the careful reader who
was about to trust them.

## 3. No patient testimonials

**The rule.** No patient testimonials, reviews or testimonial videos — not in the site, not in
this repo, not in Slack. They were offered in the meeting. They are not to be requested,
stored or processed. If they arrive unasked, they are deleted rather than filed.

**Why, in two parts.** Indian medical-council advertising rules bar practitioners from
endorsing services, so asking a clinician for a patient testimonial asks them to breach their
own professional code. And a patient's words about their own condition **are** patient data —
accepting a video means holding health data about an identifiable person, which rule 1 exists
to prevent.

**What is fine.** A review of _Webgrove_ written by the clinic owner is ordinary commercial
practice — a customer reviewing a supplier, a different thing entirely. Google reviews the
clinic receives organically are theirs, on Google's platform, and nothing to do with this
build.

## 4. Scope of advice

Two lines never crossed:

- **Do not offer "privacy and security safeguards" as a warranted feature.** Building sensibly
  and explaining where data sits is honest. Warranting their compliance is not.
- **Do not advise on their teleconsultation or practice obligations.** This is a holistic health
  and Ayurveda practice (settled 2026-10-20), so it sits under NCISM rather than the NMC, with
  AYUSH advertising norms on top. "That is your professional call" is a better answer than a
  guess.

## 5. Claims about Webgrove itself

From `business/webgrove.md`, and they apply to every document in this folder:

- Voice is **first person singular** — "I design and build", never "we" or "our team". The
  pitch depends on it being obvious that this is one person.
- Factual claims about Webgrove derive from `lib/site.ts` in the website repo. Do not restate
  them from memory. Six client sites are live, five of them in Tricity; the sixth is in
  Brampton, Canada and must never be implied to be local.
- No superlatives, no "best" or "No. 1", no scarcity, no urgency theatre, **no discounting.**
  This is a positioning decision, not a mood.

## 6. What must never land in this repo

- Patient names, conditions, reports, photographs, testimonial videos or intake material.
- Credentials of any kind — registrar logins, DNS passwords, Google account access, API keys.
  Those are shared directly and live in a password manager.
- Anything that would be a problem read aloud. Assume an LLM reads every file here.
