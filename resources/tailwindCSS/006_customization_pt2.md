# Core Concepts II : Tailwind CSS

## 3. Theme Configuration 🎨

The `theme` section of your `tailwind.config.js` file is where you define your project’s color palette, type scale, fonts, breakpoints, border radius values, and more.

**Example**:
```html
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    screens: {
      sm: '480px',
      md: '768px',
      lg: '976px',
      xl: '1440px',
    },
    colors: {
      'blue': '#1fb6ff',
      'purple': '#7e5bef',
      'pink': '#ff49db',
      'orange': '#ff7849',
      'green': '#13ce66',
      'yellow': '#ffc82c',
      'gray-dark': '#273444',
      'gray': '#8492a6',
      'gray-light': '#d3dce6',
    },
    fontFamily: {
      sans: ['Graphik', 'sans-serif'],
      serif: ['Merriweather', 'serif'],
    },
    extend: {
      spacing: {
        '128': '32rem',
        '144': '36rem',
      },
      borderRadius: {
        '4xl': '2rem',
      }
    }
  }
}
```
For more examples, you can visit the documentation 📖[Theme Configuration](https://tailwindcss.com/docs/theme) 📖

## 4. Customizing Screens 🖥️

You define your project’s breakpoints in the theme.screens section of your tailwind.config.js file. The keys become your responsive modifiers (like md:text-center), and the values are the min-width where that breakpoint should start.

The default breakpoints are inspired by common device resolutions:

**Example**:
```html
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    screens: {
      'sm': '640px',
      // => @media (min-width: 640px) { ... }

      'md': '768px',
      // => @media (min-width: 768px) { ... }

      'lg': '1024px',
      // => @media (min-width: 1024px) { ... }

      'xl': '1280px',
      // => @media (min-width: 1280px) { ... }

      '2xl': '1536px',
      // => @media (min-width: 1536px) { ... }
    }
  }
}
```
For more examples, you can visit the documentation 📖[Customizing Screens](https://tailwindcss.com/docs/screens) 📖

## 5. Customizing Colors 🌈

Tailwind includes an expertly-crafted default color palette out-of-the-box that is a great starting point if you don’t have your own specific branding in mind.

| Color Name | 50       | 100      | 200      | 300      | 400      | 500      |
|------------|----------|----------|----------|----------|----------|----------|
| Slate      | #f8fafc  | #f1f5f9  | #e2e8f0  | #cbd5e1  | #94a3b8  | #64748b  |
| Gray       | #f9fafb  | #f3f4f6  | #e5e7eb  | #d1d5db  | #9ca3af  | #6b7280  |
| Zinc       | #fafafa  | #f4f4f5  | #e4e4e7  | #d4d4d8  | #a1a1aa  | #71717a  |
| Neutral    | #fafafa  | #f5f5f5  | #e5e5e5  | #d4d4d4  | #a3a3a3  | #737373  |
| Stone      | #fafaf9  | #f5f5f4  | #e7e5e4  | #d6d3d1  | #a8a29e  | #78716c  |
| Red        | #fef2f2  | #fee2e2  | #fecaca  | #fca5a5  | #f87171  | #ef4444  |

In addition to that, there is still a website reference that you can visit to look for color codes 😊
- You can also explore color codes further on [color-hex.com](https://www.color-hex.com/), [colorhunt.co](https://colorhunt.co/) or [palettes.shecodes.io](https://palettes.shecodes.io/)

<br> 

**Example**:
```html
/** @type {import('tailwindcss').Config} */
module.exports = {
  theme: {
    colors: {
      // Configure your color palette here
    }
  }
}
```
For more examples, you can visit the documentation 📖[Customizing Colors](https://tailwindcss.com/docs/customizing-colors) 📖

---
That's it for part 2. Feel free to experiment with custom styles and any other ideas you have in mind. Good luck, and happy coding!