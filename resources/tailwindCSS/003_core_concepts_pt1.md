# Core Concepts: Tailwind CSS

## 1. Utility-First Fundamentals ⚙️

**Explanation**:  
Tailwind CSS uses a utility-first approach where you build designs using small, reusable utility classes directly in your markup. This approach allows for rapid development without the need to write custom CSS.

**Example**:
```html
<div class="bg-blue-500 text-white p-4 rounded-lg">
  This is an example element with Tailwind CSS
</div>
```
In the example above [Utility-First](https://tailwindcss.com/docs/utility-first)
:
- `bg-blue-500`: Sets a blue background.
- `text-white`: Sets the text color to white.
- `p-4`: Sets padding to 1 rem.
- `rounded-lg`: Adds a large border-radius.


## 2. Handling Hover, Focus, and Other States 🖱️

**Explanation**:  
Tailwind CSS provides state variants like `hover:`, `focus:`, `active:`, and more, allowing you to apply styles based on the element's state.

**Example**:
```html
<button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
  Hover me
</button>
```
In the example above [State Variants](https://tailwindcss.com/docs/hover-focus-and-other-states):

- `hover:bg-blue-700`: Changes the background color to a darker blue when the element is hovered.

## 3. Responsive Design 📱

**Explanation**:  
Tailwind CSS supports responsive design with breakpoints. You can apply different utility classes for different screen sizes.

**Example**:
```html
<div class="bg-white p-4 md:bg-gray-200 lg:bg-gray-400">
  Responsive design
</div>
```
In the example above [Responsive Design](https://tailwindcss.com/docs/responsive-design):
- `md:bg-gray-200`: Changes the background color to light gray on medium screens (768px and above).
- `lg:bg-gray-400`: Changes the background color to dark gray on large screens (1024px and above).

---
That's all for part 1. Try some experimentation such as customizing CSS styles or any other ideas you have. Good luck and good luck!!