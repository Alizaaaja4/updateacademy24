# Core Concepts III : Tailwind CSS

## 6. Customizing Spacing 📏
Use the `spacing` key in the `theme` section of your `tailwind.config.js` file to customize Tailwind’s default spacing/sizing scale.

**Example**:
```html
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    spacing: {
      '1': '8px',
      '2': '12px',
      '3': '16px',
      '4': '24px',
      '5': '32px',
      '6': '48px',
    }
  }
}
```
By default the spacing scale is inherited by the `padding`, `margin`, `width`, `minWidth`, `maxWidth`, `height`, `minHeight`, `maxHeight`, `gap`, `inset`, `space`, `translate`, `scrollMargin`, and `scrollPadding`core plugins.

For more examples, you can visit the documentation 📖[Customizing Spacing](https://tailwindcss.com/docs/customizing-spacing) 📖

## 7. Plugins 🔌
Plugins let you register new styles for Tailwind to inject into the user’s stylesheet using JavaScript instead of CSS.

To get started with your first plugin, import Tailwind’s `plugin` function from `tailwindcss/plugin`. Then inside your `plugins` array, call the imported `plugin` function with an anonymous function as the first argument.

**Example**:
```html
const plugin = require('tailwindcss/plugin')

module.exports = {
  plugins: [
    plugin(function({ addUtilities, addComponents, e, config }) {
      // Add your custom styles here
    }),
  ]
}
```
Plugin functions receive a single object argument that can be **destructured** into several helper functions:

- `addUtilities()`, for registering new static utility styles
- `matchUtilities()`, for registering new dynamic utility styles
- `addComponents()`, for registering new static component styles
- `matchComponents()`, for registering new dynamic component styles
- `addBase()`, for registering new base styles
- `addVariant()`, for registering custom static variants
- `matchVariant()`, for registering custom dynamic variants
- `theme()`, for looking up values in the user’s theme configuration
- `config()`, for looking up values in the user’s Tailwind configuration
- `corePlugins()`, for checking if a core plugin is enabled
- `e()`, for manually escaping strings meant to be used in class names


For more examples, you can visit the documentation 📖[Plugins](https://tailwindcss.com/docs/plugins) 📖

## 8. Presets 🎯
By default, any configuration you add in your own `tailwind.config.js` file is intelligently merged with the **default configuration**, with your own configuration acting as a set of overrides and extensions.

The `presets` option lets you specify a different configuration to use as your base, making it easy to package up a set of customizations that you’d like to reuse across projects.

**Example**:
```html
/** @type {import('tailwindcss').Config} */
module.exports = {
  presets: [
    require('@acmecorp/tailwind-base')
  ],
  // ...
}
```
This can be very useful for teams that manage multiple Tailwind projects for the same brand where they want a single source of truth for colors, fonts, and other common customizations.

For more examples, you can visit the documentation 📖[Presets](https://tailwindcss.com/docs/presets) 📖

---
That's it for part 3. Feel free to experiment with custom styles and any other ideas you have in mind. Good luck, and happy coding!