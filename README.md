# WDD 331R Portfolio

**Student:** Helga Gaona
**Semester:** Fall 2026
**Live Site:** [View Site](https://helgagaona.github.io/wdd331-portfolio/)

## About

This repository is my portfolio for WDD 331R: Advanced CSS.
Each week I add new pages and styles as I work through the course
assignments. The site deploys automatically to GitHub Pages on
every push to main.

## Project Structure
```
├── README.md
├── index.html
├── package.json
├── package-lock.json
├── postcss.config.js
├── dist/
│   └── styles.css
├── css/
│   ├── main.css
│   ├── base/
│   │   ├── elements.css
│   │   └── reset.css
│   ├── components/
│   │   ├── buttons.css
│   │   ├── cards.css
│   │   ├── effects.css
│   │   ├── forms.css
│   │   ├── nav.css
│   │   └── units.css
│   ├── js/
│   │   └── theme-preference.js
│   ├── layout/
│   │   └── primary.css
│   ├── tokens/
│   │   ├── colors.css
│   │   └── variables.css
│   └── utilities/
│       └── utilities.css
├── fonts/
│   ├── OFL.txt
│   └── RobotoFlex-VF.ttf
├── public/
│   └── files/
│       ├── U1 - Nested & Custom Properties - Helga Gaona.pdf
│       ├── U1 - Portfolio.pdf
│       ├── U2 - Build.pdf
│       ├── U2 - Layered Components.pdf
│       └── large-image.avif
└── src/
    ├── unit-1/
    │   ├── unit-1.html
    │   └── custom-properties/
    │       ├── index.html
    │       └── styles.css
    ├── unit-2/
    │   ├── unit-2.html
    │   ├── layered-components/
    │   │   ├── index.html
    │   │   └── css/
    │   │       ├── main.css
    │   │       ├── base/
    │   │       │   ├── elements.css
    │   │       │   └── reset.css
    │   │       ├── components/
    │   │       │   ├── buttons.css
    │   │       │   ├── cards.css
    │   │       │   ├── forms.css
    │   │       │   ├── nav.css
    │   │       │   └── temples.css
    │   │       ├── layout/
    │   │       │   └── primary.css
    │   │       ├── tokens/
    │   │       │   ├── colors.css
    │   │       │   └── variables.css
    │   │       └── utilities/
    │   │           └── utilities.css
    │   ├── part-and-slotted/
    │   │   └── index.html
    │   ├── postcss-demo/
    │   │   ├── index.html
    │   │   ├── .gitignore
    │   │   ├── package.json
    │   │   ├── package-lock.json
    │   │   ├── postcss.config.js
    │   │   ├── dist/styles.css
    │   │   ├── images/
    │   │   │   ├── salt-lake-temple.webp
    │   │   │   └── washington-dc-temple.webp
    │   │   └── css/
    │   │       ├── main.css
    │   │       ├── base/
    │   │       │   ├── elements.css
    │   │       │   └── reset.css
    │   │       ├── components/
    │   │       │   └── card.css
    │   │       ├── layout/
    │   │       │   ├── chrome.css
    │   │       │   └── primary.css
    │   │       ├── tokens/
    │   │       │   ├── colors.css
    │   │       │   └── variables.css
    │   │       └── utilities/
    │   │           └── utilities.css
    │   └── tailwind/
    │       ├── index.html
    │       ├── input.css
    │       ├── styles.css
    │       └── tailwind-demo/
    │           ├── dist/output.css
    │           └── src/
    │               ├── index.html
    │               └── input.css
    ├── unit-3/
    │   ├── unit-3.html
    │   ├── oklch/
    │   │   ├── index.html
    │   │   └── styles.css
    │   ├── relative-color-syntax/
    │   │   ├── relative-color-demo.html
    │   │   └── relative-color-demo.css
    │   ├── shape-outside/
    │   │   ├── index.html
    │   │   ├── shape-outside-demo.html
    │   │   └── Teaching Video Report - shape outside.pdf
    │   └── visual-effects/
    │       └── index.html
    ├── unit-4/
    │   ├── unit-4.html
    │   ├── advanced/
    │   │   ├── container-demo.html
    │   │   ├── container-demo.css
    │   │   ├── sticky-demo.html
    │   │   └── sticky-demo.css
    │   ├── anchoring/
    │   │   ├── index.html
    │   │   └── styles.css
    │   ├── grid-layouts/
    │   │   ├── cards.html
    │   │   ├── cards.css
    │   │   ├── editorial.html
    │   │   └── editorial.css
    │   └── intrinsic-sizing/
    │       ├── intrinsic-sizing-demo.html
    │       ├── intrinsic-sizing-demo-real.html
    │       ├── intrinsic-sizing-demo-final.html
    │       ├── intrinsic-sizing-demo-final-final.html
    │       ├── intrinsic-sizing-demo-helga.html
    │       └── teachinv video report intrinsitc.pdf
    └── unit-5/
        ├── index.html
        ├── resume.html
        ├── resume.css
        ├── variable-font-axes.html
        ├── variable-font-axes.css
        └── form-controls.html
```

## Typography

Typography tokens live in `css/tokens/variables.css`, including the numbered
fluid type scale and semantic body, caption, and heading sizes and line heights.
Primary `h1` headings use Lobster as an accent; other headings use DM Sans.
Both fonts load from Google Fonts with `display=swap`; heading and body tokens
include cursive and system sans-serif fallback stacks.
The variable-font demo self-hosts Roboto Flex in `fonts/` and uses its variable
weight, width, and slant axes; its font license is included alongside the file.

## Build

The PostCSS setup is located in `unit-2/postcss-demo/`. It bundles CSS
`@import`s with `postcss-import`, adds vendor prefixes with Autoprefixer, and
minifies the output with cssnano. It processes
`unit-2/postcss-demo/css/main.css` into
`unit-2/postcss-demo/dist/styles.css`.

From the repository root, install the demo's dependencies and build its CSS:

```sh
cd unit-2/postcss-demo
npm ci
npm run build
```

To rebuild the demo stylesheet automatically while editing its CSS, run
`npm run watch` from `unit-2/postcss-demo/`.

## Tailwind CSS

Tailwind CSS 4 and its CLI are installed in the root project. From the
repository root, build the demo stylesheet with:

```sh
npm run tailwind:build
```

To rebuild it automatically while editing the Tailwind demo, run
`npm run tailwind:watch`. The generated stylesheet is
`src/unit-2/tailwind/styles.css`.

## Pages

- [Home](index.html)
- [Unit 1 Overview](src/unit-1/unit-1.html)
- [Custom Properties and Nesting](src/unit-1/custom-properties/index.html)
- [Unit 2 Overview](src/unit-2/unit-2.html)
- [Layered Components](src/unit-2/layered-components/index.html)
- [Part and Slotted](src/unit-2/part-and-slotted/index.html)
- [Tailwind CSS](src/unit-2/tailwind/index.html)
- [PostCSS Demo](src/unit-2/postcss-demo/index.html)
- [Unit 3 Overview](src/unit-3/unit-3.html)
- [OKLCH](src/unit-3/oklch/index.html)
- [Relative Color Syntax](src/unit-3/relative-color-syntax/relative-color-demo.html)
- [Shape Outside](src/unit-3/shape-outside/shape-outside-demo.html)
- [Visual Effects](src/unit-3/visual-effects/index.html)
- [Unit 4 Overview](src/unit-4/unit-4.html)
- [Anchor Positioning](src/unit-4/anchoring/index.html)
- [Editorial Layout](src/unit-4/grid-layouts/editorial.html)
- [Responsive Card Grid](src/unit-4/grid-layouts/cards.html)
- [Container Query Demo](src/unit-4/advanced/container-demo.html)
- [Sticky Section Headers](src/unit-4/advanced/sticky-demo.html)
- [Intrinsic Sizing](src/unit-4/intrinsic-sizing/intrinsic-sizing-demo-final-final.html)
- [Unit 5: Variable Font Axes](src/unit-5/index.html)
- [Variable Font Axes Demo](src/unit-5/variable-font-axes.html)
- [Form Control Styling Demo](src/unit-5/form-controls.html)
- [Resume](src/unit-5/resume.html) — includes print styles in [resume.css](src/unit-5/resume.css) and a styled contact form.
