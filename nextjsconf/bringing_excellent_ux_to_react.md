# Bringing Excellent UX to React Ecosystem

## Google Font Optimizations included in Next.js
- Inlined into HTML
- Pre-load font
- Bundle only during load time

## 3rd Party Scripts
- Can't load 3rd party without affecting critical rendering path
- ScriptLoader component made for anyone to handle loading outside of Next.js context
  - 4 different priorities
    - Lazy - prioritize all other resources
      - Defer - prioritize all 1st party scripts
      - Eager - prioritize this script
      - dangerousRenderBlocking - defaults to original behavior

## Image component
  - Better CDN support
  - Enforced sizing
  - Automated image optimization
  - Automatic srcset
  - Alex is giving a talk on Images

## Critical CSS inlined in Next.js

## Conformance
  - Eslint plugin
  - Webpack conformance plugin
    - Un-optimal chunking
    - Minification disabled
    - Bundler config checks