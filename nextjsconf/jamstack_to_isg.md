# What they were using
- JAMStack
  - HTML generated at build time
  - Hosted in S3
- Contentful as CMS
  - Multiple Daily Updates

# What they moved to
- User makes a request from site. Next serves current version of HTML. Checks if content is stale. If it's stale, create a new render so that the next time a request is made it has the new version.
- Use getStaticprops, getContent and pass it as props, use revalidate option for how to know when the content is stale
  - Revalidate can be as low as 1 second
- For dynamic pages, we can set a fallback (like a 404)