# Config

Add a `next-config.js` to the root file for customizing the Next.js config.
This is where you would customize the webpack  bundle, environment variables, etc.

- By default, you can export a custom config that will use Webpack Merge to merge into Next's default config.
- Alternatively, you can export a function that takes in two parameters which allows you to check if the phase of the server
```
const {PHASE_PRODUCTION_BUILD, PHASE_DEVELOPMENT_SERVER} = require('next/constants');

module.exports = (phase, { defaultConfig }) => {
  if (phase === PHASE_DEVELOPMENT_SERVER) {
    return customDevelopmentConfig
  } else {
    return defaultConfig
  }
}
```

## Plugins

Next offers various Plugins that can wrap your config object! You can [find the list of Official and Popular plugins here](https://github.com/vercel/next-plugins)

```
const withMyPlugin = require('./myplugin.js);

module.exports = withMyPlugin(config);
```

If you need to add a lot of plugins, you can use `withPlugins` from `next-compose-plugins`