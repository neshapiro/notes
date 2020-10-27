# Fetching Data

Next.js doesn't change how your component executes, so you fetch data the same way.
Scott recommends swr or react-query.

Next will automatically inject `fetch` into your environment and will apply the polyfill if necessary.

Fetching data ahead of time offers three methods
- `getStaticProps` should return an object that contains a `props` property. This will only be executed in Next, never in client-side React. The results will be saved into a cached JSON file and passed as props to the client-side component for hydration.
- `getStaticPaths` to be used if we need the value of the url params in order to fetch the content. Should return an object that contains a `paths` property set to an array of objects with a `params` property.
  - Can also set the `fallback` property to `true` so that you can at pre-render runtime when someone navigates to it instead of doing it at build time.
- `getServerSideProps` should return an object that contains a `props` property. You can think of this as API handlers that live inside your page. The difference between this and `getStaticProps` is that this `getServerSideProps` is executed per request while `getStaticProps` is executed once at build time.

Do you need data at runtime but dont need SSR? Use client-side data fetching.
Do you need data at runtime but do need SSR? Use `getServerSideProps`
Do you have pages that rely on data that is cachable and accessible at build time? Like from a CMS? Use `getStaticProps`
Do you have the same as above but the pages have dynamic URL params? Use `getStaticProps` and `getStaticPaths`

Do not use `getServerSideProps` unless you absolutely need it.