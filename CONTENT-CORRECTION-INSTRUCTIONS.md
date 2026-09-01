# Radiant Nutrition — Content Correction Instructions
**Prepared for:** Mike
**Date:** 2026-09-01
**Local source:** `/Users/mikemontes/My Projects/TheTribeMaker/Radiant Nutrition/` (multi-page HTML prototype; client-facing pages audited: `index.html`, `services.html`, `team.html`, `contact.html`, `faq.html`, `booking.html`, `blog.html`, `privacy.html`, `terms.html`, `agreement.html`, `404.html`)
**Live source:** https://radiantnutrition.com/ (GoHighLevel / LeadConnector SPA). Additional official mirror pages with full dietitian bios: https://jannaweaver.com/about , https://jannaweaver.com/team , https://jannaweaver.com/about-716785
**Scope:** Instruction document only. Do not invent. Correct wrong; remove made-up (replace only with verified live/official text or leave blank).
**Nancy QC:** 2026-09-01 — RN-005 KEEP (Jenny credentials present). Outside verify pass: strengthen RN-001/004; rewrite RN-002 (NPI fax is 940-464-9888, not 209-3022); Mom-Approved independently confirmed; Best of Denton County remains org-claim only.

## How to use this file
For each issue below, follow **Required action** exactly. Do not invent replacement copy. When an action says **CORRECT TO**, use the quoted live/official text (or the stated phone/URL/fact) verbatim. When it says **REMOVE**, delete the claim; replace only if a **REMOVE AND REPLACE WITH** quote is provided from live/official. Items marked **CONFLICT** need Mike’s choice — both sides are quoted. Live homepage “team” showing spa roles is **unreliable**; do not copy it into local.

## Summary counts
| Classification | Count (issue blocks) |
|---|---|
| WRONG | 2 (RN-003, RN-006) |
| MADE UP / UNVERIFIED | 9 (RN-008–RN-012, RN-013★ portion, RN-016, RN-020, RN-021) |
| CONFLICT | 4 (RN-001, RN-002, RN-004, RN-014) |
| KEEP / live-fixed OK | 3 (RN-005, RN-018, RN-019) + Mom-Approved KEEP + verified list below |
| Live unreliable warning | 1 (RN-017 spa team — do not copy) |
| Missing-from-local optional | 1 (RN-007) + optional notes section |

> Counts reflect **material content issues** in the local production-bound build (not CSS placeholder classes, form input placeholders, or internal tool pages). Internal tools (`admin`, `aeo`, `seo`, `audit`, `brand`, `blog-planner`, `customer-journey`, `smart-form`, login/forgot/reset) were not treated as client-facing production copy.

## Issues (one block per item)

### RN-001 — Header phone `(940) 260-3644` vs booking/FAQ phone `(940) 464-9800`
- **Classification:** CONFLICT
- **Location (local):** Sitewide header/nav phone on all client pages (e.g. `index.html`, `contact.html`, `team.html`, `faq.html`, `booking.html`, …); also JSON-LD / `tel:` links where present
- **Local text (quote):** Header shows `(940) 260-3644`; body/FAQ/booking and contact “Phone” often show `(940) 464-9800`
- **Live / official evidence (quote):** Live header/contact also shows `(940) 260-3644`. Live FAQ “How do I schedule an appointment?” and “How can I get in touch…” quote: `contacting our office at (940) 464-9800` / `call our office at (940) 464-9800`. Live contact block also shows `940-209-3022` alongside `(940) 260-3644`
- **Why it matters:** Conflicting public NAP phones confuse callers and hurt local SEO/trust. Live itself is inconsistent.
- **Required action:** Mike must choose **one primary voice number** for production. Quoting both live usages: header `(940) 260-3644` vs FAQ/scheduling `(940) 464-9800`. Outside verification (2026-09-01): `(940) 464-9800` is the number explicitly called “office” / scheduling on FAQ, press (City Lifestyle, VoyageDallas, DFWChild), and NPI aggregators; `(940) 260-3644` is official but mainly header/“Call us!”. **Nancy recommends** standardizing production on `(940) 464-9800` unless the client says the header number is the real main line. After choice: make **every** header, footer, FAQ, booking CTA, `tel:`, and schema use that single number; keep fax separate (see RN-002). Do not invent a third number.

