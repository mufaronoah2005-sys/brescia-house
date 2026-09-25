# Audit and migration plan — 25 September 2026

The supplied workspace was empty. No source implementation was removed. This audit distinguishes public observations from private systems that cannot be inspected without the original repository and access.

## Existing public site
- Public route inventory: /, /about, /history, /our-patron-saint, /about/ursuline-catholic-ethos, /global-education-programme, /admissions, /tuition-fees-2, /tuition-fees, /how-to-apply, /phases, /brescia-bears, /foundation-phase, /intermediate-phase, /high-school, /parents, /news-events, /news, /term_calendar, /alumnae, /donation, /lets-tour, /book-a-school-tour, /contact, /privacy-policy and dated news/calendar routes.
- Framework/backend/CMS: public HTML contains bundled modern/legacy JavaScript and Imager-style asset URLs. These are insufficient to verify the server framework, database schema, APIs, authentication or CMS implementation.
- Forms: school tour collects parent contact details and child name; applications link to external ScadCo services. Keep these established services rather than inventing a submission backend.
- Assets: authentic public school logo, campus, classroom and sport photographs are available. Source URLs retained in source-home.html.
- Dependencies: public page loads jQuery 3.5.1, Popper 1.16.0, Bootstrap 4.5.0, app and legacy bundles. Exact package tree/security advisory applicability cannot be audited without lockfiles. New build does not need these dependencies.
- SEO: existing canonical points at /__home__; stylesheet reference appears three times. New routes get distinct titles/descriptions and canonical URLs.
- Accessibility: repeated H1 elements, lazy images initially replaced by SVG placeholders, dropdown links with button roles require interaction testing. New implementation uses one H1, semantic links, focus styles, native disclosure, skip link and explicit dimensions.
- Performance: video hero, legacy bundles and third-party JavaScript increase resource requests; no measured Web Vitals claim is made. New build uses static HTML, small progressive JS, responsive compressed photos and no tracking.
- Links: empty Bears footer href, generic google.com coordinate link, and src='.' observed. Replace with meaningful destinations. Whole-site external link validation is not a guarantee of third-party availability.
- Mobile, console errors, runtime security and duplicated source components: cannot establish a complete baseline from HTML alone. No authenticated/private/student records accessed.

## Migration
1. Preserve audit evidence; verify authoritative content and existing application/tour destinations.
2. Generate shared static layouts and independently addressable pages from one content model.
3. Build homepage, audience pathways, admissions and contact; preserve links to existing services.
4. Provide explicit missing-content states for unverified portal/teacher resources; centralized CMS-importable content file. A production CMS and authentication require an approved integration; do not simulate them.
5. Check generated internal links, responsive layout, interaction and assets; privately deploy redesign for review. School production domain remains unchanged.
