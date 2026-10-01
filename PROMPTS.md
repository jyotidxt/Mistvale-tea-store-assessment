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

## Prompt 2 — Core Functional Fixes

- Tool: [Antigravity]
- Type: code
- Prompt:

> [## Prompt 2 — Core Functional Fixes

Now implement only the core functional fixes identified during the audit.

IMPORTANT:
- Work on the existing `index.html`.
- Do NOT rewrite the entire file.
- Do NOT rebuild the application from scratch.
- Make the smallest targeted changes necessary.
- Preserve the existing PRODUCTS data exactly.
- Do not change the provided API START/END block.
- Do not add React, Next.js, Vite, Tailwind, Bootstrap, jQuery, or other frameworks/libraries.
- Keep this as the required single HTML file.
- Do not change BRAND.md or README.md.
- Do not create or modify NOTES.md or PROMPTS.md.
- Do not fabricate data, product information, reviews, ratings, claims, or business rules.
- Do not make visual redesign changes in this phase unless a tiny UI change is strictly required for the functionality to work.
- Do not change working functionality unnecessarily.

### 1. Cart Initialization

Fix the cart state so a fresh user with no existing `mv_cart` in localStorage gets an empty cart instead of `null`.

The cart must:
- initialize safely
- persist correctly in localStorage
- render correctly when empty
- update the cart count without JavaScript errors

### 2. Add to Cart

Fix `addToCart()`.

Verify that:
- an available product can be added
- adding the same product again increases quantity instead of creating an incorrect duplicate
- product quantity respects the existing stock/business rules
- sold-out products cannot be added
- cart state persists after refresh
- cart count updates correctly

Do not invent new stock rules. Follow the rules already specified in README.md/BRAND.md and identified in the audit.

### 3. Cart Drawer / Cart Rendering

Fix `renderCart()` and the cart-opening behavior.

Verify:
- cart opens without errors
- empty cart state renders correctly
- product image/name/price/quantity render correctly
- subtotal updates correctly
- quantity changes update the UI
- removing one item removes only that intended item
- cart closes correctly
- no `null`/`undefined` JavaScript errors occur

### 4. Quantity Handling

Fix quantity logic so quantities remain numeric.

Verify:
- incrementing 1 → 2 → 3 works numerically
- decrementing works correctly
- quantity cannot go below the intended minimum
- quantity cannot exceed the applicable product limit/stock
- UI and localStorage remain synchronized

### 5. Product ID Consistency

Fix inconsistent product ID comparisons/types where required.

Use one consistent approach so:
- product lookup works
- cart lookup works
- quantity updates work
- remove-item works
- Quick View can correctly identify a product

Do not alter the actual product IDs in the PRODUCTS data.

### 6. Search

Fix the existing product search logic.

Search should correctly match the intended product information already available in the product data.

Verify:
- matching products appear
- non-matching products are hidden
- clearing the search restores the products
- search works together with the existing category filtering
- search results have an appropriate empty state when nothing matches

Do not add fake products or fake search data.

### 7. Sorting

Fix the existing price sorting logic.

Verify:
- Low → High actually sorts prices numerically ascending
- High → Low actually sorts prices numerically descending
- the existing/default ordering remains unchanged when no price sort is selected
- sorting works together with search and category filtering

Do not modify product prices.

### 8. Quick View

Fix the Quick View product reference/closure issue identified in the audit.

Verify:
- clicking any product's Quick View opens the correct product
- the correct product image is shown
- the correct product information is shown
- there are no `undefined` product/image errors
- closing Quick View works normally

### 9. Combined Filtering Logic

After fixing the individual functions, verify that these work together:

Search + Category Filter + Price Sort

Example:
1. Select a category.
2. Search for a product.
3. Apply Low → High.
4. Confirm only matching products remain and they are correctly sorted.

Then test other combinations.

### 10. JavaScript Error Check

After implementation, test the affected functionality and check the browser console.

The following baseline errors must no longer occur:

- `updateCount()` — Cannot read properties of null (reading 'length')
- `addToCart()` — Cannot read properties of null (reading 'find')
- `renderCart()` — Cannot read properties of null (reading 'length')
- `openQuickView()` — Cannot read properties of undefined (reading 'image')

Also check for any new JavaScript errors introduced by your changes.

### Scope Boundary

Do NOT implement these yet:
- full visual redesign
- new product images
- typography redesign
- responsive redesign
- SEO/JSON-LD work
- accessibility overhaul
- navigation redesign
- newsletter redesign
- Trust Strip
- FAQ
- performance/image optimization
- pincode/API changes
- checkout redesign

Those will be handled in separate phases.

### Before finishing

Review your changes against the existing README.md and BRAND.md.

Then provide:

1. Files changed
2. Functions/sections changed
3. What functional bugs were fixed
4. Any business-rule decisions made
5. Tests performed
6. Console errors before vs after
7. Any remaining functional issues
8. A concise summary of exactly what you changed

Do not modify anything outside this scope.]

- Outcome: accepted
- Why: The AI implemented the requested core functional fixes in `index.html`, including cart initialization, Add to Cart, quantity handling, search, sorting, Quick View, combined filtering, and pincode error handling. I manually verified the main shopping flows and found them working.