### RN-002 — `(940) 209-3022` labeled Fax locally; NPI fax is a different number
- **Classification:** CONFLICT / likely WRONG as fax
- **Location (local):** `contact.html` (“Fax”), `index.html` contact strip (“(940) 209-3022 — Fax”)
- **Local text (quote):** `Fax` / `(940) 209-3022 — Fax`
- **Live / official evidence (quote):** Live footer lists `940-209-3022` next to voice numbers **without** a Fax label. Outside verification (2026-09-01): NPI directories list fax **`940-464-9888`** for Janna Weaver Nutrition & Wellness and for Jennifer Brewton at Suite F — **not** `209-3022`. Role of `209-3022` on the marketing site remains unlabeled/ambiguous.
- **Why it matters:** Calling the wrong number “Fax,” or inventing a fax label, breaks clinical/admin workflows and NAP trust
- **Required action:** Do **not** publish `209-3022` as Fax unless the client confirms that label. Ask the client which is true: (a) `209-3022` is fax, (b) `209-3022` is a second voice line, or (c) remove it. If a fax must appear and client confirms NPI: CORRECT TO `940-464-9888` labeled Fax — only after client confirmation (do not invent). Until then: REMOVE the Fax label on `209-3022` or REMOVE the number from public pages.

### RN-003 — Social URLs use `/radiantnutrition` instead of live `/radiantnutritionrds`
- **Classification:** WRONG
- **Location (local):** Nav/footer/social links sitewide + `index.html` JSON-LD `sameAs` (e.g. `index.html`, `contact.html`, `team.html`, …)
- **Local text (quote):** `https://www.facebook.com/radiantnutrition` and `https://www.instagram.com/radiantnutrition`
- **Live / official evidence (quote):** Live homepage links: `https://facebook.com/radiantnutritionrds` and `https://instagram.com/radiantnutritionrds`
- **Why it matters:** Wrong social destinations = broken brand presence / possible unrelated pages
- **Required action:** CORRECT TO: `https://facebook.com/radiantnutritionrds` and `https://instagram.com/radiantnutritionrds` (update every occurrence including schema `sameAs`)

### RN-004 — Office hours contradict live hours
- **Classification:** CONFLICT
- **Location (local):** `contact.html` — Office Hours table
- **Local text (quote):** `Monday–Thursday 9:00 AM – 5:00 PM`; `Friday 9:00 AM – 3:00 PM`; `Saturday & Sunday Closed`
- **Live / official evidence (quote):** Live homepage IN-OFFICE VISIT: `Mon–Fri 8:00am–5:00pm`; `Saturday 9:00am–4:00pm`; `Sunday CLOSED`
- **Why it matters:** Wrong hours = missed appointments / lockouts
- **Required action:** Mike chooses which schedule is currently true. Outside verification prefers **live official** hours (Mon–Fri 8–5 / Sat 9–4 / Sun closed). DentonCountyLocal lists a different weekday pattern — do **not** copy that directory. If live is authoritative: CORRECT TO live hours quoted above. If local is a known client correction of stale live hours: keep local and update live later — mark decision in commit notes. Do not invent a hybrid schedule.

### RN-005 — Jenny Brewton credentials on team card (QC note)
- **Classification:** KEEP (verified present)
- **Location (local):** `team.html` — Jenny Brewton card
- **Local text (quote):** Visible card includes `Jenny Brewton` plus credential line `RDN, LD` (and alt text / schema also say `Jenny Brewton, RDN, LD`)
- **Live / official evidence (quote):** Live/official team: `JENNY BREWTON, RDN, LD`
- **Why it matters:** Earlier draft incorrectly flagged credentials as missing; they are on the card
- **Required action:** KEEP `RDN, LD` on the Jenny Brewton card. No change required for credentials. (Separate issue: do not use Jenny’s name as the *client* attribution on the Gina testimonial — see RN-006.)

