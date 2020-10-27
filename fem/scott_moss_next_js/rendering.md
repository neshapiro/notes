# Rendering Modes

- `Static Generation` - Pages built at build time into HTML. CDN cacheable.
  - Converts React into HTML string at build time.
  - Content that is not changed by a user.
- `Server-side Rendering` - Pages built at run time into HTML. Cached after the initial hit.
  - Converts React into HTML string at run time.
- `Client-side Rendering` - Single-page app.

## Pre-rendering

Pre-rendering just means we're going to turn this to an HTML string before it goes to the browser.