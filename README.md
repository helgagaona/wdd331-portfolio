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
├── index.html                         # Portfolio home page
├── css/                               # Portfolio CSS modules
│   ├── main.css                       # Imports modules in cascade layers
│   ├── base/                          # Reset and element styles
│   ├── components/                    # Cards, buttons, forms, and navigation
│   ├── layout/                        # Page layout
│   ├── tokens/                        # Colors and design variables
│   └── utilities/                     # Utility classes
src                                     # Source folder with all pages
├── unit-1/
│   └── custom-properties/             # Unit 1 page and stylesheet
└── unit-2/
    ├── layered-components/             # Layered components exercise
    ├── tailwind/                       # Tailwind CSS demo and source stylesheet
    │   ├── input.css                   # Tailwind input stylesheet
    │   └── styles.css                  # Generated stylesheet
    └── postcss-demo/                   # Standalone PostCSS demo
        ├── css/                        # Demo stylesheet modules
        ├── dist/styles.css             # Generated demo stylesheet
        ├── images/                     # Demo images
        ├── package.json                # Demo build scripts and dependencies
        └── postcss.config.js           # PostCSS plugin configuration
```

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
- [Custom Properties and Nesting](unit-1/custom-properties/index.html)
- [Layered Components](unit-2/layered-components/index.html)
- [Tailwind CSS](unit-2/tailwind/index.html)
- [PostCSS Demo](unit-2/postcss-demo/index.html)
