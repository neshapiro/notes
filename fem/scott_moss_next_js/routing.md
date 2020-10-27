# Routing
[Link](https://hendrixer.github.io/nextjs-course/pages)

## Routes

### Standard Routes
Default routing in Next.js is pretty simple.
- For a single page, just create a file in the `pages/` directory. I.e. `pages/index.jsx`
- For a sub route, just create an additional directory in the `pages/` directory. I.e. `pages/about/company.jsx`
- For a dynamic route, just create a file using square brackets in the `pages/` directory. I.e. `pages/[id].jsx`. You can then pull id from the `useRouter` hook. I.e. `const {id} = useRouter()`

### Catch-all Routes
Catch-all routes are similar to globs.
You can use something like `docs/[...param].jsx` to catch `docs/notes/fem/scott-moss/nextjs`. When grabbing the params via `const { params } = useRouter()` it will set params to be `["notes", "fem", "scott-moss", "nextjs"]`.

This can be used whenever you have a bunch of pages with the same layout, but they need a unique URL. This is helpful for documentation or blogs.

## Navigation
The `<Link />` component is provided by Next to route between pages for client-side transitions
- The `href` prop should be relative to the `pages/` directory. If linking to a dynamic route, use the dynamic route name for the `href` prop and include an `as` prop to specify the variable. I.e. `<Link href="/notes/[id]" as="/notes/1">`
- The text inside the `<Link />` component should still be wrapped in an `a` element without an assigned `href`.

Server-side routing should continue to use `a` elements.

## Programmatic Routing
For programmatic client-side navigation, we'll leverage the `push` method on Next's `useRouter` hook. This proxies the HTML5 push state router, which allows refresh and replace. The `push` method allows two arguments - the name and the resolved URL. I.e. `router.push('/user/[id]', '/user/' + id)`
Note: It's possible that ths might work without the `href` prop (only using the `as` prop), however, that might mean that there is no pre-fetching optimization provided by Next. Something worth looking into.