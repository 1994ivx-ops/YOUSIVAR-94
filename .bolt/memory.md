# Project memory

## Product intent & audience

- YOUSIVAR–Ω product showcase — a premium single-file `index.html` landing/promotional page
- Showcase repository only; separate from the main application repository
- Developer: Yousef Z. A. Shaheen; audience: users interested in the Android AI app
- Tagline: “YOUSIVAR–Ω — Beyond Intelligence. Beyond Limits.”
- Bilingual content: Arabic (primary, RTL) and English (LTR UI labels)

## Brand personality & voice

- Sophisticated, editorial, developer-centric
- Silver accents, refined typography, premium feel
- Factual only; no fabricated stats, awards, certifications, partnerships, or release claims
- Planned capabilities must be clearly marked, not presented as shipped

## Visual design & UX direction

- Single-file `index.html` with all CSS and JS embedded; no React/Vite/build pipeline for core
- CSS custom properties, semantic HTML5, modular JS functions
- Mobile-first responsive: 968px and 600px breakpoints; no horizontal overflow
- Separate RTL/LTR containers for Arabic vs. English content; no global RTL
- Silver/omega (Ω) motif; graceful fallback for brand image (Ω on error)
- Animations via transforms/opacity only; pause when tab hidden; respect `prefers-reduced-motion`
- Touch-friendly buttons, keyboard nav, visible focus, safe-area spacing, accessible icon labels
- Centralized `CONFIG` object for all external URLs and toggleable assets

## Decisions, constraints & rationale

- Four CTAs: download APK (null → “coming soon”), source code (opens repo), support (null → “coming soon”), docs/licensing (repo URL, configurable)
- Repository: `https://github.com/Yousef-Shaheen-1/-.git`
- 11 social links + 2 email contacts preserved exactly; icon+label UI, no raw URLs visible; `noopener noreferrer`
- Local chat preview runs fully in-browser, no backend/API calls
- Feature explorer: 6 categories with availability status; roadmap: 4 columns (Available, In Development, Planned, Requires Configuration)
- Video: placeholder shown; activates only when `CONFIG.videoUrl` set
- No secrets/API keys; no untrusted HTML injection; validate configurable destinations
- Icon-only buttons must have accessible labels; external icon library failure must not break social directory

## Open questions & assumptions

- Threads URL may contain an invisible/invalid character — needs correction rather than guessing
- APK, support, docs, and video URLs are not yet provided and remain configurable placeholders
- No actual security audit performed; must not claim otherwise
- Deployment target: static hosting (e.g., GitHub Pages); no server-side processing required