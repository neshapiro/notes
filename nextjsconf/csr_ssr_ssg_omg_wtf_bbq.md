# CSR, SSR, SSG
Select on page to page basis on how to use Next.js

## Client-side Rendering
- Rendering happening on the browser
- Request sent from browser to server, serves loading state, response comes in from server, replace loading state with rendered response
- SWR will allow you to cache the request, and update in the background
- Bad for SEO

### When to use it
- Don't care about SEO
- Private pages
- Dependent upon specific info (auth)

## Server-side Rendering
- Rendering happening on the server
- Next sends request to server, server responds with fully rendered page
- Uses getServerSideProps
- Server returns resulting JSON as a response, Next.js uses JSON response to render page

## Pros
- Dynamic content readily available
- Good for SEO
- No loading state

## Cons
- Slower time to first byte (due to pre-rendering)
- Slower rendering on server
- Results cannot be cached w/o extra config
- Incompatible with libraries that need access to document
  - Can lazy load this though

### When to use it
- Pages data MUST be fetched at request time
- Lots of pages (thousands)
- Pages with heavy work-load that shouldn't lean heavily on browser clients

# Static Site Generation
- Rendering happening during build time
- Fastest load time
- Completely static
- Incremental Static Regeneration
  - Server generates pages with defined paths on build time
  - If a user requests non-generated page
    - Serve fallback
    - Send API request to server
    - Statically generate page in background
    - Serve generated page to browser
    - Page is now in pre-generated page list

## Pros
- Super fast
- Built once served by CDN
- Cached
- Immediately displayed
- Build offline PWA
- Millions of pages can be generated incremenetally
- Great for SEO
- No server needed
- Pre-generate page ahead of user's request

## Cons
- Slow server site build
  - ISR resolves this
- Regenerate all pages every time (when fallback is false)
- Incompatible with libraries that use broswer natives (window or document)

### When to use it
- Blogs
- Marketing
- Help and documentation
- Ecommerce product listings
- Pages infrequently updated