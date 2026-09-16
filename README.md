# TRL Digital Services

**TRL — The Right Lifestyle.** A digital services platform focused on AI, automation, websites, digital systems and practical business solutions.

Live site: <https://therightlifestyle.github.io/TRL-DIGITAL-SERVICES/>

---

## What TRL Does

TRL helps individuals and businesses design, build, automate and improve digital workflows and customer-facing systems.

Core areas:

- **AI & Automation** — automation systems, AI agents and chatbots, workflow and CRM automation, email/SMS sequences
- **Business Systems** — appointment booking, workflow analysis, reporting dashboards, custom integrations
- **Websites & Digital Experiences** — website development, branding and graphic design, SEO and social setup
- **Digital Support** — content and social automation, lead capture and follow-up systems
- **Custom Solutions** — scoped per business, built around the tools a client already uses
- **Learning & Digital Services** — tutoring, mentorship, AI tools training, freelance task work

## Current Product

This repository is the **service-delivery layer** of the broader TRL ecosystem. It is the public site through which
prospective clients discover what TRL offers and start a conversation.

Visitors can:

1. Explore the service catalog (filterable, with per-service detail views)
2. Review starting-at pricing and tier structure
3. Build a quote in the estimate wizard, which composes a pre-filled WhatsApp request
4. Read how TRL works, what the engagement standards are, and the FAQ
5. Contact TRL directly through WhatsApp, email or Instagram

The website itself does not store, transmit or process any client data. Quotes are handed off to a conversation.

## Positioning

> We don't sell tools. We build systems that give you your time back.

## TRL Vision

TRL is building a broader operating system for ambitious people where goals, business, AI, education, knowledge,
community and execution converge into one ecosystem. The ecosystem applications shown on the site
(TRL SaaS, Academy, AI Labs, Community, Marketplace, Ventures) are presented with their current build status,
and are developed separately from this repository.

This repository represents the **Digital Services layer** of that vision.

## Technology

Nothing here is aspirational — this is what the project actually uses:

| Concern | Implementation |
| --- | --- |
| Markup | Single semantic HTML5 document (`index.html`) |
| Styling | Hand-written CSS in one `<style>` block, custom properties for theming |
| Behaviour | Vanilla ES6 JavaScript, no framework, no build step |
| Icons | Inline SVG |
| Fonts | WOFF2 webfonts embedded as base64 `@font-face` (Inter, Montserrat, Oswald, Great Vibes) |
| Data | A static `SERVICES` array in the script; the catalog, modal and estimate wizard render from it |
| External calls | None for content or analytics. Outbound links go to `wa.me`, `mailto:`, Instagram and the TRL site |

The site is intentionally a single self-contained file: no package manager, no bundler, no external requests,
no cookies, no tracking.

## Project Structure

```
TRL-DIGITAL-SERVICES/
├── index.html   # Complete site: markup, CSS, data and JS in one self-contained document
└── README.md    # This file
```

`index.html` is organised in this order: `<head>` metadata, embedded fonts, CSS, then the page sections —
hero, marquee, about, values, services, service modal, pricing, process, why TRL, ecosystem, story, roadmap,
standards, FAQ, estimate wizard, contact, footer — followed by the data engine and interaction script.

## Development

No installation or build is required.

```bash
git clone https://github.com/therightlifestyle/TRL-DIGITAL-SERVICES.git
cd TRL-DIGITAL-SERVICES
python3 -m http.server 8080      # then open http://localhost:8080/
```

Opening `index.html` directly in a browser also works.

Editing guidance:

- Service names, descriptions, features and starting-at tier prices all live in the `SERVICES` array. Adding an
  entry there adds a catalog card, a modal, a filter result and a wizard option automatically.
- `WA` at the top of the script holds the contact number used to build every `wa.me` deep link.
- Colours, radii and the type scale are defined as CSS custom properties at the top of the stylesheet.
- Keep the file free of external asset references — that is what makes it portable across static hosts.

## Deployment

Hosted on **GitHub Pages**, published from the `main` branch at the repository root (classic/legacy Pages build).
There is no workflow file and no deploy command: pushing to `main` publishes the site.

```
https://therightlifestyle.github.io/TRL-DIGITAL-SERVICES/
```

Because every asset is inline, the repository root can be served by any static host without path changes.

## Quality Standards

This project follows these principles:

- No fabricated metrics — no invented service counts, uptime claims, commitment percentages or scale figures
- No fake testimonials, ratings or invented client results
- No secrets, tokens or private data committed to the repository
- Mobile-first usability: fluid type and layout widths, breakpoints at 460px, 700px and 1060px
- Accessible, semantic markup: landmarks, labelled controls, keyboard-operable interactive elements
- Maintainable code: one file, no dependencies, no build pipeline
- Clear user journey: services → pricing → quote → conversation
- Production-oriented implementation, not a prototype

## Status

The site is **live and complete** for the service lines described on it. It is a static presentation and quote-request
layer: there is no account system, no CMS and no backend. Quoting and booking are handled through WhatsApp handoff.
Ecosystem applications referenced on the page carry their real status labels (in development, building, planned).

## Contact

- **WhatsApp:** +92 319 0091457
- **Email:** officialtrlservice@gmail.com
- **Instagram:** [@the.right.lifestyle](https://instagram.com/the.right.lifestyle)
- **TRL:** <https://therightlifestyle.github.io/TRL-1/>

---

*Automate the routine. Accelerate your legacy.*
