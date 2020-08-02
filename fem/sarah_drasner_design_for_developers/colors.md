# Color Modes

All your teachers lied to you, red yellow and blue are not the primary colors!
When working on the computer, you're working with Red, Blue, and Green (RBG).

Color mixing is the difference here- additive or subtractive.
Computers are additive.
What we were taught in school is subtractive.

## Color Combinations

The color wheel!

Types of combinations:

- Monochromatic - Variances of a single color
- Complementary -
- Analogous - Colors next to each other on the spectrum
- Triadic -

A color is only a color in relation to another color.

[Kuler / Color CC](https://color.adobe.com/create/color-wheel)

Recommended Reading - [Color Theory for Designers](https://www.smashingmagazine.com/2010/02/color-theory-for-designer-part-3-creating-your-own-color-palettes/)

### Duotones

Think Spotify Ads

This is the idea that if you shine a light on an object, the shadow will be the opposite color. I.e. yellow light casts purple shadows

## Color in Code

- RGBA - 0 to 255 from dark to light. Keeping the same numbers makes variances of gray.
- Hex - Most common but not human readable
- HSLA - Sarah's favorite! Hue is a number from 0 - 360. Saturation and Lightness are percentage from 0 to 100%. Alpha is a number from 0 to 1. This is great for generation of colors. [See this example](https://ich.unesco.org/dive/biome/?language=en)

Recommended Reading - [Code side of Color](https://www.smashingmagazine.com/2012/10/the-code-side-of-color/)
Named colors (like `color: white`) are super inconsistent. There is even a [game to guess the CSS color](http://codepo8.github.io/css-colour-names/)

## Color Tools

[Dribbble](https://dribbble.com/)

- Allows you to get the palette from those designs
- Allows you to search by a color

[Coolors](https://coolors.co/)

- Generate a palette

[Paletton](http://paletton.com/)

- Build a palette based on proportions

[Adobe Capture](https://www.adobe.com/products/capture.html)

- Pull colors from an image
- Pull a mood from the image as well!

[Ultimate CSS Gradient Generator](https://www.colorzilla.com/gradient-editor/)

- Not great for finding a gradient colors, but has great gradient outputs based on two colors

[UI Gradients](https://uigradients.com/#Harvey)

- Much better for finding/generating a gradient color.

## How to work with colors

1. Start by anchoring to one color! Find a brand color and get energetic versions and corporate versions.
2. Then gather your accents against your anchor.
3. Now that you have a couple versions of your (3+) primary and accent colors, desaturate those to get your grays!
4. -> Profit

# Pro-tips

- Limit your colors to start. As your design begins to come together you'll know which colors need to be added in.
- Don't just animate gradients directly because it's really expensive to do that. Instead, Sarah made a [CodePen](https://codepen.io/sdras/pen/akAWPR/) to animate transparent masks. Creates two blocks of colors, creates a mask from one of them, and moves it with transforms.
- Transforms are a lot less expensive than other options like margin and left and especially changing background colors.
