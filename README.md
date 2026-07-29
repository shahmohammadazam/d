# Research Portfolio

A single-page academic portfolio site — about, research highlights, publications, ongoing projects, and contact — built as one self-contained HTML file and published with GitHub Pages.

> **Status:** this is still the unedited template. Every name, publication, and figure on the page is placeholder text.

## Live site

https://shahmohammadazam.github.io/d/DOCTYPE.html

Note that the repository root (`/d/`) currently returns 404, because GitHub Pages serves `index.html` at a directory root and this repository's page is named `DOCTYPE.html`. Renaming the file to `index.html` would make the short URL work.

## What's in here

| Path | Purpose |
| --- | --- |
| `DOCTYPE.html` | The entire site — markup, styles, and scripts in one file |
| `.github/workflows/static.yml` | Deploys the repository to GitHub Pages on every push to `main` |

There is no build step and no dependencies to install. [Tailwind CSS](https://tailwindcss.com) and the Inter font are loaded from CDNs at page load.

## Editing the page

Open `DOCTYPE.html` in a browser to preview it, and in any editor to change it. Placeholders are marked with `CUSTOMIZE` comments:

```html
<!-- CUSTOMIZE: Replace with your name -->
<div class="text-2xl font-bold text-gray-800">Your Name</div>
```

Searching the file for `CUSTOMIZE` will walk you through every spot that needs your details. Beyond those, the things most worth changing:

- **Title and name** — the `<title>` tag, the nav, the hero heading, and the footer copyright each carry the placeholder name separately.
- **Accent colours** — the hero gradient is the `.gradient-bg` rule in the `<style>` block; the rest of the palette comes from Tailwind utility classes such as `text-blue-600`.
- **Interactive buttons** — Download CV, View All Publications, LinkedIn, ORCID, the per-paper buttons, and the contact form are all wired to `alert()` placeholders in the `<script>` block at the bottom. Each alert names what should replace it.

The contact form is a demo: it intercepts the submit event and shows an alert rather than sending anything. Wiring it to a service such as Formspree or Netlify Forms would make it functional.

## Deploying

Pushing to `main` triggers the workflow in `.github/workflows/static.yml`, which uploads the whole repository as a Pages artifact and deploys it. No manual step is needed. The workflow can also be run by hand from the repository's **Actions** tab.