### RN-006 — Testimonial mis-attribution (Gina’s Jenny review credited to Jenny Brewton)
- **Classification:** WRONG
- **Location (local):** `index.html` — Client Stories / Real Clients. Real Results.
- **Local text (quote):** Quote beginning `I've been seeing Jenny for about 10 months now...` attributed as `Recurring Client` / `Jenny Brewton, RDN`
- **Live / official evidence (quote):** Same quote attributed to `Gina Albaladejo` / `Recurring Monthly Client` (not to Jenny)
- **Why it matters:** Fabricating or swapping attribution is false advertising
- **Required action:** CORRECT TO live attribution: author `Gina Albaladejo`, role `Recurring Monthly Client`. Do **not** attribute this quote to Jenny Brewton.

### RN-007 — Missing third live testimonial (Sabrina / Talya H)
- **Classification:** MADE UP N/A — this is **MISSING FROM LOCAL** (optional)
- **Location (local):** `index.html` testimonials (only two quotes present)
- **Local text (quote):** Local shows Gina/Jenny quote (misattributed — RN-006) and Rita Lasuzzo / Janna quote; no Sabrina testimonial
- **Live / official evidence (quote):** `Sabrina is absolutely amazing! She's always full of energy and very upbeat! She actually take time to listen to your concerns then map out a full plan to get it done ! I just started using Radiant Nutrition but so far my experience has been nothing short of wonderful!` — `Talya H` / `New Client`
- **Why it matters:** Optional completeness; not a local false claim by itself
- **Required action:** Optional — REMOVE AND REPLACE WITH is N/A for a missing block; if adding a third story, use only the live Talya H quote + attribution above verbatim. Otherwise leave as-is after fixing RN-006.

### RN-008 — Peptides / compounded research peptides booking path & claims
- **Classification:** MADE UP / UNVERIFIED
- **Location (local):** `index.html` (“Peptides” booking panel); `booking.html` Peptides tab (`GLP-1s, BPC-157, TB-500, PT-141…`); `services.html` bullet `GLP-1 / peptide-paired nutrition support available`; `faq.html` “Do you support clients using GLP-1 medications or peptides?”
- **Local text (quote):** e.g. `Interested in compounded or research peptides? Our dietitians guide you through candidacy, protocols, and a paired nutrition strategy — GLP-1s, BPC-157, and more.`; `GLP-1s, BPC-157, TB-500, PT-141, and more — guided by an RDN`
- **Live / official evidence (quote):** not found on live radiantnutrition.com homepage or jannaweaver about/team/booking extracts as a bookable “Peptides” service. Live Janna bio mentions an expert panel discussion of `medications like GLP-1 injectors (Ozempic)` — that is **not** the same as offering compounded peptide protocols for booking
- **Why it matters:** Medical/supplement service claims without official source = legal/compliance risk
- **Required action:** REMOVE peptide booking panels/tabs and peptide-as-service FAQ/service bullets unless/until client supplies official copy. Do **not** invent replacements. Optional later: if keeping a GLP-1 *nutrition support* mention, use only verified live wording about the panel discussion — or client-approved text (out of scope to invent here).

