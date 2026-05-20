# DAMARIS ALUM · PORTFOLIO

A hand-crafted editorial portfolio for **Damaris Alum** — UX Researcher, UI Designer, QA Tester and Full Stack Developer. Built from scratch in vanilla HTML, CSS and JavaScript with no frameworks and no templates. The site showcases six live deployed applications, a signature burgundy and gold brand system, an in-page brand guide modal, and a featured MyLocalDressmaker case study with an inline slide carousel and rich-media modal.

The site is fully responsive, accessible to WCAG 2.1 AA, and ships with a light and dark theme, keyboard-first navigation, ARIA scroll-spy, focus-visible states, reduced-motion respect and lazy-loaded media.

Primary audience: hiring managers, agency leads and product teams looking for a UX practitioner who can run research, design accessible interfaces, write the production code and test it end-to-end.

<p align="center">
  <a href="https://alumsdesigns.github.io/damaris-portfolio/">
    <img src="https://img.shields.io/badge/▶%20%20VIEW%20LIVE%20PORTFOLIO%20%20↗-bc0000?style=for-the-badge&labelColor=8a0000&logoColor=white" height="56" alt="View Live Portfolio">
  </a>
  &nbsp;&nbsp;
  <a href="https://www.linkedin.com/in/damaris-alum/">
    <img src="https://img.shields.io/badge/💬%20%20BOOK%20INTRO%20CHAT%20%20↗-0a3020?style=for-the-badge&labelColor=062320&logoColor=white" height="56" alt="Book Intro Chat">
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com/Alumsdesigns/damaris-portfolio">
    <img src="https://img.shields.io/badge/⌥%20%20VIEW%20CODE%20%20↗-0d0d0d?style=for-the-badge&labelColor=000000&logo=github&logoColor=white" height="56" alt="View Code">
  </a>
</p>

<p align="center">
  <sub>↑ Live site · LinkedIn intro chat · Source code on GitHub</sub>
</p>

---

