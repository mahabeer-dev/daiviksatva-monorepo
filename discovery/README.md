# Discovery — Daiviksatva

Everything belonging to the discovery phase of the Daiviksatva project lives in this folder.
Opened 2026-10-17, the day of the on-site discovery meeting.

These documents are drafted fresh in this repo. Earlier agent-generated drafts are deliberately
**not** carried over.

## Reading order

| #   | Document                                                     | What it is                                                                              |
| --- | ------------------------------------------------------------ | --------------------------------------------------------------------------------------- |
| 01  | [01-meeting-notes.md](01-meeting-notes.md)                   | Record of the 2026-10-17 on-site meeting, with reported vs confirmed separated          |
| 02  | [02-open-questions.md](02-open-questions.md)                 | Every question that must be answered before build work starts, with owner               |
| 03  | [03-requirements.md](03-requirements.md)                     | Sitemap, page content model, how appointment requests work, non-functional requirements |
| 04  | [04-compliance-constraints.md](04-compliance-constraints.md) | The lines this project does not cross, and why                                          |
| 05  | [05-scope-options.md](05-scope-options.md)                   | Internal: Clinic ₹29,999 vs Custom from ₹50,000, with a recommendation                  |

## Client-facing documents

In [client-facing/](client-facing/). The Markdown in this repo is the **source of truth**; the
Google Docs below are what gets sent to the client. If you change one, change the other and say
so here.

**Status as of 2026-10-20: finalised and published as Google Docs, not yet sent to Pawan.**

| Document                                                     | Google Doc                                                                                   | Purpose                                                                             |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| [minutes-of-meeting.md](client-facing/minutes-of-meeting.md) | [open](https://docs.google.com/document/d/13PaVo9TU8c3TPZZZ7Q5yervBVsnWM8F9I74VWD-xjmM/edit) | Forwardable record of the 17 Oct meeting, with the points Pawan must confirm        |
| [website-plan.md](client-facing/website-plan.md)             | [open](https://docs.google.com/document/d/1KRyP0EO_limqyUJb4rD3xfApz4Xks_-_h3v2dZiXimM/edit) | 15–18 page website, **₹40,000** (20% upfront), one month from content, 4 milestones |
| [social-media-plan.md](client-facing/social-media-plan.md)   | [open](https://docs.google.com/document/d/1bdJyjLr0At-mUorcnGYAq-eI5mYtl49hE7dHrn3kjcA/edit) | Three months across Instagram, Facebook, YouTube and LinkedIn, **₹35,000/month**    |

The Docs were produced from this Markdown by `md2gdoc.py` (session scratchpad, not committed):
Poppins throughout, real heading styles, bordered tables. **This session had the Drive connector
but no Google Docs editor connector**, so a Doc cannot be edited after creation — any change
means creating a new Doc and a new link. Enable the Google Docs connector first if you need to
edit in place.

Pricing here supersedes the tier analysis in [05-scope-options.md](05-scope-options.md).
Online appointment booking is **excluded from the website** by decision — it belongs with the
clinic management system later. Both prices are below list (₹50,000 website, ₹45,000/month
social); the website reduction is tied to that scope change, the social one is not.

## Where the truth lives

- **This folder** — the discovery phase: what was learned, what is still unknown, what was
  drafted.
- [`docs/client/daiviksatva.md`](../docs/client/daiviksatva.md) — the standing build brief.
  Read it before writing any client-facing copy.
- `~/Documents/Personal/webgrove-brain/leads/daiviksatva.md` — the canonical log of the
  relationship: calls, messages, dates, status. Update it when this folder changes something
  material.

## Two rules that govern this whole folder

1. **No patient data, ever** — no names, conditions, reports, photos, testimonial videos or
   intake material, in any file here. See [04-compliance-constraints.md](04-compliance-constraints.md).
2. **No credentials, ever** — no domain registrar logins, DNS passwords, Google account access
   or API keys. Those are shared directly and live in a password manager.

## Phase exit

Discovery closes when every blocker in [02-open-questions.md](02-open-questions.md) is resolved,
the tier decision in [05-scope-options.md](05-scope-options.md) is made, and Pawan has approved
a scope in writing. Until then `apps/` stays empty.
