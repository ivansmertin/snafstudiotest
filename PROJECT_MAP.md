# Project Map

## Current file tree
```text
.
├── index.html
├── styles.css
└── images/
    ├── heart-icon.svg
    ├── ivan.png
    ├── logo.svg
    ├── tg.svg
    ├── vk.svg
    └── wave.svg
```

## File responsibilities
- `index.html` — Entire page markup, all semantic sections, and inline JavaScript behavior.
- `styles.css` — Global design tokens, layout, components, animations, and responsive rules.
- `images/logo.svg` — Brand logo used in header/footer.
- `images/ivan.png` — Author portrait in “Обо мне”.
- `images/heart-icon.svg` — Decorative icon in quote/stat card.
- `images/wave.svg` — Decorative wave background asset.
- `images/vk.svg`, `images/tg.svg` — Social icon assets (not all social icons are asset-backed; some are inline SVG/text).

## Key page sections in `index.html`
1. **Sticky header** (`#top`) with logo, desktop nav, mobile burger menu, contacts, and social links.
2. **Hero / Services** (`#services`) with value proposition and primary CTA.
3. **About / Author** (`#about`) with portrait and stats cards/counters.
4. **Benefits / Value** (`#value`) with horizontal carousel and progress indicator.
5. **FAQ** (`#faq`) accordion-style questions/answers plus bottom CTA block.
6. **Footer** with contacts, legal links placeholders, social links, and copyright.

## Inline JavaScript behavior map (in `index.html`)
- Header offset sync for anchor scrolling.
- Mobile burger menu open/close state and body scroll lock.
- Nav highlight pill + hover/focus/current state handling.
- Scrollspy via IntersectionObserver.
- Reveal/stagger animations + animated counters.
- Benefits carousel controls and progress bar sync.
- FAQ accordion with ARIA state + animated panel heights.

## Style zones in `styles.css`
- `:root` design tokens (colors, radii, shadows, motion vars, header offset).
- Base/reset rules (`*`, `html`, `body`, `img`, `.container`).
- Shared UI (`.btn`, `.surface-glow`, common patterns).
- Header/navigation/mobile menu.
- Hero section.
- Author/stats section.
- Benefits carousel section.
- FAQ + CTA block.
- Footer.
- Reveal animation utilities.
- Responsive breakpoints (`max-width: 1100px`, `768px`, `560px`) + reduced-motion adjustments.

## Asset inventory (`images/`)
- Total assets: 6
- Formats: SVG (5), PNG (1)
- Usage profile: branding, portrait, decorative icons/background accents, social marks.

## Likely future extraction targets (documentation only)
- Potential JS extraction target: `scripts/main.js` (or similar single file first).
- Potential CSS extraction structure: `styles/base.css`, `styles/layout.css`, `styles/components.css`, `styles/sections/*.css`, then optional bundle step **only if explicitly approved**.
- For now, keep current monolithic files as source of truth.