# Contents
1. [User Experience (UX)](#1-user-experience-ux)
    - [User Stories](#user-stories)
        - [Visitors & Recruiters](#visitors--recruiters)
        - [Site Owner](#site-owner)
2. [Features](#2-features)
    - [Current Features](#current-features)
    - [Future Features](#features-which-could-be-implemented-in-the-future)
3. [Design](#3-design)
4. [Technologies Used](#4-technologies-used)
5. [Testing](#5-testing)
6. [Deployment and Local Development](#6-deployment-and-local-development)
7. [Credits](#7-credits)

---

# 1. User Experience (UX)

## User Stories

### Visitors & Recruiters
As a hiring manager, recruiter or prospective collaborator visiting the portfolio:
- I want to immediately understand who Damaris is and what roles she fits, so I can decide in seconds whether to keep reading.
- I want to see availability, location and remote preferences up-front, so I don't waste time on a candidate who isn't open to my role.
- I want proof of shipped work — live URLs, GitHub code links and case studies — so I can verify the claims rather than just trust the copy.
- I want a clear picture of research methodology, testing rigour and accessibility practice, because those are hard to fake.
- I want to read recommendations from real clients and colleagues, so I can triangulate the self-description against independent voices.
- I want to download or view a CV in one click, so I can share it internally with my team.
- I want a contact path that doesn't require a form (LinkedIn, email), so I can reach out in the channel I prefer.
- I want the site itself to demonstrate accessibility and craft, because a portfolio that fails its own audit fails the interview.

### Site Owner
As Damaris (the site owner):
- I want the portfolio to read as a single editorial artefact, so it signals craft and intent rather than a generic template.
- I want every project card to tell a complete story — role, stack, methodology, outcomes — so recruiters don't have to ask basic questions.
- I want a brand guide modal that documents the palette, typography, voice and process, so visitors can see the system, not just the surface.
- I want the MyLocalDressmaker case study to be a featured, full-width artefact with playable walkthroughs, so the work speaks for itself.
- I want a recommendations carousel with real photos and full quotes, so social proof is human, not anonymous.
- I want WCAG AA compliance and keyboard-first navigation throughout, because accessibility is a qualifier for every role I want.
- I want light and dark theme support with persistent contrast pairings, so the site looks intentional in either mode.
- I want the source code to be public on GitHub, so the build itself is part of the case study.

---

# 2. Features

## Current Features

The portfolio is a single-page editorial site with seven distinct sections (Hero, About, Live Work, Skills, UX Principles, Recommendations, Contact), a sticky nav with scroll-spy, two in-page modals (brand guide and MyLocalDressmaker slide viewer), and a recommendations carousel.

### Sticky navigation with scroll-spy
A persistent top nav with anchor links to every section. The current section's link is auto-marked with `aria-current="page"` via an IntersectionObserver, giving screen-reader users live position feedback. A theme-toggle button with `aria-pressed` flips between light and dark mode.

### Hero with animated role typewriter and brand monogram
The hero introduces Damaris by name with an animated `aria-live` role typewriter cycling through "UX Researcher", "QA Tester", "Software Tester", "UX/UI Designer" and "Full Stack Developer". A bespoke SVG monogram disk anchors the right column with a circular `RESEARCH · DESIGN · TEST · DEVELOP · TEST · SHIP · TEST · SMILE` cadence stamp set on a `<textPath>` arc. Hero stats render as a 7-tile grid covering live apps, test sessions, years of experience, Google UX certificates, the Code Institute diploma (St Mary's University, Scotland), cyber projects and the Phase Innovate "Tech Women to Watch" recognition.

### About section with skills matrix
A side-by-side layout pairs a four-paragraph bio (with a `Currently learning` badge for Playwright and AI testing) against a seven-row skills grid covering Research, Design & Prototyping, QA Testing, Development, Communication, Collaboration and AI Build & Tools.

### Live Work, seven project cards with filter chips
A filter bar (`All / QA Tester / ML & Data / Full Stack / Front End / CLI & Python`) toggles the visibility of seven `ux-card` articles. Each card carries a per-card `--card-accent` CSS variable so hover/focus borders inherit the card's signature colour. Cards include:
- **QuipOrder · NHS** (Django / PostgreSQL, signed NDA, demo on request)
- **DavinaLeilaniBlooms** (real client, HTML/CSS/JS, live site + GitHub)
- **Quizverse** (a11y-first JS quiz, 92–100 Lighthouse, live game + GitHub)
- **Standup Updates** (Python CLI, two-persona UX, live Heroku demo + GitHub)
- **Damaris Alum Portfolio** (this site, with a `Brand guide` button that opens a luxe in-page modal)
- **Phase Innovate** (double-wide card, ongoing UX research for a non-profit)
- **Environmental Risk Prediction** (double-wide ML card with embedded 100% / 0.59 / 3 / 457 mini-stat tiles)
- **MyLocalDressmaker** (full-width featured case study with inline hero carousel, eight-slide modal, moodboard flip tiles, typography spec and Ghana-inspired palette)

### Brand guide modal
Triggered from the portfolio card's `Brand guide` button. A six-section luxe burgundy/gold dialog covers **Essence**, **Palette** ("A wardrobe, not a palette" — seven swatches including the theme-aware Label Accent token), **Typography**, **Interactive elements** (light + dark mode CTA pairs with contrast ratios), **Voice & Tone** and an eight-beat **Process Signatures** cadence. ESC closes, click-outside closes, focus is trapped on the close button and restored to the trigger on dismissal.

### MyLocalDressmaker slide modal + flip moodboard
The featured case study has an inline arrow-controlled hero carousel showing eight slides (mixed images and walkthrough videos), a thumbnail strip beneath, and a `Read the full story` CTA that opens a full-width slide modal with rich narrative copy per slide. Below the carousel, a nine-tile moodboard has flip-to-back cards revealing discovery notes, and a typography section documents Asul + Roboto with the project's brand colour swatches.

### Skills section
A sixteen-block grid covering Manual Testing, Security Testing, UX Research Methods, Analysis & Synthesis, Design, Design Tools, Engineering & DevOps, Development, Data & ML, Cloud & Infrastructure, AI Tools, Project Delivery, Accessibility, Information Security, Methodology and a `Currently Learning` block.

### UX Principles section
Six principle cards covering user-centred design, accessibility, evidence-led iteration, cognitive load reduction, privacy by design and consistency — each paired with an `In practice` line tying the principle back to a shipped project.

### Recommendations carousel
A horizontal-scroll carousel with three full recommendation cards (Evelyn Nomayo, Martha Taylor, Aqua Ofosuhene) including photos, role context and multi-paragraph quotes. Burgundy pagination dots, prev/next arrow controls, keyboard arrow nav and centre-snap scroll behaviour.

### Theme toggle
A light and dark theme with persisted contrast pairings across hero, monogram, skill blocks, cards and the brand modal. A `prefers-reduced-motion` media query disables shimmer, pulse and stagger reveals for users who request reduced motion.

### Accessibility features
- Skip-link to main content (WCAG 2.4.1)
- Semantic landmarks (`<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- ARIA roles, labels and `aria-pressed` / `aria-selected` / `aria-current` state on every interactive control
- Visible focus rings via `:focus-visible`
- All decorative SVG marked `aria-hidden="true"`
- All informative images carry descriptive `alt` text; lazy-loaded
- All ratio-locked colour pairings tested for WCAG 2.1 AA contrast
- Keyboard-first navigation across nav, filter bar, carousels and modals

---

## Features which could be implemented in the future

- **Playwright end-to-end test suite** — currently learning Playwright; the portfolio is the natural first target for a documented automation pass.
- **Lighthouse CI** — wire performance/a11y/SEO/best-practice budgets into a GitHub Action so regressions fail the build.
- **Per-card brand guides** — the portfolio card already opens a brand guide modal; the pattern can be templated for the Standup Updates (CLI/dev tone), Quizverse (a11y-forward tone), Environmental Risk Prediction (data-credible tone) and Phase Innovate (community/mission tone) cards.
- **Phase Innovate proposed brand system** — a separate card and modal offering a one-page brand audit and proposed system as a leave-behind for the non-profit.
- **Case-study deep-dive pages** — promote each NDA-cleared project from card to dedicated `/case-studies/...` page with research artefacts, test plans and outcome metrics.

---

# 3. Design

## Structure
The portfolio is a single-page application with seven sections, a fixed top nav and two overlay modals. The layout uses CSS Grid for the hero, About and Live Work sections and Flexbox for navigation, filter bar, tag rows and carousels.

## Brand identity
Hand-mixed signature palette built around heritage, craft and trust:
- **Burgundy `#6D1B28`** — heritage anchor, used for accents, dots, dividers and modal section eyebrows
- **Gold `#C5A021`** — signature highlight, used sparingly for the `Currently learning` badge, italic display text and the SMILE process pill
- **Teal `#2A9D8F`** — default interactive trust colour, links and the project-card default accent
- **Deep Teal `#1A6B5E`** — dark-mode CTA fill, paired with cream text for 6.2:1 contrast (WCAG AA)
- **Cream `#FBF9F6`** — canvas/background tint
- **Charcoal `#0d0d0d`** — typographic anchor, body text and dark-mode surfaces
- **Label Accent** (semantic token `--label-accent`) — theme-aware accent carrying small uppercase eyebrows (`.skill-cat`, `.skill-block-title`, `.role-word`, `.cv-role`, `.cv-skill-label`). Resolves to burgundy `#6D1B28` in light mode and mint `#5fc7b8` in dark mode, both ≥6:1 against their surfaces.

Each project card additionally carries a unique `--card-accent` CSS custom property (set inline per card) so hover/focus borders inherit the card's own header gradient — for example QuipOrder uses `#2a4a7a`, Quizverse uses `#3a6e6e`, the portfolio card uses the brand `#bc0000`.

## Typography
Three-tier type system loaded from Google Fonts:
- **Fraunces** (serif, weights 300/500, italic) — display, hero name, section titles
- **DM Sans** (sans, weights 300/400/500) — UI, body copy, navigation
- **Asul** (alt serif, weights 400/700) — atelier accent used in the MyLocalDressmaker case study to honour the original brand
- **Roboto** — case-study body fallback paired with Asul

Fallbacks: system serif and sans-serif stacks if Google Fonts fails.

## Imagery
All decorative SVG is generated inline. Project card thumbnails use CSS linear-gradient banners with overlaid type. Moodboard, slide and recommendation photography is lazy-loaded from `/myLocalDressMaker/` and `/recommendation_images/`.

## Icons
Decorative pictographs use Unicode glyphs (`✓ ◉ ◇ ⟨⟩ ⚡ ♿ 🔄 🧩 🔒 📐 ▶ ⌥ ↗ ✦`) rather than an external icon library, to keep the dependency surface zero.

---

# 4. Technologies Used

- **HTML5** — semantic markup, landmarks, ARIA, native `<dialog>`-pattern modals
- **CSS3** — Grid, Flexbox, custom properties, `@keyframes`, `prefers-reduced-motion`, light/dark theming via `[data-theme]`
- **JavaScript (vanilla)** — IntersectionObserver scroll-spy, role typewriter, theme toggle, filter chips, recommendations carousel, MLD hero + modal carousel, brand modal, magnetic hover on hero buttons
- **SVG** — bespoke monogram with circular `<textPath>` cadence stamp, gradients, glow layers
- **Google Fonts** — Fraunces, DM Sans, Asul, Roboto
- **Git** — version control
- **GitHub** — repository hosting
- **GitHub Pages** — static site deployment
- **VS Code** — development environment
- **[Claude Code](https://claude.com/claude-code)** (Anthropic) — AI pair-programming CLI used throughout for code edits, accessibility checks, semantic HTML review and brand-system iteration
- **Chrome DevTools / Firefox DevTools / Safari DevTools** — cross-browser testing and debugging
- **Lighthouse** — performance, accessibility, SEO and best-practice audits
- **WAVE / axe DevTools** — accessibility auditing
- **W3C HTML Validator** — markup validation
- **W3C CSS Validator** — CSS validation

---

# 5. Testing

This project underwent thorough testing to ensure functionality, responsiveness, accessibility and adherence to web standards across browsers and devices.

### Validators Used
- **W3C HTML Validator** — used to check the structural integrity and validity of the HTML markup across `index.html`, `cvs.html` and `damaris-cv.html`.
- **W3C CSS Validator** — used to validate the `styles.css` and `cvs.css` syntax and compliance with web standards.
- **Lighthouse (Chrome DevTools)** — performance, accessibility, SEO and best-practice audits across desktop and mobile breakpoints.

### Browser Compatibility
The site's rendering and functionality were verified across the following browsers:
- **Google Chrome** (latest) — primary development browser, full DevTools profiling
- **Mozilla Firefox** (latest) — cross-browser layout and a11y verification
- **Apple Safari** (latest, macOS) — WebKit rendering, native font fallback behaviour
- **Mobile Safari** (iOS) — touch interactions, swipe gestures, viewport scaling

### Accessibility Testing
- **Keyboard-only navigation pass** — every interactive control (nav, filter chips, carousel, modals, theme toggle, moodboard flip tiles) reachable and operable without a mouse.
- **Screen reader spot-checks** — VoiceOver on macOS verified that `aria-current`, `aria-pressed`, `aria-live` and `aria-label` announce correctly.
- **Contrast audit** — every text-over-background pairing in light and dark mode verified against WCAG 2.1 AA (4.5:1 for body, 3:1 for large text). Small uppercase eyebrows routed through a dedicated `--label-accent` token to meet AA in both themes; CV light-mode teal text raised from `--teal` (2.9:1) to `--teal-mid` (6.5:1).
- **Reduced-motion** — verified that `prefers-reduced-motion: reduce` disables stagger reveals, shimmer sweeps, pulse rings and hero glow drift.

### Manual User Testing Table

| ID  | Test Label                  | Steps                                                                                  | Expected Outcome                                                          |
|-----|-----------------------------|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| T01 | Nav scroll-spy              | Scroll through every section, watch the nav links                                      | Current section's link auto-marks with `aria-current="page"`              |
| T02 | Theme toggle                | Click the theme button                                                                 | Theme flips light↔dark, `aria-pressed` updates, contrast preserved        |
| T03 | Role typewriter             | Wait on the hero                                                                       | Roles cycle smoothly, `aria-live` polite                                  |
| T04 | Filter chips                | Click each filter on the Live Work section                                             | Only cards matching the data-cat remain visible; `aria-selected` updates  |
| T05 | Project card hover/focus    | Hover or tab to each project card                                                      | Border inherits the card's `--card-accent` colour                         |
| T06 | Brand guide modal           | Click `✦ Brand guide` on the portfolio card                                            | Modal opens, ESC closes, click backdrop closes, focus returns to trigger  |
| T07 | MLD hero carousel           | Click ‹ / › arrows on the MyLocalDressmaker hero                                       | Slides advance with counter update; touch swipe also advances on mobile   |
| T08 | MLD slide modal             | Click `Read the full story` or any thumbnail                                           | Modal opens at the correct slide; arrow keys + nav buttons step through   |
| T09 | Moodboard flip tiles        | Click any moodboard tile                                                               | Tile flips to reveal discovery note; `aria-pressed` toggles               |
| T10 | Recommendations carousel    | Click prev/next arrows, pagination dots, or use arrow keys when track has focus        | Cards centre-snap, active dot updates                                     |
| T11 | Responsiveness · Desktop    | View site at ≥1280px                                                                   | Hero, About and Live Work use multi-column grid; all content visible      |
| T12 | Responsiveness · Tablet     | View site at 768–1024px                                                                | Cards re-stack, monogram and stats reflow, nav links remain visible       |
| T13 | Responsiveness · Mobile     | View site at ≤480px                                                                    | Single-column layout, touch swipe on MLD carousel, no horizontal overflow |
| T14 | Skip link                   | Tab once on page load                                                                  | "Skip to main content" focusable link appears, jumps to `#main-content`   |
| T15 | Reduced motion              | Set OS to `Reduce motion`, reload                                                      | Stagger reveals, shimmer and glow drift disabled; all content still usable|

### Browsers and devices verified
- macOS Safari, Chrome, Firefox
- iOS Safari (iPhone)
- Android Chrome (Pixel)

---

# 6. Deployment and Local Development

The site is deployed to **GitHub Pages** from the `main` branch of the repository.

### Live URL
[https://alumsdesigns.github.io/damaris-portfolio/](https://alumsdesigns.github.io/damaris-portfolio/)

### How this site was deployed
1. In the GitHub repository, navigate to the **Settings** tab, then choose **Pages** from the left-hand menu.
2. From the **Source** section drop-down, select the **`main`** branch and the **`/ (root)`** folder.
3. Once selected, the page refreshes with a ribbon confirming successful deployment.
4. Any changes pushed to `main` will redeploy automatically.

### How to clone the repository
1. Go to the [damaris-portfolio GitHub repository](https://github.com/Alumsdesigns/damaris-portfolio).
2. Click the green **Code** button, choose **HTTPS** and copy the URL.
3. Open a terminal and navigate to the directory where you want the cloned folder to live.
4. Run `git clone https://github.com/Alumsdesigns/damaris-portfolio.git` and press Enter.

### How to run locally
The site has no build step. Open `index.html` directly in a browser, or for live-reload during development:
```bash
# VS Code Live Server extension (right-click index.html → Open with Live Server)
# or
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

# 7. Credits

## Code
- Built by **Damaris Alum** with **[Claude Code](https://claude.com/claude-code)** (Anthropic's official CLI for Claude) as an AI pair-programmer. Every design decision, accessibility choice, brand direction, copy line and architectural call was driven by Damaris — Claude Code executed the edits, generated CSS scaffolding from spoken intent, and helped maintain WCAG and semantic-HTML rigour across iterations.
- No frameworks, no UI libraries, no templates. Vanilla HTML, CSS and JavaScript end-to-end.
- This README itself was drafted by Claude Code from the live source, then reviewed and approved by Damaris.

## Content
- All copy, project narratives, case-study text, brand guide voice and recommendation framing written by **Damaris Alum**.
- Recommendation quotes used with permission from Evelyn Nomayo (Phase Innovate), Martha Taylor (JLR) and Aqua Ofosuhene (MyLocalDressmaker).

## Typography
- **Fraunces**, **DM Sans**, **Asul** and **Roboto** sourced from [Google Fonts](https://fonts.google.com/).

## Icons
- Decorative pictographs use Unicode glyphs only — no external icon library.

## Media
- Project thumbnails, brand monogram, hero glow and all decorative SVG generated inline.
- MyLocalDressmaker slide imagery and moodboard tiles courtesy of client **Aqua Ofosuhene**, used with permission.
- Recommendation portrait photos provided by the individuals named, used with permission.

## Acknowledgements
- **Evelyn Nomayo** and the **Phase Innovate** team for the ongoing real-world UX research practice that anchors this portfolio.
- **Martha Taylor** at JLR for the cross-team QA mentorship referenced in the recommendations section.
- **Aqua Ofosuhene** at MyLocalDressmaker for trusting the end-to-end brand and Shopify build.
- **Code Institute** and **St Mary's University, Scotland** for the Diploma in Full Stack Software Development with Predictive Analytics.
- **Anthropic** for [Claude Code](https://claude.com/claude-code) and Claude Opus 4.7, the AI pair-programming tools used throughout this build.
- **Google UX Design Certificate** programme for the seven-certificate research and design grounding.
