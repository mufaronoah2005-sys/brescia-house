# Brescia House School redesign

A zero-dependency static website with nine public routes and a custom error page. Run `npm run build`, `npm run check`, then `npm start` (http://127.0.0.1:4173).

## Editing
- Shared layout and page generation: build.mjs
- Theme and responsive layout: dist/style.css (tracked source, preserved by build)
- Audience resources and missing-content placeholders: content/audiences.json (editable; build preserves it)
- Authentic school assets: dist/assets; their source paths are in source-home.html
- Baseline and migration limitations: AUDIT.md

The content model is ready for migration into a school-selected CMS, but this delivery does not provide an authenticated CMS/admin panel. No portal URLs, fees, policies, staff, testimonials or examination results have been fabricated. Admissions and tour calls to action lead to the existing school-owned services; this site does not collect application or child data. Parent portal and teacher resources remain explicit placeholders pending confirmation. New editorial headlines are based on the school's published educational ethos; they are not represented as quotations.

## Deployment
Private review deployment through Sites. This does not modify brescia.co.za. Before replacing the official website, connect the chosen CMS, confirm all school content, map old routes and redirects, and validate the existing admissions systems with the school. The original server implementation and its private infrastructure were not available for audit.
