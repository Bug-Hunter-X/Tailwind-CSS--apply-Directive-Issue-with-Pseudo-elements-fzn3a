# Tailwind CSS @apply Directive Issue with Pseudo-elements

This repository demonstrates a bug encountered when using Tailwind CSS's `@apply` directive with pseudo-elements (`::before`, `::after`). The `@apply` directive fails to correctly apply styles to these elements, resulting in unexpected behavior.

## Bug Description

When applying styles to a pseudo-element using `@apply` within a class definition, the styles might not be applied as expected.  This is particularly noticeable when dealing with background colors, padding, or other properties that visually impact the pseudo-element.

## Reproduction Steps

1. Clone this repository.
2. Run a local web server (e.g., `python -m http.server`).
3. Navigate to `index.html` in your browser.
4. Observe that the pseudo-element does not have the expected styles applied.

## Solution

The solution is to apply styles to the pseudo-element directly, outside of the `@apply` directive, as demonstrated in `solution.css`.

## Additional Notes

This issue is specific to using `@apply` within a pseudo-element selector. Applying classes directly to the pseudo-element using Tailwind's utility classes works as expected.