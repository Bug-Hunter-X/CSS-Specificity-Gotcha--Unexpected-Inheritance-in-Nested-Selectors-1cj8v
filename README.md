# CSS Specificity Gotcha: Unexpected Inheritance in Nested Selectors

This repository demonstrates an uncommon CSS specificity issue where a nested selector does not override a more general selector due to specificity rules and order of declaration. The `div p` selector, which intuitively should override `p`, may not always do so depending on the overall specificity calculation.

## Bug Description
The bug lies in the unexpected behavior of CSS specificity when combining nested selectors and general selectors.  A seemingly more specific selector like `div p` might not always override a less specific selector like `p`, especially when stylesheets or declarations are loaded in a certain order. This can lead to unexpected styling results.

## Solution
The solution involves understanding and addressing CSS specificity. The `!important` flag (used judiciously) can solve the problem, or the selector specificity could be modified to ensure it has a higher specificity than the conflicting general selector.