# CLAUDE.md

Static one-page portfolio, hosted on GitHub Pages.

## Stack
- No build step, no frameworks, no npm packages.
- Only `index.html`, `style.css`, and small vanilla JS.

## Direction (redesign, October 2026)
- Inspired by a bold dark portfolio: giant heavy uppercase display type, a visual overlapping the headline, a screenshot marquee, big numerals, stacked project cards.
- Only real content: no invented client logos, testimonials, avatars or stats.
- The redesign happens on the `redesign` branch, one section at a time. Sections still waiting keep the old styling (marked in `style.css`).

## Theming
- Dark first; light mode follows `prefers-color-scheme: light` and `data-theme="light"`.
- Change colors by updating the tokens at the top of `style.css`. Never create a parallel theme or hard-code hex colors in component rules.
- Accent is a violet → pink gradient (`--gradient`, from `--accent` and `--accent-2`); use `--accent-ink` for accent-coloured text.

## Typography
- Display: Archivo (Google Fonts variable, weight 800–900, `font-stretch` ~112%), uppercase, tight tracking.
- Body: Instrument Sans.
- Instrument Serif is still loaded only for sections not yet redesigned; remove it once they're done.

## LINKS object
- Never remove or rename the `LINKS` object at the bottom of `index.html`.
- Never remove the logic that hides buttons whose URL isn't set.

## Animations
- Use Motion's vanilla JS version from the jsDelivr CDN (`animate`, `inView`, `stagger`).
- Sections fade in and rise 20px on scroll.
- Card grids stagger by 0.08s.
- Durations 0.3–0.6s. Nothing bouncy.
- Exception: the hero screenshot marquee is a slow CSS loop (60s), pauses on hover, and becomes a plain scroller under reduced motion.
- Always respect `prefers-reduced-motion`.

## Design system
- Lives in `design-system/hassaan/`.
- Read `design-system/hassaan/MASTER.md` before any UI work. Its "Project overrides" section wins over the generated rules below it.

## Images
- WebP only, always with `width`, `height` and `alt`.
- Lazy-load images below the fold.

## Responsive
- Mobile first.
- Check at 375px, 768px, 1024px and 1440px.

## Workflow
- Change one section at a time, then stop for review.