### RN-009 — Named insurer list (Oscar Health, Scott & White, etc.)
- **Classification:** UNVERIFIED
- **Location (local):** `services.html` insurance pills; `faq.html` insurer list
- **Local text (quote):** `Blue Cross Blue Shield`, `Aetna`, `Cigna`, `United Healthcare`, `Humana`, `Medicare`, `Scott & White`, `Oscar Health`, `+ More`
- **Live / official evidence (quote):** Live states `Insurance companies we are currently in-network with:` and `we are in-network with several major insurance companies`. Browser pass 2026-09-01: that block shows **no insurer names or logos** (placeholder image only). Do not treat live as confirming named carriers
- **Why it matters:** Listing a plan you are not in-network with is a serious compliance issue
- **Required action:** REMOVE specific carrier names until verified against current contracts / live logo set confirmed by client. Safe interim: keep only live-verified phrasing such as `We are in-network with several major insurance companies. Many plans cover nutrition counseling at little or no out-of-pocket cost.` (from live FAQ)

### RN-010 — Cancellation fees `$50` / `$75` and related fee schedule
- **Classification:** UNVERIFIED
- **Location (local):** `faq.html`, `terms.html`, `agreement.html`
- **Local text (quote):** `Late cancellations (less than 24 hours) may incur a $50 fee`; `No-shows may incur a $75 fee` / `A $75 no-show fee applies`; agreement also `Returned checks are subject to a $35 processing fee`
- **Live / official evidence (quote):** not found on live public FAQ/home content crawled
- **Why it matters:** Fee disclosures must match real policy; inventing fees is harmful
- **Required action:** REMOVE from public FAQ/marketing pages until confirmed. For `agreement.html` / `terms.html`, REPLACE only with client-provided official policy text — do not invent. If client confirms these exact amounts, they may stay in the legal agreement after confirmation (still not invent).

### RN-011 — HSA/FSA acceptance claims
- **Classification:** UNVERIFIED
- **Location (local):** `faq.html`, `terms.html`, `agreement.html`
- **Local text (quote):** `Yes! We accept HSA (Health Savings Account) and FSA (Flexible Spending Account) cards...`
- **Live / official evidence (quote):** not found on live public pages crawled
- **Why it matters:** Payment claims must be accurate
- **Required action:** REMOVE from public FAQ until verified; keep in legal pages only if client confirms. Do not invent alternate wording.

### RN-012 — “Northlake” in blog branding
- **Classification:** MADE UP / UNVERIFIED (location branding)
- **Location (local):** `blog.html` title/meta/hero: `Argyle & Northlake TX` / `Argyle & Northlake, TX`
- **Local text (quote):** `Nutrition Blog | Radiant Nutrition – Argyle & Northlake TX`; `Radiant Nutrition · Argyle & Northlake, TX`
- **Live / official evidence (quote):** Live title/meta center on Argyle: `Radiant Nutrition | Personalized Dietitian Services in Argyle, TX`; address `306 Hwy 377, Suite F, Argyle, TX 76226`; FAQ clarifies Argyle not Roanoke. “Northlake” not found as a practice location on live extracts
- **Why it matters:** Extra city in NAP/branding can dilute or misstate location
- **Required action:** REMOVE “Northlake” from titles/tags unless client confirms a Northlake location. CORRECT TO Argyle-only branding consistent with live (e.g. Argyle, TX)

### RN-013 — Stats block `2000+` / `5★ Top-Rated` / `20 yrs`
- **Classification:** KEEP for `2000+` and `20 yrs` (verified on live about); `5★` presentation is UNVERIFIED as a star glyph
- **Location (local):** `index.html` About stats row
- **Local text (quote):** `2000+` `Happy Clients`; `5★` `Top-Rated`; `20 yrs` `Nutrition Experience`
- **Live / official evidence (quote):** Live about: `2000+` `HAPPY CLIENTS`; `TOP-RATED`; `20yrs` `NUTRITION EXPERIENCE` — live does **not** show a literal `5★` in the extracted text
- **Why it matters:** Review-star claims need a real source (Google, etc.)
- **Required action:** KEEP `2000+ Happy Clients` and `20 yrs Nutrition Experience` as matching live. For stars: REMOVE the `5★` glyph unless Mike has a verifiable review source; KEEP plain `Top-Rated` to match live wording, or REMOVE entirely if no source.

