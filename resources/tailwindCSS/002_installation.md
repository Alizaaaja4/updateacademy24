## Get started with Tailwind CSS

Tailwind CSS operates by scanning your HTML files, JavaScript components, and other templates for specified class names. It then generates corresponding styles and compiles them into a static CSS file.

### Installation

- **Tailwind CLI:**
  The easiest and quickest way to start using Tailwind CSS from scratch is through the Tailwind CLI tool. The CLI can also be used as a standalone executable if you prefer not to install Node.js. If you need to install Node.js, you can find it [here](https://nodejs.org/).

  - **Step 1: Install Tailwind CSS**
    Install tailwindcss via npm, and create your tailwind.config.js file.

    ```bash
    npm install -D tailwindcss
    npx tailwindcss init
    ```

  - **Step 2: Configure your template paths**
    Add the paths to all of your template files in your tailwind.config.js file.

    ```javascript
    /** @type {import('tailwindcss').Config} */
    module.exports = {
        content: ["./src/**/*.{html,js}"],
        theme: {
            extend: {},
        },
        plugins: [],
    }
    ```

  - **Step 3: Add the Tailwind directives to your CSS**
    Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.

    ```css
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

  - **Step 4: Start the Tailwind CLI build process**
    Run the CLI tool to scan your template files for classes and build your CSS.

    ```bash
    npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
    ```

  - **Step 5: Start using Tailwind in your HTML**
    Add your compiled CSS file to the `<head>` and start using Tailwind’s utility classes to style your content.

    ```html
    <!doctype html>
    <html>
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link href="./output.css" rel="stylesheet">
    </head>
    <body>
        <h1 class="text-3xl font-bold underline">
            Hello world!
        </h1>
    </body>
    </html>
    ```

For more installation options like Using PostCSS, Framework Guides, and Play CDN, visit the [Tailwind CSS installation documentation](https://tailwindcss.com/docs/installation).
