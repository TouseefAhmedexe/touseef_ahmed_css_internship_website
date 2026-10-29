# Internship Website

A complete responsive internship website built with HTML and CSS only.
Task 10 of my Bloomrix internship. No JavaScript is used.

## Files
- index.html - the page
- style.css - all the styling
- images/ - hero photos and profile photo

## CSS architecture
The stylesheet is split into cascade layers, in this order:
reset, base, layout, components, utilities, overrides, print.
Class names follow BEM: block, block__element, block--modifier. Selectors are kept to one class
where possible. The only longer selectors are the table cells, the form states and the active
navigation link.

## Design tokens
Colors, spacing, font sizes, radii, shadows and layout widths are custom properties in :root.
Dark mode only swaps the color values. It follows the device setting (prefers-color-scheme).

## Responsive strategy
Mobile-first. Breakpoints in rem: 40rem (640px), 48rem (768px) and 64rem (1024px).
- 40rem: the footer gets two columns.
- 48rem: the header and the hero become rows, and the About section gets two columns.
- 64rem: the header becomes sticky, the contact section gets two columns, and the footer gets four.
The card grids use repeat(auto-fit, minmax()), so they change their columns without a media query.

## Layout
- Flexbox: header, navigation list, hero buttons, badges, card header, tag list, form buttons.
- Grid: hero, About, card grids, roadmap, form, footer.

## Container query
Each assignment card sits in a container. When the card is 26rem or wider, its header places the
title and the badge on one row. The window width does not decide this. The number of columns does.

## Accessibility
- A skip link for keyboard users.
- :focus-visible outlines on links, buttons, fields and summaries.
- Every field has a visible label. Required, invalid, valid and disabled states use more than color.
- Status badges have text, a symbol and a border style.
- Animations and transitions are turned off with prefers-reduced-motion.
- Text and borders were checked for contrast in DevTools.

## Print
Navigation, hero buttons and photo, and the contact form are hidden. Backgrounds are removed,
cards avoid page breaks, and the address of each external link is printed after its text.

## Performance
Only transform and opacity are animated, shadows are small, and there are no filters.
Unused rules were checked with the DevTools Coverage tool.

## Tested
Mobile 375px, tablet 768px and desktop 1280px, plus the print preview, dark mode and
reduced motion in the DevTools Rendering panel.

## How to run
Open index.html with Live Server in Visual Studio Code, or in any web browser.