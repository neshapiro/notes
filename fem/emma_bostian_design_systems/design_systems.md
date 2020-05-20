# Design Systems

## What are design systems?

Designers often talk about the foundational elements of the UI kit:

- Color
- Typography
- Grid
- Iconography

Engineers often talk about the component library and style guide.

Really, it's all of these things wrapped up.

## Why do design systems matter?

Everyone needs to achieve the same results from your application. They don't need to do it in the same way, but they need to be able to accomplish their tasks.

Design systems help solve shared problems like mobile responsiveness and accessibility. Color palette, font scale, and tab ordering can be shared throughout the site or applications.

They enable consistency throughout your applications regardless of the implementer. Often, design systems are shared across multiple products (think Material Design for Google). A well maintained design system allows multiple applications to seamlessly update via new packages.

Serves as an amazing tool for onboarding.

Components can allow parameters for customization and flexibility. This gives a set of tools for people to use.

When a design system is up and running, it's faster to develop new experiences.

## What are the drawbacks?

- A full design system takes a long time. It's going to take months and will never be complete.
- Maintenance will need to be ongoing to support design trends and changes.
- Will require leadership investment. Lack of adoption is the number one reason why design systems fail.

## Who builds it?

Design systems can be built via a centralized model - a single dedicated team with Engineers, Designers, and PM.

They can also be built via a distributed model - the consuming teams contribute back to the design system. Teams own the design system and it's developed by multiple vantage points.

Hybrid model can support both of these options. A centralized team will be the main driver, but distributed teams can make change requests.

## Who are they for?

