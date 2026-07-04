# Responsive Landing Page — Task 01 (Prodigy InfoTech Web Dev Internship)

This is my submission for Task 01 of the Prodigy InfoTech web development internship. The brief was to build a responsive landing page with an interactive navigation menu — one that stays fixed on screen, reacts when you scroll, and responds when you hover over the links.

## What it does

- The navbar is fixed to the top of the page across all sections.
- While you're at the top of the page, the navbar sits transparent over the hero section.
- Once you scroll past a certain point, it smoothly transitions into a solid dark background with a subtle shadow — makes it more readable once it's sitting over content instead of the hero.
- Hovering over any menu item changes its color and draws an underline under it.
- On smaller screens, the menu collapses into a hamburger icon that slides a mobile nav panel in from the right.

## Tech used

- **HTML** for the page structure (nav, hero, and three content sections)
- **CSS** (internal, inside a `<style>` tag) for styling, transitions, and the responsive/mobile layout
- **JavaScript** (internal, inside a `<script>` tag) for detecting scroll position and toggling the mobile menu

Everything lives in one file — no external `.css` or `.js` links, so it's fully self-contained and runs by just opening `index.html`.

## How it's built

The scroll detection is intentionally simple — just listening for the `scroll` event, checking `window.scrollY`, and toggling a `.scrolled` class on the navbar once it crosses ~60px. All the actual visual change (background, shadow, padding) happens in CSS through a transition on that class, so JS is only responsible for the on/off switch, not the animation itself.

The hover effect on nav links is pure CSS — an `::after` pseudo-element that grows from 0% to 100% width on `:hover`, instead of using a static underline.

## Files

responsive-landing-page/
└── index.html   (HTML + internal CSS + internal JS, all in one file)

## Running it locally

No build step, no dependencies, no separate files to keep track of. Clone the repo and open `index.html` directly in any browser.
