# ContractorRanks

**Independent software reviews, cost calculators, and free templates for US trade contractors.**

No vendor sponsorships. No paywalls. Updated monthly.

→ **[contractorranks.com](https://contractorranks.com)**

---

## What This Is

Most software review sites are funded by the vendors they review. ContractorRanks isn't.

Rankings are built from current G2/Capterra user reviews, hands-on trial testing, and verified pricing data — not ad revenue. A tool that works well for HVAC crews may score completely differently for roofing, so we score each software per trade rather than using a single generic number.

---

## Trades Covered (10)

| Trade | Software Guide | Templates Available |
|-------|---------------|---------------------|
| HVAC | [/hvac-estimating-software](https://contractorranks.com/hvac-estimating-software) | Proposal, Service Contract, Invoice |
| Plumbing | [/plumbing-estimating-software](https://contractorranks.com/plumbing-estimating-software) | Proposal, Service Contract |
| Electrical | [/electrical-estimating-software](https://contractorranks.com/electrical-estimating-software) | Proposal, Service Contract |
| Roofing | [/roofing-software](https://contractorranks.com/roofing-software) | Proposal, Inspection Report |
| General Construction | [/construction-estimating-software](https://contractorranks.com/construction-estimating-software) | Proposal, Subcontractor Contract |
| Landscaping | [/landscape-estimating-software](https://contractorranks.com/landscape-estimating-software) | Proposal, Maintenance Contract |
| Painting | [/painting-estimating-software](https://contractorranks.com/painting-estimating-software) | Proposal, Contract |
| Mechanical | [/mechanical-estimating-software](https://contractorranks.com/mechanical-estimating-software) | Proposal |
| Concrete | [/concrete-estimating-software](https://contractorranks.com/concrete-estimating-software) | Proposal |
| Solar | [/solar-estimating-software](https://contractorranks.com/solar-estimating-software) | Proposal |

---

## Software Reviewed (25 Tools)

Ranked by pricing transparency, mobile usability, QuickBooks integration, scheduling, and verified user reviews. Minimum 50 reviews required before a tool is included.

**Enterprise / all-in-one** — ServiceTitan, Procore, BuilderTrend, Simpro  
**Mid-market** — Jobber, Housecall Pro, FieldEdge, Workiz, FieldPulse, Service Fusion, Knowify  
**Estimating-focused** — Sage Estimating, ProEst, STACK, PlanSwift, Joist  
**Roofing-specific** — JobNimbus, AccuLynx  
**Small crew / mobile-first** — Tradify, ServiceM8, Markate, Kickserv, mHelpDesk, ZenMaid, CompanyCam

Full comparison tables with pricing, pros/cons, and trade-specific scores:
→ [contractorranks.com](https://contractorranks.com)

---

## Free Calculators & Cost Guides

Real numbers sourced from contractor quotes and public datasets — no lead-gen forms required.

| Tool | What It Does |
|------|-------------|
| [Roof Pitch Calculator](https://contractorranks.com/roof-pitch-calculator) | Rise/run → degrees, multiplier, area. OSHA/IRC references included. |
| [New Roof Cost Guide (2026)](https://contractorranks.com/new-roof-cost) | Cost per sq ft by material (asphalt to slate), size, pitch, and region. |
| [Storm Damage Roof Repair](https://contractorranks.com/storm-damage-roof-repair) | 48-hour checklist, insurance claim process, common denial reasons. |
| [Plumbing Repair Cost Calculator](https://contractorranks.com/plumbing-repair-cost-calculator) | 25 job types × 17 metros × timing. Drain, leak, repipe, water heater. |
| [Electrical Estimating Courses](https://contractorranks.com/electrical-estimating-courses) | 8 real programs ranked: NECA, IEC, Mike Holt, ASPE CPE, Penn Foster. |

---

## Free Templates (29 Total)

Download any template without signing up. All formats include editable fields.

| Category | Count | Formats |
|----------|-------|---------|
| Proposals | 9 | Google Docs, Word, PDF |
| Contracts | 10 | Google Docs, Word, PDF |
| Invoices | 4 | Google Docs, Excel, PDF |
| Inspection Reports | 5 | Google Docs, Word, PDF |
| Job Cost Budget | 1 | Excel, Google Sheets |

→ [contractorranks.com/templates](https://contractorranks.com/templates)

---

## How Rankings Work

1. **Pricing** — Pulled directly from vendor sites and cross-checked against G2 listings. Updated monthly.
2. **User reviews** — Sourced from G2, Capterra, and Software Advice. We require 50+ verified reviews before a tool is included.
3. **Feature testing** — Trial accounts created for each tool. We test estimate creation, mobile job management, invoicing, and scheduling.
4. **Trade-specific scoring** — Each tool is scored independently per trade. ServiceTitan scores differently for HVAC vs. plumbing; roofing tools are assessed against roofing-specific workflows.

Affiliate links are disclosed and do not affect rankings. Full methodology:
→ [contractorranks.com/methodology](https://contractorranks.com/methodology)

---

## Tech Stack

| Layer | Tool |
|-------|------|
| Framework | Astro 5.18 (static SSG) |
| Styling | Tailwind CSS 4 |
| Type safety | TypeScript (strict) |
| Hosting | Cloudflare Workers + Static Assets |
| Data | Static JSON in `src/data/` |
| Analytics | Cloudflare Web Analytics |
| Search indexing | IndexNow (auto-pings Bing/Yandex on deploy) |

## Project Structure

```
contractorranks.com/
├── src/
│   ├── data/
│   │   ├── softwares.json       # 25 software entries
│   │   ├── trades.json          # 10 trade definitions
│   │   └── templates.json       # 29 template metadata
│   ├── lib/
│   │   ├── data.ts              # Data loaders + affiliate switch
│   │   └── schema.ts            # Schema.org JSON-LD generators
│   ├── components/              # LogoCard, SoftwareCard, etc.
│   ├── layouts/                 # Base Layout with SEO head
│   └── pages/
│       ├── index.astro
│       ├── [trade]-estimating-software.astro   # 10 trade pages
│       ├── software/[slug].astro               # 25 software pages
│       ├── templates/[slug].astro              # 29 template pages
│       ├── roof-pitch-calculator.astro
│       ├── new-roof-cost.astro
│       ├── storm-damage-roof-repair.astro
│       ├── plumbing-repair-cost-calculator.astro
│       └── electrical-estimating-courses.astro
├── public/
│   ├── robots.txt
│   └── favicon.svg
└── .github/workflows/deploy.yml
```

## Local Development

```bash
npm install
npm run dev      # http://localhost:4321
npm run build
npm run preview
```

## Affiliate Links

Every software entry in `softwares.json` has an `is_affiliate_active` flag (default: `false`). When a partner program is approved:

1. Add affiliate URL to the software entry
2. Set `is_affiliate_active: true`
3. Push to GitHub — deploys automatically

CTAs use `rel="nofollow sponsored noopener"` when affiliate is active, `rel="nofollow noopener"` otherwise.

## License

Code: MIT
Content: All rights reserved — do not republish reviews or templates without permission.

---

Visit [ContractorRanks](https://contractorranks.com) for full reviews.
