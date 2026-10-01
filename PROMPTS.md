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

## Prompt 3 — Navigation + Shopping UX Improvements

- Tool: [Antigravity]
- Type: code
- Prompt:

> [## Prompt 3 — Navigation + Shopping UX Improvements

Now improve the existing website's navigation and shopping UX based on the audit and the manual testing I completed after Prompt 2.

IMPORTANT:
- Work on the existing `index.html`.
- Make targeted, minimal changes.
- Do NOT rewrite the entire file.
- Preserve the existing `PRODUCTS` data exactly.
- Do not change the provided API START/END block.
- Do not add React, Next.js, Vite, Tailwind, Bootstrap, jQuery, or other frameworks/libraries.
- Keep the required single HTML file.
- Do not modify README.md or BRAND.md.
- Do not create or modify NOTES.md or PROMPTS.md.
- Do not fabricate product information, reviews, ratings, claims, or business data.
- Preserve all functionality already fixed in Prompt 2.
- Do not break cart, search, filtering, sorting, Quick View, coupon, stock, or pincode functionality.
- Do not start the full visual redesign yet. That will be handled in a later phase.

## 1. Navbar Navigation

The current navbar links for:

- Home
- Shop
- About
- Contact

do not provide useful navigation.

Fix them using the existing page sections/content.

Requirements:
- Home should take the user to the top/hero section.
- Shop should take the user to the tea/product section.
- About should take the user to the existing About section.
- Contact should take the user to the existing Contact section.
- Do not invent new content just to create navigation targets.
- Use appropriate semantic links/buttons where applicable.
- Make sure navigation works when clicked.
- Preserve the existing visual design for now as much as possible.

## 2. Add-to-Cart Feedback

During manual testing, Add to Cart works correctly, but there is no immediate visual confirmation.

Currently:
- The cart badge updates.
- The user has to scroll back to the navbar/cart icon to notice that the product was added.

Improve this UX.

When a product is successfully added:
- Show a small, professional success notification/toast near the user.
- Example meaning: "Darjeeling Tea added to cart."
- The message should be temporary and disappear automatically.
- It may include a small "View Cart" action if that fits the existing implementation.
- Do NOT use a browser `alert()` for successful Add to Cart.
- Do not make the notification block the page or require the user to close it.
- Do not cause the product card or page layout to jump.
- Make sure repeated Add to Cart actions do not create a broken stack of notifications.

For unsuccessful actions:
- Keep the existing useful feedback for sold-out products and quantity-limit errors.
- Do not replace useful validation messages with generic success messages.

## 3. Cart Access

Make sure the existing cart icon remains easy to use.

Verify:
- Clicking the cart icon opens the cart.
- Cart badge updates immediately after Add to Cart.
- Cart contents are visible without requiring a page refresh.
- Closing the cart works.
- Existing quantity/remove functionality remains intact.

Do not redesign the entire cart yet.

## 4. Product-to-Cart UX

After Add to Cart:
- The product should remain in its current position.
- Do not cause the product grid to jump.
- Do not change product prices or product data.
- Do not remove the existing Add to Cart button unless the current implementation requires a state change.
- Preserve sold-out behavior.

## 5. Navigation + Product Section Testing

After implementing the changes, test:

1. Click Home.
2. Click Shop.
3. Click About.
4. Click Contact.
5. Add an available product to cart.
6. Confirm the success feedback appears.
7. Click View Cart if implemented.
8. Confirm the cart opens correctly.
9. Close the cart.
10. Add another product.
11. Confirm the cart badge updates.
12. Test the maximum quantity message.
13. Test a sold-out product.
14. Refresh the page and confirm the cart still works.

## 6. Accessibility for These Changes

For the navigation and new notification:
- Use semantic HTML where appropriate.
- Do not remove visible focus indicators.
- Make interactive elements keyboard accessible.
- If the toast uses an accessibility announcement mechanism, use an appropriate ARIA live region without overusing ARIA.
- Do not perform the full accessibility overhaul in this phase.

## 7. Regression Check

The following Prompt 2 functionality must continue working:

- Add to Cart
- Cart persistence
- Quantity controls
- Remove item
- Search
- Category filtering
- Price sorting
- Combined search + filter + sort
- Quick View
- Sold-out restriction
- Maximum quantity restriction
- Coupon logic
- Pincode handling

Do not change their underlying business rules unless a bug is discovered that directly prevents this Prompt 3 work.

## Scope Boundary

Do NOT implement these yet:

- Full visual redesign
- New product images
- Full responsive redesign
- Complete accessibility overhaul
- SEO/JSON-LD
- Performance optimization
- Image optimization
- Trust Strip
- FAQ redesign/addition
- Newsletter redesign
- Typography overhaul
- Major CSS architecture changes

Those will be handled in later phases.

## Before finishing

Run a syntax check and inspect the browser console for new JavaScript errors.

Then report:

1. Files changed
2. Navigation changes
3. Add-to-Cart feedback changes
4. Cart UX changes
5. Accessibility changes made in this phase
6. Tests performed
7. Any console errors
8. Any remaining issues
9. Confirm that Prompt 2 functionality was not broken
10. Concise summary of exactly what changed

Do not modify anything outside this scope.]

- Outcome: accepted
- Why: The AI implemented the requested navigation and shopping UX improvements. Navbar links now navigate to the existing page sections, Add to Cart provides immediate toast feedback with a View Cart action, and cart/accessibility behavior was improved. Prompt 2 functionality remained intact and browser testing reported zero JavaScript errors.