### RN-014 — Entity name `Radiant Nutrition, PLLC` on agreement vs DBA elsewhere
- **Classification:** CONFLICT / UNVERIFIED
- **Location (local):** `agreement.html` Provider line; contrast footer sitewide `Janna Weaver Nutrition & Wellness DBA Radiant Nutrition`
- **Local text (quote):** `Provider: Radiant Nutrition, PLLC` vs footer `Janna Weaver Nutrition & Wellness DBA Radiant Nutrition`
- **Live / official evidence (quote):** Live copyright/footer style is generic (`© 2026 All Rights Reserved`); emails/DBA context reference Janna Weaver / Radiant Nutrition. PLLC string not verified on live crawl
- **Why it matters:** Wrong legal entity on a client agreement is a contract defect
- **Required action:** Mike/client confirm legal entity. CORRECT agreement Provider line to the real legal name (quote whichever client confirms). Align privacy/terms entity lines. Do not invent.

### RN-015 — Prototype / non-final banner on 404
- **Classification:** MADE UP (theme/prototype leftover)
- **Location (local):** `404.html`
- **Local text (quote):** `For prototype purposes only. All content and images are not final and are only here to show what is possible.`; developer note about removing banner from React production build
- **Live / official evidence (quote):** not found on live (and must not ship)
- **Why it matters:** Prototype disclaimers must not reach production
- **Required action:** REMOVE the prototype bar, performance modal, and developer notes entirely before production

### RN-016 — Shortened dietitian bios vs fuller live official bios
- **Classification:** UNVERIFIED completeness (not necessarily false) — optional production note
- **Location (local):** `team.html` bios for Janna Weaver, Sabrina Monaco, Jenny Brewton
- **Local text (quote):** Condensed bios (e.g. Janna omits Merit Street Media panel, community board roles, VoyageDallas/Northlake City Lifestyle features; Sabrina omits OU degrees / D1 volleyball detail; Jenny omits grandfather/Parkland detail depth)
- **Live / official evidence (quote):** Full bios on https://jannaweaver.com/team and /about — e.g. Janna: `I also had the privilege of representing Radiant Nutrition as part of an expert panel on The Great Weight Debate hosted by @MeritStreetMedia...`; Sabrina: `I earned my Bachelor of Science in Nutritional Sciences... University of Oklahoma... Master of Arts in Dietetics at The University of Oklahoma Health Sciences Center`; Jenny: grandfather renal dialysis story + `Parkland's Neonatal ICU`
- **Why it matters:** Shortening is OK if remaining facts stay true; expanding must use live text only
- **Required action:** KEEP verified facts already present. Optional: REMOVE AND REPLACE WITH fuller live bio paragraphs quoted from jannaweaver.com/team (verbatim) if Mike wants parity. Do not invent new credentials.

### RN-017 — Live homepage “OUR TEAM” spa leftovers must NOT be copied into local
- **Classification:** Live unreliable (not a local defect) — WARNING
- **Location (local):** N/A (local correctly lists RDs). Live home “OUR TEAM”
- **Local text (quote):** Local team = Janna Weaver RDN LD; Sabrina Monaco MA RDN LD; Jenny Brewton (see RN-005)
- **Live / official evidence (quote):** Live home shows `Katherine Wong` `License Laser Technician`; `Nicholas Bryant` `Lead Esthetician`; `Victoria Morgan` `Body Contouring`; `Walter Jenkins` `Registered Nurse` — these contradict live testimonials/bios naming dietitians Janna, Jenny, Sabrina and the official team page
- **Why it matters:** Spa theme contamination on live is wrong; copying it would invent false staff
- **Required action:** Do **not** add those four spa names to local. Treat jannaweaver.com/team RD bios + testimonials as the official team source. KEEP local RD roster (after RN-005 fix).

