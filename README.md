# Plumber Site Templates

Professional one-page website templates for plumbing businesses.  
Built for AI-driven generation — every `{{PLACEHOLDER}}` gets filled with real business data.

## How to Add a Template

1. Open this repo on GitHub
2. Click **Add file → Create new file**
3. Name it `templates/your-template-name/index.html`
4. Paste your HTML (use the placeholders below)
5. Commit directly to `main`

That's it — no git CLI required.

## Placeholder System

Every template uses these exact placeholders. The generation script swaps them with real business data:

```
{{BUSINESS_NAME}}       → Joe's Plumbing LLC
{{PHONE}}               → (801) 555-0142
{{EMAIL}}               → joe@joesplumbing.com
{{ADDRESS}}             → 1234 Main St
{{CITY}}                → Salt Lake City
{{STATE}}               → UT
{{ZIP}}                  → 84101
{{HERO_HEADLINE}}       → Your Local Trusted Plumbers
{{HERO_SUBHEADLINE}}    → 24/7 Emergency Service — Free Estimates
{{SERVICES_LIST}}       → <li>Drain Cleaning</li><li>Water Heater Repair</li>...
{{ABOUT_TEXT}}          → Family-owned since 1998. Licensed and insured...
{{REVIEWS_SECTION}}     → ★★★★★ "Best plumber in town!" — Sarah M.
{{LICENSE_NUMBER}}      → UT-98472
{{EMERGENCY_BADGE}}     → 24/7 Emergency Available
{{CTA_BUTTON_TEXT}}     → Call Now for Free Estimate
{{MAP_EMBED}}           → <iframe src="https://maps.google.com/..."></iframe>
{{BUSINESS_HOURS}}      → Mon-Fri: 7AM-7PM | Sat: 8AM-4PM | Sun: Emergency Only
{{SOCIAL_PROOF_TEXT}}   → 500+ 5-Star Reviews | Licensed & Insured | 25+ Years
{{FOOTER_TEXT}}         → © 2026 Joe's Plumbing LLC. All rights reserved.
```

## Template Requirements

- **Single file** — `index.html` per template (inline CSS, no external deps)
- **Mobile-responsive** — must look good on phone screens
- **No JavaScript frameworks** — vanilla HTML/CSS only (inline or `<style>` block)
- **Keep it under 8KB** — smaller = faster generation, lower token cost
- **Test with real plumber data** — does it look good with "Joe's Plumbing, Salt Lake City, UT 84101" filled in?

## What Makes a Good Template?

- **Hero section** — big headline, phone number, emergency badge, CTA button
- **Services grid** — 6-8 common plumbing services with icons/emojis
- **Trust signals** — license number, years in business, review stars, insured badge
- **Contact section** — phone (tap-to-call on mobile), address, hours
- **Reviews** — 3 real-feeling testimonials
- **Footer** — license, city/state, copyright

## Directory Structure

```
templates/
├── modern/       → Clean, white-space, contemporary
├── bold/         → Dark, high-contrast, aggressive CTA
├── minimal/      → Simple, fast-loading, essential info only
├── hero/         → Big background image, emotional hook
└── trust/        → Review-heavy, certification badges, authority-focused
```

## Usage

Templates get cloned to the VPS and the generation script (`generate_sites.py`) reads them,
swaps placeholders with lead data from the pipeline database, and outputs complete sites.