> _"If a design system is built by a company, it's for that company."_ - [Chris Coyier](https://css-tricks.com/who-are-design-systems-for/)

Even if it's open source, the target office is the company.

## Placeholder

> _"And you thought buttons were easy"_ - [Nathan Curtis](https://medium.com/eightshapes-llc/and-you-thought-buttons-were-easy-26eb5b5c1871)

There are a lot of considerations for even something as simple as a button. They're used everywhere. Not only are there a ton of properties, but there are a ton of states that can change those properties. The more button types you add, the more combinations of buttons your app is expected to support. Add different themes and this gets out of control quickly.

## Three pillars of design systems

### Design Language

Personality or brand identity for the application and its corresponsding design.

Foundation

- Color
- Typography
- Grid
- Spacing
- Iconography
- Illustrations
- Motion

UI Kit

- Buttons
- Text Fields
- Modals
- Dropdowns
- Navigation
- Footer

### Component Library

Can be built with many different frameworks/libraries (Vue/Rect/Angular) or technologies (SCSS, CSS-in-JS, Jest, Greensock).

### Style Guide

Documentation for the design language, UI Kit, and component library. It tells people where and how to get assets. How to get up and running. How to integrate. How to open Pull Requests.

Style Guide Technologies:

- Storybook
- Invision
- Gatsby
- React Styleguidist

## Building a design system

### Define your design principles

The grounding values that drive the creation of your products. Answer the question _"What do you want your users to feel when using your product?"_

Example from Atlassian: _"Bold, optimistic, and practical"_

### Conduct a UI audit

For legacy applications, we need to take screenshots of everything that currently exists. Group them by functionality instead of visual experience since functionality will stay the same.

#### Calculating priority

To prioritize components, ask these questions:

- Does this request embody our design principles?
- Does this request require a lot of design/development effort?
- Is there a high risk associated?
- Does it coincide with our roadmap?
- Does this improve UX?
- Are we confident in this dectision or will we need to revisit in the near future?
- Is this request technically feasible?

##### Impact Metrics

Adoption Metric - Indicate a component has higher priority

- Impact
- Identity
- Confidence

Opposition Metric - indicate a component has lower priority

- Maintenance
- Risk
- Effort

Scores

- impact + identity + confidence = individual adopter total
- individual adopter total / # of adopter questions = individual adopter
- maintenance + risk + effort = individual opposer total
- individual opposer total / # of opposer questsions = individual opposer

Sum the scores from your adopter and opposer questions, then find the mean. Take individual scores and find the mean across all participants. This becomes your (X,Y) coordinates for the priority of your components.

[Check out the graph quadrants here](https://www.canva.com/design/DAD2ReY78JQ/9PwrO5lswW_tB4o4ZEbA2Q/view?utm_content=DAD2ReY78JQ&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton#58)

### Create your checklists

Design Checklist

- Accessibility - Can all users regardless of circumstance use this component?
- Interaction - How should it respond when user interacts with it?
- Context - How and where should this component be used?
- Completion - Are all states, including neutral, hover, focus, and disabled, defined?
- Content - What type of content does this component rely upon?
- Customization - Are aspects of this component customizable? How so?
- Screen Resolution - How does this component look at various screen resolutions?

Development Checklist

- Accessibility - Can all users regardless of circumstance use this component?
- Responsiveness - Does it respond to browser resizing and various screen resolutions?
- Completion - Did we account for all aspects of the design?
- Customization - Have we implemented all customizable aspects of the component?
- Error Handling - How do our components respond when something breaks?
- Compatibility - How does this work across browsers? Do we need polyfills?

### Common Mistakes

#### Starting for Scale

While ability to scale is good, building your components for scale be detrimental. Only scale when needed.

#### Educating before building

Educating your teams about your design system can negatively impact rapport if there's nothing to use.
(????)

#### Not discussing workflow

If you're going to be collaborating on a design system, come to terms on a working model.

#### Not documenting decisions

Design systems require a lot of investment and will often have lots of eyes on them.
Documenting decisions will save you and your team the headache of having to explain to each stakeholder why you're doing something a certain way.

# Foundations of Design

Decisions should coincide with your brand identity.

## Color

### Color Mixing

- Additive Color mixing - Colors start black and become more white as red, blue, green are added. RGB colors are additive. TVs and monitors use this.
- Subtractive Color mixing - Colors start white and as filters are added it takes on the appearance of color. Photos and magazines use this.

### Color Types

- Primary Colors - Colors which cannot be created by combining other colors
- Secondary Colors - Result from mixing primary colors
- Tertiary Colors - Result from combining primary and secondary colors

### Color Palettes

- Monochromatic - Created by establishing variations on a shade of a single color
- Complementary - Select two colors opposite from each other on the color wheel
- Analagous - Select three colors that are side by side on the color wheel
- Triadic - Select three colors evenly spaced around the color wheel

### Terminology

- Hue - Any color on the color wheel
- Saturation - The intensity/purity of the color
- Luminance - The brightness/light of the color
- Shade - Incorporate black to a base hue, which darkens the color
- Tint - Incorporate white to a base hue, which lightens the color
- Tone - Combining black, white, or gray with a base hue
  - Subtle variations of the original color, good for things like hover state

### Naming

Naming colors is hard. A lot of people use the primary, secondary, tertiary pattern for themes instead of colors. It's also common to see shades in 100 values (blue-100, blue-200, etc.) to leave space for additional shades that need to be added.

### Semantics

Colors elicit emotional responses.

- Red - Associated with fire, violence, war, love, and passion. Can actually raise user's blood pressure. Limit.
- Orange - Vibrant color associated with earth, autumn, change, movement, creativity.
- Yellow - Associated with happiness, sunshine, and cheer, but also deceit and cowardice.
- Green - Represents new beginnings, renewal, growth, and abundance. Can also elicit envy and jealousy. Has calming effects. Similar to blue but has vibrancy of yellows.
- Blue - Associated with calmness, responsibility, reliability, and peace. Also sadness.
- Purple - Associated with luxury, royalty, wealth.
- Black - Associated with power, elegance, and formality. Also evil, death, mystery.
- White - Associated with purity, cleanliness, virtue, goodness. Common in modern designs.
- Gray - Associated with conservativism, is formal and modern. Can also represent moodiness, depression.
- Brown - Represents dependability, reliability, earthiness. A bit boring.

### Color Values

- Hex is hexidemical (base 16)
- RGB is red, green, blue
- RGBA is RGB with an added alpha
- CYMK is the subtractive color mixing model used in print design

### Creating a color palette

Use [Coolors](https://coolors.co/) to generate a color scheme

In Figma you can select a color and add it to color styles

## Typography

- Base line is the imaginary line our letters sit on
- Cap line is imaginary upper boundary of capital letters and ascenders
- X-height is the height of the typeface's lowercase letters
- Ascender is the piece of a letter rising above the x-height
- Descender is the piece of a letter falling below the baseline
- Tracking is the uniform amount of spacing between characters
- Kerning is horizontal spacing between two consecutive characters
- Leading is the vertical space between lines of text

### Types of fonts

- Serif fonts have short lines or stokes on the open ends of letters
  - Times New Roman
  - Droid Serif
  - Playfair Display
- Sans-serif do not have short lines or strokes on open ends of letters
  - Helvetica
  - IBM Plex Sans
  - PT Sans
- Monospaced means letters and characters occupy the same amount of space
  - Anonymous Pro
  - IBM Plex Mono
  - Roboto Mono

### Font measurements

- Pixels are units used by designers, howeever they shouldn't be used to define a type scale
- Em is a unit of typography relative to the currently specified point-size.
- Rem is a unit of typography relative to the html/body element.

Relative fonts units like em and rem is more accessible for font, but don't use them for spacing.

### Typescale

- Major Third
- Major Second
- Perfect Fourth
- Golden Ratio
- Perfect Fifth

#### Create a new typescale

1. Choose a font from [Google Fonts](https://fonts.google.com/)
2. Create a [type scale](https://type-scale.com/)

### Question

- Would you recommend adding more than one font family?

  - Yes, but don't exceed three. Normally you'll see a sans-serif font header with serif font paragraphy text

## Misc

### Other areas of design

- Grid
- Spacing
- Accessibility
- Motion
- Iconography

### Additional Resources

- [Smashing Magazine Color Theory](https://www.smashingmagazine.com/2010/01/color-theory-for-designers-part-1-the-meaning-of-color/)
- [Canva Color Wheel](https://www.canva.com/colors/color-wheel/)
- [Canva Typography](https://www.canva.com/learn/typography-terms/)
- [Em vs Rem vs Px](https://engageinteractive.co.uk/blog/em-vs-rem-vs-px)
- [Design for Developers by Sarah Drasner](https://frontendmasters.com/courses/design-for-developers/)

## Buttons

Need to look and function like buttons

- Solid Buttons - Buttons with solid fill background. Easily reognizable and great choice for primary button
- Ghost Buttons - Buttons without a solid fill background, just an outline. Good for secondary buttons.
- Icon Buttons - Buttons with only an icon and no label. These are bad for accessibility.

### Button Styles

- Border radius - More playful
- Drop shadow - give buttons elevation
- Labels - Place readability above all else. Consider color contrast for accessibility. Make sure font is thick enough.
- Vertical padding - Large enough to use on touch/mobile device
- Horizontal padding - Keeps buttons responsive. Can also set minimum widths.

Square buttons draw the user's eye more because there are more pixels to draw the users eye.

# Figma Notes

- When you create a group, you can write click and create a component. You can then use that component directly and not have to copy/paste or recreate.
- When resizing, hold down shift key to maintain proportions.

# Misc Notes

- Recommends using increments of 4 for px values like spacing. I personally like increments of 6.
- [Undraw](https://undraw.co/) is a great free resource for illustrations that allows you to set a color
- [The Noun Project](https://thenounproject.com/) is a great resource for icons
