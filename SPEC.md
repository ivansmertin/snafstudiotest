# Current-State Specification

## Project summary
This repository contains a single-page static website for **SNAF STUDIO** (Russian-language marketing/personal studio landing page) focused on design, frontend implementation, and launch support.

## Current architecture summary
- **HTML:** One document (`index.html`) containing all page sections and an inline `<script>` for interactivity.
- **CSS:** One monolithic stylesheet (`styles.css`) with variables, shared UI, section styles, animation rules, and responsive breakpoints.
- **Assets:** Local SVG/PNG files under `images/` referenced directly from HTML/CSS.
- **Runtime model:** Client-side only, no backend or build pipeline observed.

## Important constraints
- Existing visual appearance and interaction behavior should be treated as baseline.
- Section IDs are used for anchor navigation and scrollspy; changing them is high risk.
- JavaScript currently depends on specific class names and DOM structure.
- CSS is centralized; selector edits can have broad impact.

## Deployment assumptions (observed/probable)
- Observed: all paths are relative and static-host friendly.
- Probable inference: intended deployment is a simple static host (e.g., GitHub Pages / Nginx static root / CDN bucket) with no compilation step.

## Known current files
- `index.html`
- `styles.css`
- `images/logo.svg`
- `images/ivan.png`
- `images/heart-icon.svg`
- `images/wave.svg`
- `images/vk.svg`
- `images/tg.svg`

## Current frontend stack
- Semantic HTML5
- Vanilla CSS (custom properties, media queries, transitions/animations)
- Vanilla JavaScript (inline in `index.html`) using DOM APIs and IntersectionObserver
- Google Fonts (`Montserrat`) via external stylesheet link

## Likely future refactor goals
- Extract inline JavaScript from `index.html` into a dedicated script file while preserving behavior.
- Split `styles.css` into logical modules (base/layout/components/sections/responsive) without changing output.
- Improve maintainability/testability of interactive logic (menu, scrollspy, reveal, carousel, FAQ).

## Known risks
- **High risk:** changing class names/IDs used by JS handlers.
- **High risk:** modifying sticky header offset logic and anchor scroll behavior.
- **Medium risk:** adjusting carousel width/gap logic can break controls/progress calculations.
- **Medium risk:** FAQ open/close animation depends on runtime height measurement.
- **Medium risk:** reveal/counter behavior depends on IntersectionObserver thresholds and reduced-motion handling.