### RN-018 — Rita Lasuzzo testimonial spelling
- **Classification:** KEEP (local fixed live typo)
- **Location (local):** `index.html` testimonials
- **Local text (quote):** `Radiant Nutrition is the place to go. Janna helps...` / `Radiant Nutrition's guidance`
- **Live / official evidence (quote):** Live has typo `Radiant Nutrtion is the place to go...` and `Radiant Nutritions guidance`
- **Why it matters:** Local spelling correction is good; do not “correct” back to the typo
- **Required action:** KEEP local corrected spelling of “Radiant Nutrition.” Optional: if restoring live punctuation quirks, still do **not** restore `Nutrtion`.

### RN-019 — `connect@radiantnutrition.com` usage
- **Classification:** KEEP (appears on live) — verify routing with client
- **Location (local):** `index.html`, `contact.html`
- **Local text (quote):** `admin@radiantnutrition.com` and `connect@radiantnutrition.com`
- **Live / official evidence (quote):** Both `admin@radiantnutrition.com` and `connect@radiantnutrition.com` appear in live source; Cloudflare-protected mailto decodes to `admin@radiantnutrition.com`
- **Why it matters:** Secondary inbox must actually be monitored
- **Required action:** KEEP both if client monitors both. If only admin is official public inbox, REMOVE `connect@...` from public contact — client choice; do not invent a new address.

### RN-020 — Developer instructions visible on booking page
- **Classification:** MADE UP / leftover (implementation notes shipped as visible copy)
- **Location (local):** `booking.html` — under Insurance / Self-Pay / Peptides widget areas
- **Local text (quote):** `For the embedded widget: Go to Practice Better → Settings → Share My Link → Booking Widget, set theme color #AF8A3B...` (and similar Self-Pay `#7a5c9e`, Peptides `#4a8872` notes)
- **Live / official evidence (quote):** not found as public patient-facing copy on live
- **Why it matters:** Internal build notes must not appear to end users
- **Required action:** REMOVE all “For the embedded widget…” developer instructions from the visible page. Replace widgets with real embeds when ready — no invented patient copy needed.

### RN-021 — “Best of Denton County” award claim
- **Classification:** UNVERIFIED (org claim)
- **Location (local):** `team.html` — Janna Weaver bio
- **Local text (quote):** `honored as a Best of Denton County winner for the past two years, as well as a DFW Mom-Approved provider`
- **Live / official evidence (quote):** Same sentence on https://jannaweaver.com/about and /team. Outside verification: DFWChild independently confirms **Mom Approved 2024, 2025, 2026**. No independent “Best of Denton County” winners list found this pass for Radiant Nutrition (do not confuse with other “Radiant” / Best of Denton businesses).
- **Why it matters:** Award claims need a citeable source
- **Required action:** KEEP the Mom-Approved portion. For Best of Denton County: REMOVE until an independent citation is provided, **or** Mike accepts org-claim-only risk. Do not invent a year list or publisher.

## Verified content that may stay
(brief — not a full dump)

- Business name / DBA framing: Radiant Nutrition; footer pattern `Janna Weaver Nutrition & Wellness DBA Radiant Nutrition` (confirm legal entity separately — RN-014)
- Address: `306 Hwy 377, Suite F, Argyle, TX 76226` (matches live; Argyle not Roanoke note matches live FAQ)
- Primary scheduling phone appearing in live FAQ: `(940) 464-9800` (see CONFLICT RN-001 for header)
- Email: `admin@radiantnutrition.com` (verified)
- Meta title/description pattern matching live homepage: `Radiant Nutrition | Personalized Dietitian Services in Argyle, TX` and insurance/telehealth schedule messaging
- Philosophy / first-visit ~two hours / customized plan / no one-size-fits-all — aligned with live philosophy & FAQ
- Services themes present on live messaging: weight management, sports nutrition, diabetes, pediatric, telehealth, insurance accepted, InBody scans (InBody mentioned on live about)
- Team identities verified on official team page: **Janna Weaver, RDN, LD** (founder); **Sabrina Monaco, MA, RDN, LD**; **Jenny Brewton, RDN, LD** (local credential line present — RN-005 KEEP)
- Rita Lasuzzo testimonial (keep local spelling fix — RN-018)
- Gina Albaladejo testimonial body (fix attribution — RN-006)
- Stats `2000+` happy clients and `20 yrs` nutrition experience (live about / jannaweaver about)
- DFW **Mom-Approved** / Mom Approved: KEEP (independent DFWChild confirms 2024, 2025, 2026). Local “DFW Mom-Approved provider” language may stay.
- “Best of Denton County winner for the past two years”: present on jannaweaver.com about/team as org claim, but outside verification found **no independent winners list** this pass — treat as **ORG CLAIM / UNVERIFIED**. Required action: REMOVE from public team bio until client supplies an independent citation, **or** KEEP only if Mike accepts org-claim risk. Do not confuse with unrelated “Best of Denton” / Radiant Life listings.
- Social platforms Facebook & Instagram exist for the brand (fix URLs — RN-003)

