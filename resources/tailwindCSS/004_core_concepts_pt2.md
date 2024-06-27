# Core Concepts: Tailwind CSS

## 4.  Dark Mode 🌙

**Explanation**:  
Tailwind CSS has built-in support for dark mode. You can use the `dark:` variant to style elements when dark mode is enabled.

**Example**:
```html
<div class="bg-white dark:bg-black text-black dark:text-white p-4">
  Dark mode example
</div>
```
In the example above [Dark Mode](https://tailwindcss.com/docs/dark-mode)
:
- `dark:bg-black`: Changes the background color to black when dark mode is enabled.
- `dark:text-white`: Changes the text color to white when dark mode is enabled.


## 5. Reusing Styles ♻️

**Explanation**:  
Although Tailwind is utility-first, you can still create custom classes for reusable styles.

**Example**:
```html
<style>
  .btn-primary {
    @apply bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded;
  }
</style>

<button class="btn-primary">
  Reusable Button
</button>
```
In the example above [Reusing Styles](https://tailwindcss.com/docs/reusing-styles):

- `@apply` is used to combine several utility classes into a single custom class `btn-primary`.

## 6. Adding Custom Styles 🎨

**Explanation**:  
You can add custom styles and configure Tailwind CSS to suit your needs by modifying the `tailwind.config.js` file.

**Example**:
```html
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        customColor: '#ff6347',
      },
    },
  },
};
```

```html
<div class="bg-customColor text-white p-4">
  Custom color example
</div>
```
In the example above [ Customizing Tailwind](https://tailwindcss.com/docs/customizing-colors):
- `customColor` is added and used in the HTML.

## 7. Functions & Directives 📜

**Explanation**:  
Tailwind CSS provides various functions and directives to facilitate customization, such as `@apply`, `@variants`, `@responsive`, and more.

**Example**:
```html
<style>
  .card {
    @apply bg-white shadow-md rounded-lg p-6;
  }

  @variants hover {
    .card:hover {
      @apply bg-gray-100;
    }
  }
</style>

<div class="card">
  Card with custom styles
</div>
```
In the example above [Functions & Directives](https://tailwindcss.com/docs/functions-and-directives):
- `@apply`: Combines several utility classes into a single custom class.
- `@variants hover`: Adds a hover variant to the card class.

---
That's it for part 2. Feel free to experiment with custom styles and any other ideas you have in mind. Good luck, and happy coding!