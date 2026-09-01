# Radiant Nutrition — SCOPE.md

## Project Identity

| Field | Value |
|---|---|
| **Business name** | Radiant Nutrition |
| **Legal name** | Janna Weaver Nutrition & Wellness DBA Radiant Nutrition |
| **Tagline** | Nutrition That Fits Your Life. |
| **One-liner** | Registered dietitians who meet you where you are — building sustainable habits for lasting health. |
| **Phone** | (940) 464-9800 |
| **Email** | admin@radiantnutrition.com |
| **Address** | 306 Hwy 377, Suite F, Argyle, TX 76226 |
| **Hours** | Mon–Thu 9 am–5 pm · Fri 9 am–3 pm |
| **Production domain** | radiantnutrition.com |
| **Agency** | TheTribeMaker |
| **GitHub org** | Yavin-Digital |
| **Slug** | radiant-nutrition |
| **Prototype repo** | Yavin-Digital/radiant-nutrition-prototype |
| **App repo** | Yavin-Digital/radiant-nutrition-app |
| **Review URL** | https://radiantnutrition.clientreview.co |

## Project Type

`Dynamic PG` — Next.js + Postgres, no ecommerce  
**Scaffold:** `dynamic-pg-scaffold`

## Integrations

| Integration | Status | Notes |
|---|---|---|
| User accounts / auth | ✅ YES | NextAuth — admin login + protected admin panel |
| File uploads / storage | ✅ YES | Blog post featured images via DO Spaces (yavin-media) |
| Transactional email (SendGrid) | ❌ NO | GoHighLevel (GHL) handles all lead capture and email |
| Payment processing | ❌ NO | Booking → Practice Better (external link). Peptide Blueprint → external platform |
| WooCommerce backend | ❌ NO | |
| Age gate | ❌ NO | |
| Google Analytics (GA4) | ✅ YES | Measurement ID: `G-WNKJLGK27X` |
| Third-party chat widget | ❌ NO | |
| SMS / OtterText opt-in | ❌ NO | A2P 10DLC compliance language is on forms; no backend SMS integration |
| GoHighLevel forms | ✅ YES | Embedded iframes from `agency.jannaweaver.com` — preserve embed URLs |
| Practice Better booking | ✅ YES | External links — preserve all `practicebetter.io` URLs exactly |

## Pages

### Public Site
| Route | Prototype file | Notes |
|---|---|---|
| `/` | `index.html` | Home — hero, stats, services overview, testimonials, blog preview, CTA |
| `/services` | `services.html` | Full service list with detail cards |
| `/team` | `team.html` | Janna Weaver RD + team bios |
| `/booking` | `booking.html` | 3-tab booking: Insurance · Self-Pay · Peptides. Deep-link via `#insurance`, `#selfpay`, `#peptides` |
| `/contact` | `contact.html` | Contact info + embedded GHL form |
| `/blog` | `blog.html` | Blog listing with category filter (all posts in `allPosts` JS array) |
| `/blog/[slug]` | `blog-post-*.html` | Individual blog post with sidebar + prev/next navigation |
| `/faq` | `faq.html` | Accordion FAQ |
| `/peptide-blueprint` | `peptide-blueprint.html` | Waitlist / sales funnel for Peptide Blueprint program |
| `/smart-form` | `smart-form.html` | A2P 10DLC compliant multi-step intake form |
| `/agreement` | `agreement.html` | Service agreement / consent |
| `/terms` | `terms.html` | Terms & Conditions |
| `/privacy` | `privacy.html` | Privacy Policy |
| `/404` | `404.html` | 404 error page |

### Auth & Admin (protected)
| Route | Prototype file | Notes |
|---|---|---|
| `/login` | `login.html` | Admin login |
| `/forgot-password` | `forgot-password.html` | Password reset request |
| `/reset-password` | `reset-password.html` | Password reset with token |
| `/admin` | `admin.html` | Admin dashboard — blog post management, site config (GA4 ID, GHL embed URLs) |

### Internal / Do Not Publish
`brand.html`, `seo.html`, `aeo.html`, `audit.html`, `blog-planner.html`, `customer-journey.html`, `RadiantNutrition-*.html` — sales/research deliverables; not part of the public build.

## Brand Assets

| Asset | Location / Value |
|---|---|
| Logo | `logo.webp` in prototype root |
| Footer logo | White via CSS filter `brightness(0) invert(1)` on `.footer-logo img` |
| Primary color (Gold) | `#AF8A3B` |
| Gold light | `#C8A557` |
| Dark background | `#1A150C` |
| Body font | Open Sans or Raleway (labels / nav) |
| Heading font | Cormorant Garamond (italic style) |
| Body font | Raleway (body copy, buttons) |
| OG image | 1200×630 — reference prototype `<meta og:image>` |

## Deployment

| Field | Value |
|---|---|
| Region | SFO3 |
| App Platform plan | Basic ($24/mo) |
| Spaces folder | `radiant-nutrition` (inside `yavin-media`) |
| Database name | `radiant_nutrition` |
| Database user | `radiant_nutrition_user` |

## Legal / Compliance

- Copyright: © 2026 Janna Weaver Nutrition & Wellness DBA Radiant Nutrition All Rights Reserved.
- No age verification required.
- Privacy Policy and Terms pages exist in prototype.
- No prohibited gambling language applicable.
- A2P 10DLC disclaimer language on smart-form.html — preserve verbatim in implementation.

## Social

| Platform | URL |
|---|---|
| Instagram | https://www.instagram.com/radiantnutritionrds |
| Facebook | https://www.facebook.com/radiantnutritionrds |

## Google Maps

https://www.google.com/maps/place/Radiant+Nutrition/@33.1176464,-97.1886993,17z/data=!3m1!4b1!4m6!3m5!1s0x864dcfe6473ff6d7:0x247331e0312bf47!8m2!3d33.1176419!4d-97.186119!16s%2Fg%2F11frnsbgn9

## Key Behaviors to Preserve

- Booking page tabs are deep-linkable via URL hash (`#insurance`, `#selfpay`, `#peptides`)
- All Practice Better booking URLs must be preserved exactly
- GHL form embed src URLs must be preserved exactly
- Footer logo uses CSS filter for white — no separate white logo asset required
- Blog posts: prev/next navigation at bottom of each single post page
- Nav logo height: `71px`
