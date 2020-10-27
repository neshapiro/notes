# Working with SSR

Sometimes you just need to skip rendering some component on the server because it depends on the DOM API, it depends on client-side data, etc.

## Dynamic Imports

Dynamic Imports don't get rendered/built/bundled until they're accessed. Think about making a component it's own page entirely.

```
const SponsoredAd = dynamic(
  () => import('../components/sponsoredAd'),
  { ssr: false }
)
```

This can be used for something that relies heavily on the browser (like `document.body` or `window.something`)