# Manual QA Checklist (Post-change)

Use this after each frontend patch to guard against regressions.

## 1) Global sanity
- [ ] Page loads without missing styles.
- [ ] No broken image links (check logo, portrait, icons, decorative graphics).
- [ ] Browser console has no errors.

## 2) Desktop layout (>= 769px)
- [ ] Sticky header stays visible on scroll and does not overlap content incorrectly.
- [ ] Navigation links highlight/active state behaves correctly while scrolling.
- [ ] Hero, About, Benefits, FAQ, Footer spacing and alignment look unchanged.

## 3) Mobile layout (< 769px)
- [ ] Burger button opens/closes menu.
- [ ] Menu open state locks body scroll and closes after nav link click.
- [ ] Mobile nav, contact info, and social links are readable and usable.

## 4) Navigation and anchors
- [ ] Header links scroll to correct sections (`#services`, `#about`, `#value`, `#faq`).
- [ ] Scroll offset is correct (section headings not hidden under sticky header).

## 5) CTA and links
- [ ] Primary CTA buttons work (Telegram, phone links).
- [ ] External links with new tabs still open correctly where expected.

## 6) Interactive components
- [ ] Reveal/scroll animations trigger correctly (or remain stable with reduced motion).
- [ ] Counter animation in stats section reaches expected values.
- [ ] Benefits carousel prev/next buttons scroll cards as expected.
- [ ] Carousel progress indicator updates while scrolling.
- [ ] FAQ accordion opens/closes correctly; ARIA-expanded behavior remains coherent.

## 7) Visual regression check
- [ ] Compare before/after quickly at desktop + mobile widths.
- [ ] No unintended typography/color/spacing/shadow changes.
- [ ] No clipping/overflow issues introduced.
