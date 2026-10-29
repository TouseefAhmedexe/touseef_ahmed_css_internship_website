# Internship Website

A complete responsive internship website built with HTML and CSS only.
Task 10 of my Bloomrix internship. No JavaScript is used.

## Files
- index.html - the page
- style.css - all the styling
- images/ - hero photos and profile photo

## CSS Architecture & Sub-Layering
The stylesheet is structured into cascade layers and component sub-layers:
`reset`, `base`, `layout`, `components` (`header`, `hero`, `cards`, `table`, `widgets`, `form`, `faq`, `footer`), `utilities`, `overrides`, `print`.
Class names strictly adhere to BEM (`block__element--modifier`).

## Design Tokens
Colors, spacing, font sizes, font weights, line heights, radii, shadows, z-indexes, and layout widths are custom properties in `:root`.

## Responsive Strategy
Mobile-first layout using breakpoints at `40rem` (640px), `48rem` (768px), and `64rem` (1024px). Card grids auto-fit cleanly across device viewports.

## Accessibility & ARIA
- Fixed skip-link revealed at top of viewport on key focus.
- Table headers configured with `scope="col"`.
- Progress bar built with `role="progressbar"` and `aria-valuenow="90"`.
- Native `:user-invalid` styling with visible error spans across all form controls (select, date, file, checkbox).
- `rel="noopener noreferrer"` applied to all external links.

## Performance Optimization
Keyframe animations (e.g. `@keyframes bar-grow`) exclusively use hardware-accelerated transforms (`transform: scaleX()`) and opacity for zero layout reflows.

## How to Run
Open index.html with Live Server in Visual Studio Code or in any modern web browser.