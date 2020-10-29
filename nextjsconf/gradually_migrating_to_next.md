# Gradually Migrating to Next

- Preface unsafe references to browser globals via typeof window !== 'undefined'
- Move head or react-helmet code into custom document component
- Document any polyfills
- Document globally imported scripts and styles to be used in _app.js

## Next.js Rewrites

### Pros
- Can ignore pregame work.
- Fastest

### Cons
- Splits between multiple repos
- Conversion process is complicated
- Client side routing must be relative, and make sure you're linking to Next.js paths

## Catch All Routes

### Pros
- No unique benefits

### Cons
- Requires pregame tasks
- PH
- Only viable for Create React App migrations


## Optional Catch All Routes

### Pros
	- Truly gradual

### Cons
	- Requires pregame tasks
	- Only viable for CRA migrations

## Toe Stubbing
- 3rd party libs unsafely reference browser globals
  - Use next dynamic to lazy load until after window is available - set ssr to false
  - Might need to use next-transpile-modules
  - [How to Import Browser Only Libraries Into Your Next.js Application Using next/dynamic](https://www.youtube.com/watch?v=DA0ie1RPP6g)
- Mixing client routing with Next.js routing
- Redux store shouldn't be global
- Circular dependencies
- SVGR - next-plugin-svgr