## Live content missing from local (optional production notes)
- Fuller RD bios from https://jannaweaver.com/team (see RN-016)
- Third testimonial Talya H / Sabrina (RN-007)
- Live “We Are Hiring” / job post content (https://jannaweaver.com/about-716785) including pay band `$35.00 - $40.00 per hour` — only add if Mike wants a careers page; do not invent
- Additional RD bios appearing on the hiring page crawl: **Sophia Smith, RDN, LD** and **Annie Cavalier, MS, RDN, LD** — present on about-716785 team section but **not** on the primary https://jannaweaver.com/team three-dietitian layout. Treat as **optional**: confirm with client whether they are still on staff before adding; if yes, use live bio text verbatim; if unsure, do not invent or add
- Live Saturday open hours (if RN-004 chooses live schedule)
- Live Facebook/Instagram handles with `radiantnutritionrds` suffix (RN-003)

## Contact / NAP / credential checklist

| Field | Local | Live / official | Instruction |
|---|---|---|---|
| Name | Radiant Nutrition; DBA Janna Weaver Nutrition & Wellness | Radiant Nutrition (Argyle, TX); Janna Weaver context | KEEP brand; confirm legal entity (RN-014) |
| Address | 306 Hwy 377, Suite F, Argyle, TX 76226 | Same | KEEP |
| Phone (header) | (940) 260-3644 | (940) 260-3644 | CONFLICT vs FAQ phone — RN-001 |
| Phone (FAQ / book) | (940) 464-9800 | (940) 464-9800 | Prefer for scheduling unless Mike picks header number |
| Fax / alt | (940) 209-3022 labeled Fax | 209-3022 unlabeled on live; NPI fax 940-464-9888 | Likely wrong Fax label — RN-002 |
| Email | admin@… ; connect@… | admin@… (CF mailto); connect@… in source | KEEP admin; confirm connect — RN-019 |
| Hours | Mon–Thu 9–5; Fri 9–3; Sat/Sun closed | Mon–Fri 8–5; Sat 9–4; Sun closed | CONFLICT — RN-004 |
| Social | facebook.com/radiantnutrition ; instagram.com/radiantnutrition | facebook.com/radiantnutritionrds ; instagram.com/radiantnutritionrds | CORRECT — RN-003 |
| Credentials / team | Janna RDN LD; Sabrina MA RDN LD; Jenny RDN LD (present) | Official team: Janna, Sabrina, Jenny all RDN, LD (+ MA for Sabrina). Live home spa names unreliable | KEEP RD roster; do not copy spa leftovers — RN-005 KEEP, RN-017 |

---

**Crawl notes for Mike:** `radiantnutrition.com/about`, `/team`, `/contact`, `/booking` return the same GHL shell as home via plain HTTP fetch (SPA). Full dietitian bios were verified from the linked official pages on `jannaweaver.com` (linked from the live site). Raw extracts saved under `/workspace/radiant-nutrition/raw/` and `/workspace/radiant-nutrition/raw/local-extract/`.
