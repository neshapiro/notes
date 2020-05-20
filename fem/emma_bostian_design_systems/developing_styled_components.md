# Developing Styled Components

## How we used to apply CSS

- External CSS stylesheet with link in head HTML element
- Within HTML file in style tag
- Inline on HTML elements

## Problems with CSS

1. CSS examines how specific a style is, and different selectors hold different point values. The highest point total wins the specificity war. Some types of selectors:

   1. Type selectors and pseudo-elements
   2. Class selectors, attribute selectors, and pseudo-classes
   3. ID selectors

2. Styles slowly became decentralized and hard to remove or update.
3. A lack of knowledge about CSS specifity leads to !importants

## Solutions

- CSS naming architectures help combat these problems
- CSS pre-processors introduced nesting to offer some new solutions
- CSS in JS allows us let to let CSS directly in our components JS file so it's fully encapsulated.
