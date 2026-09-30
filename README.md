# CSS Showcase

![MIT License](https://img.shields.io/badge/license-MIT-006d70)
![HTML5](https://img.shields.io/badge/HTML5-semantic-e34f26)
![CSS3](https://img.shields.io/badge/CSS3-modern-1572b6)
![Dependencies](https://img.shields.io/badge/dependencies-none-2b6a50)

**A bilingual, JavaScript-free portfolio of practical CSS techniques.** The default experience is US English; use the language controls in the sticky header to switch to Brazilian Portuguese. The switch is implemented with native radio inputs and CSS.

All project files live at the repository root; open `index.html` directly.

**GitHub Pages:** [Open the live project](https://roldan-eng-software.github.io/perfect-html-css-example/) (enable Pages to publish this URL).

**Screenshot:** _Add a screenshot of the finished page here._

## What this project demonstrates

- Semantic HTML, keyboard access, visible focus, reduced-motion support, and responsive layouts.
- Grid, Flexbox, container queries, scroll snap, and progressive scroll-driven effects.
- Design tokens, light/dark themes, modern color spaces, masks, and CSS animations.
- Native HTML interactions: `details`, anchor tabs, form validation, and the Popover API.
- Cascade layers, BEM naming, low-specificity selectors, and CSS-only language controls.

## How the CSS is organized

```text
css/
├── main.css                 # Imports and declares layer order
├── 00-settings/             # Tokens and theme behavior
├── 01-base/                 # Reset, typography, accessibility
├── 02-layout/               # Containers, grids, section rhythm
├── 03-components/           # Reusable controls and code samples
├── 04-utilities/            # Small composable helpers
└── 05-demos/                # One focused stylesheet per demo family
```

The complete file map is in [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md). The technique catalog is in [docs/CSS-TECHNIQUES.md](docs/CSS-TECHNIQUES.md).

## Technical decisions

- **Cascade layers:** `main.css` declares `settings`, `base`, `layout`, `components`, `demos`, and `utilities` in that order. Layer priority is intentional and more predictable than escalating selector specificity.
- **BEM:** component blocks and elements use names such as `.card`, `.card__title`, and `.card--featured`. IDs are reserved for document anchors and label relationships, never style selectors.
- **Zero JavaScript:** browser-native controls cover language selection, mobile navigation, disclosure, tabs, form validation, and popovers. This keeps the project dependency-free and directly inspectable.
- **Design tokens:** semantic custom properties separate meaning from palette values, so theme changes do not require rewriting component rules.
- **Progressive enhancement:** recent features are guarded where appropriate, with usable base styles or fallback values when unsupported.

## Browser compatibility

The baseline targets current evergreen browsers. Core layout, form controls, anchors, and disclosure remain useful without the newest effects. Support for native CSS nesting, `:has()`, `@container`, `@property`, OKLCH, `field-sizing`, Popover API, `@starting-style`, and scroll-driven timelines varies by browser and release.

Fallbacks include solid/linear colors before newer color functions, conventional sizing before `field-sizing`, a visible reveal sample when view timelines are unavailable, and page content that does not depend on animation. The page-wide theme preview uses `:has()`; browsers without it still get the system color preference. Cascade layers and native nesting are part of the baseline for current browsers; older browsers may omit those rules.

## Run locally

Open `index.html` directly in a browser. No installation or build step is required. For a local HTTP preview, run `npx serve .` from this directory; `npx` downloads the server package only if needed and is not a project dependency.

To publish, create a GitHub repository and enable Pages from the root of its default branch. Replace the Pages URL, screenshot placeholder, social links, and author details below.

## Quality checklist

- [x] No required runtime dependencies; the page opens from `index.html`.
- [x] No JavaScript files and no inline `style` attributes.
- [x] Keyboard-operable controls, associated form labels, focus indication, and reduced-motion rules.
- [x] Responsive sizing and mobile navigation without script.
- [ ] Run the final page through the W3C Nu HTML Checker and a CSS validator before publishing.
- [ ] Measure Lighthouse on the published Pages URL; 95+ is a target, not a verified score.
- [ ] Verify WCAG AA contrast in both themes with an automated contrast checker and manual review.

## About the author

- **Name:** [Your Name]
- **Brand:** Roldan Eng Software
- **Website:** [Add your website]
- **Email:** [Add a contact email]
- **GitHub:** [Add your GitHub profile]
- **LinkedIn:** [Add your LinkedIn profile]
