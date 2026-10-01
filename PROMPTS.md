# AI Prompt Log

## Prompt 1 — Full Codebase Audit

- Tool: [Antigravity]
- Type: code
- Prompt:

> [You are working on the MeroxIO Web Developer Assessment: “Rescue the Mistvale tea store”.

IMPORTANT: This is a hiring assessment. Follow the provided README.md and BRAND.md as the source of truth. Do not guess requirements or invent business facts.

FIRST, DO NOT MODIFY index.html.

Your first job is to understand the entire assessment and audit the existing project.

Read completely:

- README.md
- BRAND.md
- index.html
- all relevant existing image/assets and their usage

Understand all:

- functional requirements
- business rules R1–R8
- design/brand requirements
- accessibility requirements
- responsive requirements
- SEO/structured-data requirements
- performance requirements
- image requirements
- prohibited libraries/techniques
- API constraints
- submission requirements

CORE IMPLEMENTATION CONSTRAINTS:

1. Keep the project as a single HTML file.
2. Keep CSS and JavaScript inside index.html.
3. Do not migrate the project to React, Next.js, Vite, Tailwind, Bootstrap, jQuery, or another framework/library.
4. Do not add unnecessary dependencies.
5. Do not rewrite working code merely for style or personal preference.
6. Preserve existing functionality unless the README requires changing it or it is necessary to fix a bug.
7. Make the smallest reasonable code changes required to satisfy the assessment.
8. Do not modify the provided PRODUCTS data unless the README explicitly permits/requires it.
9. Do not modify the provided API implementation between the API START and API END markers.
10. Do not invent product information, reviews, ratings, awards, statistics, claims, or business rules.
11. Preserve the required legal text exactly.
12. Do not remove required existing content simply because you personally prefer a different design.

AUDIT TASK:

Inspect the current code and create a structured audit covering:

A. Functional bugs

- cart
- quantity controls
- stock limits
- sold-out products
- remove/clear behavior
- cart count
- price calculations
- coupon
- shipping
- search
- filtering
- sorting
- API interactions
- pincode handling
- checkout
- newsletter
- quick view/modal behavior
- any other interactive functionality

B. Business-rule violations

Check every R1–R8 requirement from README.md individually.

C. UI/UX problems

- navigation
- product discovery
- product cards
- CTA clarity
- cart experience
- checkout flow
- empty/error states
- mobile usability
- responsive behavior
- visual hierarchy
- unnecessary visual effects

D. Accessibility

Check:

- semantic HTML
- heading hierarchy
- labels
- buttons
- keyboard navigation
- focus states
- alt text
- ARIA usage where genuinely necessary
- color contrast
- dialogs/modals
- form errors

E. SEO

Check:

- title
- meta description
- canonical
- Open Graph
- Twitter metadata
- structured data
- Product data
- FAQ data
- Organization/OnlineStore data
- single H1 requirement

F. Performance

Check:

- image sizes
- unnecessary requests
- unnecessary JavaScript
- layout issues
- external dependencies
- loading behavior

G. Brand compliance

Compare the current UI against every relevant requirement in BRAND.md.

For every identified issue, record:

- Issue
- Location in code
- Why it is a problem
- Related README/BRAND requirement
- Severity: Critical / High / Medium / Low
- Minimal recommended fix

IMPORTANT:

Do not immediately fix anything.

Do not rewrite index.html.

Do not generate a replacement index.html.

Do not make cosmetic changes yet.

I will maintain the assessment NOTES.md myself based on the actual work and testing.

Do not create, modify, or invent NOTES.md content.

Do not create or modify PROMPTS.md.

Do not fabricate any assessment documentation or previous prompt history.

TESTING:

After the code audit, create a practical baseline testing checklist based on README.md.

Separate:

1. Code-level issues you can identify from inspection.
2. Issues that must be manually verified in the browser.
3. Edge cases that need testing.

Do not claim something was tested if you have not actually tested it.

FINAL OUTPUT OF THIS TASK:

At the end, report:

1. Complete assessment requirements understood.
2. Complete prioritized bug list.
3. Business-rule violations.
4. UI/UX issues.
5. Accessibility issues.
6. SEO issues.
7. Performance issues.
8. Brand violations.
9. Browser/manual tests I need to perform.
10. Recommended implementation order.

MOST IMPORTANT:

DO NOT MODIFY index.html DURING THIS AUDIT.

Wait for my approval before implementing fixes.

Throughout the assessment, prefer minimal, targeted changes over unnecessary rewrites.

Every future change must have a reason tied to the README, BRAND.md, a discovered bug, accessibility, UX, performance, or another concrete assessment requirement.

I have also manually tested the current website in the browser.

My initial observations are:

NAVIGATION

- The Home navbar link does not appear to perform useful navigation.
- The Shop navbar link does not appear to perform useful navigation.
- The About navbar link does not appear to perform useful navigation.
- The Contact navbar link does not appear to perform useful navigation.
- The "Shop Now" button in the hero does correctly take me to the tea/product section.

SEARCH

- The search bar does not appear to work correctly.

CART

- Add to Cart does nothing.
- The cart icon does not update after trying to add a product.
- Clicking the cart icon also fails.
- Adding the same product multiple times does not work because the cart functionality is currently failing.
- Sold-out product behavior needs to be verified against the README/business rules after the cart initialization issue is understood.

QUICK VIEW

- Quick View can fail when clicking product images.

SORTING/FILTERING

- Category controls are visible.
- The sort dropdown is visible.
- Low-to-high and high-to-low sorting do not appear to work accurately.
- Sorting and filtering should be verified in combination with search.

PRODUCT CARDS

- Product cards have an awkward dashed border.
- Product card/CTA hover behavior causes visible layout resizing/jumping.
- The current product images are technically visible, but they look like simple placeholder-style graphics and do not present the tea products professionally.

RESPONSIVE/UI

- The current desktop design is visually inconsistent with a professional premium tea brand.
- The page does not appear responsive/professional on smaller screens.
- The overall visual hierarchy and spacing need improvement.

PINCODE

- I tested pincode 282007.
- The website displayed: "Sorry, we do not deliver to 282007."
- Verify this behavior against the provided API and README requirements. Do not assume it is a bug.

BROWSER CONSOLE ERRORS

During my manual testing I observed:

1. updateCount:
   Uncaught TypeError: Cannot read properties of null (reading 'length')

2. addToCart:
   Uncaught TypeError: Cannot read properties of null (reading 'find')

3. renderCart:
   Uncaught TypeError: Cannot read properties of null (reading 'length')

4. openQuickView:
   Uncaught TypeError: Cannot read properties of undefined (reading 'image')

Treat these as manual observations to VERIFY against the source code, not as assumptions.

For each observation:

1. Inspect the relevant code.
2. Determine the actual cause if identifiable.
3. Mark whether it is confirmed by code, requires further browser testing, or is primarily a design/UX issue.
4. Do not fix it yet.

Also identify any important bugs from the README requirements that I have not manually discovered yet.

Do not modify index.html during this audit.]

- Outcome: accepted
- Why: The AI completed the requested audit without modifying index.html and verified the manually observed issues.