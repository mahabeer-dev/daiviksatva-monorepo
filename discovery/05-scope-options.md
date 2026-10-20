# Scope options and the tier decision

> **Superseded on 2026-10-19 on the pricing question.** Mahabeer set the website at
> **₹40,000 with 20% upfront**, with online booking excluded from the web build and deliverables,
> code and hosting all handed to the client. The tier comparison below is kept for the reasoning
> about page count and the five-page limit, which still applies. Do not quote ₹29,999 from this
> file.

**Internal. Not for the client.** This is the analysis behind the number that goes in
[client-facing/website-plan.md](client-facing/website-plan.md).

## The problem in one line

Pawan asked for a separate page per therapy and stated a budget of about **₹30,000**. Per-page
work at that budget means the Clinic tier at **₹29,999, up to five pages** — and "a page per
therapy" does not fit in five unless the therapy list is tiny. Blocker B4 (the definitive
service list) is therefore the input that decides everything, and it is not yet answered.

Standard tiers, for reference: Starter ₹14,999 · **Clinic ₹29,999** · Custom from ₹50,000 ·
optional care plan ₹999/month. Confirm what each tier actually includes against the website
repo's own source of truth before quoting — do not restate inclusions from memory.

## Option A — Clinic, ₹29,999, five pages

Home · About · Services (every therapy as an anchored block) · Contact & Appointments · one
flex page.

**For.** Lands inside the stated budget at list price, with no discount and no erosion of the
tier structure. Delivers the thing they actually need now — people are asking for a website
and they do not have one. The content model in
[03-requirements.md](03-requirements.md) authors each therapy as a discrete record, so
splitting them into their own pages later is a layout change, not a rewrite.

**Against.** It is not literally what was asked for. A therapy that lives at
`/services#panchakarma` ranks less well on its own name than one at `/therapies/panchakarma` —
and for a local clinic, Google is the channel that has actually produced leads. If they have
ten therapies and genuinely want each one findable, Option A delays that.

## Option B — Custom, from ₹50,000

Home · About · Services index · a page per therapy · Diet & Yoga · Medicines · Contact ·
blog-ready structure.

**For.** It is the brief as stated, and the per-therapy pages are the SEO-correct shape for a
clinic competing on treatment names in Mohali.

**Against.** It is roughly **1.7× the stated budget.** Pawan named ₹30,000 unprompted, which is
usually a real ceiling rather than an opening position. Pushing Custom now risks the lead
rather than the scope — and this lead has already survived two weeks of near-silence and one
cancelled meeting.

## Option C — Clinic now, Custom phase later

Build Option A at ₹29,999. Name the per-therapy pages, the blog and the medicine catalogue as a
**separately quoted Phase 2**, with no price committed and no date implied.

## Recommendation: Option C

It is the only option that is simultaneously inside their budget, honest about what five pages
means, and aligned with what they will want in six months. It also avoids the one move that is
explicitly ruled out — discounting Custom to ₹30,000 — while still giving Pawan a real answer
to "can you do it for thirty."

**Conditions on that recommendation:**

1. **It depends on B4.** If the definitive therapy list is three or four items, Option A _is_
   the brief, and the Phase 2 framing is unnecessary. Get the list before quoting.
2. **If C7 comes back bilingual, Option A is off.** A Hindi/English site is routing and content
   work, not translated copy, and it belongs in Custom.
3. **Say "up to five pages" in writing, in the plan.** The single most likely source of friction
   on this project is a sixth page arriving as an assumption mid-build.

## What must not happen

- ~~**No discount on Custom.**~~ **Overtaken 2026-10-20:** Mahabeer priced the website at
  ₹40,000 against the ₹50,000 tier, tied to booking moving into the CRM, and social at ₹35,000
  against a ₹45,000 standard rate. His decision.
- **No CRM in the quote**, in any form, including as a priced future phase. See
  [04-compliance-constraints.md](04-compliance-constraints.md).
- **No social work folded silently into the website price.** If social is offered at all it is
  separately scoped and separately priced — blocker B7, Mahabeer's decision.

## Timing, honestly

Three weeks was floated in the meeting. Two things make that conditional:

- **It runs from the day the kickoff inputs land**, not from the day the plan is approved.
  Logo, photos, the service list and practitioner details are all on their side, and C6
  (whether usable photographs exist) is the item most likely to slip.
- **Build capacity is evenings and weekends.** Mahabeer works weekdays 09:00–19:00 at indiit
  solution. Three weeks is achievable on that footing, but a week of waiting on content does
  not compress afterwards.

State the timeline as "about three weeks from receiving everything on the checklist", and let
the checklist carry the dependency.

## Recurring costs to name before launch, not after

Domain renewal (theirs, on their registrar), hosting, and the optional care plan at ₹999/month.
Naming recurring costs up front was the right call on the Blessings enquiry and it is the right
call here — an unmentioned renewal invoice is how a good first project turns sour.
