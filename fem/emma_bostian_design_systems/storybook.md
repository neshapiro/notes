# Storybook

Storybook can show components, their states, code snippets, and documentation.

It's meant to be used as a communication tool between developers, product, and design.

# Set up

Run this command
`npx -p @storybook/cli sb init`

This will set up a stories directory with some default stories, a .storybook directory to allow for configuration (like plugins), and will add two scripts to your package.json file:

1. storybook
2. build-storybook

By default it uses the stories/ directory because it doesn't know the default structure of your project, but stories should live alongside your components. This can be changed via the `.storybook/main.js` file.

## Addons

### Actions

This addon comes by default, but allows you to simulate actions (e.g. you have a button trigger an embedded youtube player)

### Docs

Run the command `npm i -D @storybook/addon-docs`

When this is done, add the following to the addons array in `.storybook/main.js`

```
{
    name: "@storybook/addon-docs",
    options: {
        configureJSX: true,
    },
},
```

This will add a new tab next to Canvas in Storybook to add Documentation for each component!

### Background

Run the command `npm i -D @storybook/addon-backgrounds`

When this is done, add the following to the addons array in `.storybook/main.js`

`"@storybook/addon-contexts/register"`

This will give us the ability to change the background.

### Knobs

Run the command `npm i -D @storybook/addon-knobs`

When this is done, add the following to the addons array in `.storybook/main.js`

`"@storybook/addon-knobs"`

This will give us the ability to change state of a component (e.g. set a button to disabled)

Note: It's recommended to have more stories than to have a component instead of exposing all knobs on one story

### Context

Run the command `npm i -D @storybook/addon-contexts`

When this is done, add the following to the addons array in `.storybook/main.js`

`"@storybook/addon-backgrounds/register"`

This will give us the ability to set context.

### Accessibility

Run the command `npm i -D @storybook/addon-a11y`

When this is done, add the following to the addons array in `.storybook/main.js`

`"@storybook/addon-a11y/register"`

This will give us the ability to do quick accessibility checks.

## Customizations

[Check out the slides](https://fem-design-systems.netlify.app/customizing-storybook)

This is needed if you want to have your brand identity on your Storybook. It will require a `manager.js` file to specify the config. Here you can choose to use their standard themes, or you can create and import your own!
