# CLAUDE.md

Static one-page portfolio, hosted on GitHub Pages.

## Stack
- No build step, no frameworks, no npm packages.
- Only `index.html`, `style.css`, and small vanilla JS.

## Direction (redesign, October 2026)
- Inspired by Daniel Tan's "Unifiers of Japan" Dribbble shot: two colours (crimson + cream), a framed page with thin side rules and tiny rotated margin labels, condensed heavy uppercase display type, red bands for showpieces, cream bands for reading, notched frames, numbered "+" rows.
- Hero: Urdu name above a giant name, with an original animated cartoon (inline SVG) standing over the letters. The cartoon was requested by Hassaan; it can be swapped for one drawn from his photo.
- Only real content otherwise: no invented client logos, testimonials or stats.
- Work happens on the `redesign` branch.

## Theming
- Light only: red and cream for everyone. No dark mode.
- Change colors by updating the tokens at the top of `style.css`. Never hard-code hex colors in component rules (the favicon and `theme-color` meta are the only exceptions).
- `--red` for display type, fills and rules; `--red-deep` for running text on cream; cream text on red. `--ink`, `--blush`, `--red-soft`, `--white` are for the cartoon only.

## Typography
- Display: Archivo (Google Fonts variable), weight 800–900, `font-stretch` 62–85% (condensed), uppercase.
- Body: Instrument Sans.
- Urdu name: Noto Naskh Arabic 700.

## LINKS object
- Never remove or rename the `LINKS` object at the bottom of `index.html`.
- Never remove the logic that hides buttons whose URL isn't set.

## Animations
- Use Motion's vanilla JS version from the jsDelivr CDN (`animate`, `inView`, `stagger`).
- Sections fade in and rise 20px on scroll.
- Card grids stagger by 0.08s.
- Durations 0.3–0.6s. Nothing bouncy.
- Exceptions, all in the hero cartoon: a blink every 5.5s, icons floating 8px over 6s, and pupils following the mouse (fine pointers only). All off under reduced motion.
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
