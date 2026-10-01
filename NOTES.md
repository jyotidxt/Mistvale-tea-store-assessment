# Mistvale Tea Store — Assessment Notes

## 1. Baseline Testing

I first opened and tested the original website before making any code changes.

## 2. Navigation

- Home navbar link does not perform useful navigation.
- Shop navbar link does not perform useful navigation.
- About navbar link does not perform useful navigation.
- Contact navbar link does not perform useful navigation.
- The Shop Now button in the hero correctly scrolls to the tea/product section.

## 3. Cart

- Add to Cart does nothing.
- The cart icon does not update after trying to add a product.
- Clicking the cart icon also fails.
- Adding the same product multiple times does not work because the cart is currently failing.
- Sold-out product behavior needs to be verified against the assessment requirements after the cart issue is understood.

## 4. Search

- Search does not work as expected.
- Search needs to be tested together with category filtering and sorting.

## 5. Filtering and Sorting

- Category buttons are visible.
- The sort dropdown is visible.
- Low-to-high and high-to-low price sorting do not appear to work accurately.
- Combined search, filtering and sorting need further testing.

## 6. Quick View

- Quick View can fail when clicking product images.

## 7. Product Card UI

- Product cards have an awkward dashed border.
- Hovering over product cards causes the card/CTA area to resize or jump.
- The current product images are visible but look like simple placeholder-style graphics.
- Product imagery does not present the tea products professionally.

## 8. Responsive Design

- The current page does not appear sufficiently responsive/professional on smaller screens.
- Mobile and tablet layouts need further testing.

## 9. Visual Design

- The current design does not look like a professional premium tea brand.
- Colors and visual effects are too strong/inconsistent.
- Some sections have too much empty space.
- Typography and visual hierarchy need improvement.

## 10. Pincode

- Tested pincode: 282007.
- Result shown: "Sorry, we do not deliver to 282007."
- This needs to be verified against the provided API and assessment requirements.

## 11. Browser Console Errors

During baseline testing, these errors were observed:

- `updateCount()` — Cannot read properties of null (reading 'length')
- `addToCart()` — Cannot read properties of null (reading 'find')
- `renderCart()` — Cannot read properties of null (reading 'length')
- `openQuickView()` — Cannot read properties of undefined (reading 'image')

These errors were observed before making any implementation changes.

## 12. Current Status

- Original website tested.
- Baseline issues recorded.
- No implementation changes made yet.
- Next step: complete the code audit against README.md and BRAND.md before making fixes.

## 13. Code Audit Results

The AI audit was performed after the initial manual browser testing. No code was changed during the audit.

### Confirmed Functional Issues

- Cart initializes as `null` when there is no existing cart in localStorage.
- Add to Cart therefore throws a JavaScript error.
- Cart count also throws a JavaScript error.
- Opening the cart throws a JavaScript error.
- Search filtering logic is incorrect.
- Quick View has an array/closure issue that can produce an undefined product.
- Price sorting uses an incorrect boolean comparison.
- Removing a cart item can remove more items than intended.
- Quantity increment can cause string concatenation instead of numeric addition.
- Cart item ID types are inconsistent.
- Pincode errors are not handled correctly.
- Checkout currently uses an alert instead of submitting the required checkout form.

### Business Rules Requiring Fixes

The audit identified issues related to:

- Price source and GST calculation.
- Maximum 5 items per product.
- Stock limits.
- Sold-out products.
- WELCOME10 coupon rules.
- Discount minimum and maximum limits.
- Free-shipping threshold.
- Indian rupee number formatting.
- Search + category + sorting working together.
- Pincode error handling.

### UI / UX Issues Confirmed

- Navbar links do not have useful destinations.
- Product cards shift size when the Add to Cart button appears.
- Global transition styling causes unnecessary visual movement.
- Mobile layout uses a fixed width and is not responsive.
- Search has no proper empty-result state.
- Cart experience needs clearer controls and states.

### Accessibility Issues

- Focus outlines have been removed.
- Several interactive elements are not semantic buttons.
- Form inputs do not have proper labels.
- There are multiple H1 elements.
- Cart and Quick View dialogs need better accessibility behavior.

### SEO Issues

- Page title is not descriptive.
- Required metadata is missing.
- Canonical information is missing.
- Open Graph and Twitter metadata are missing.
- Required JSON-LD structured data is missing.
- There should be one main H1.
- Product images need descriptive alt text.

### Performance / Asset Issues

- The current page loads prohibited external libraries.
- Current image assets are heavy.
- The hero image is especially large.
- Font loading needs to follow the brand requirements.

### Brand Issues

- Current colors do not follow the Mistvale palette.
- Current fonts do not follow the brand requirements.
- Some existing marketing claims violate the provided brand/content rules.
- Marquee/blinking effects are not allowed.
- Newsletter is currently presented as a popup instead of the required inline section.
- Required Trust Strip and FAQ sections are missing.

### Current Status

- Original website manually tested.
- Code audit completed.
- Manual observations verified against the code.
- Additional issues identified from README.md and BRAND.md.
- No implementation changes made yet.