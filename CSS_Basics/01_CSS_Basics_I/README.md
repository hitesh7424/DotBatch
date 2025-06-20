## CSS Basics 01

### Why Learn CSS?

- CSS determines how you want to show the content and controls the appearance of content.

### What is CSS?

- **CSS**: Cascading Style Sheets

### What are Selectors in CSS?

- Selectors are ways to select elements in an HTML document.

#### Types of Selectors:

1. **Element Selector / Tag Selector / Type Selector**:

   - Select elements using tags like `<p>`, `<table>`, etc.

2. **Class Selector**:

   - Select elements with a class name using `.classname` (e.g., `.green`, `.blue`).

3. **ID Selector**:

   - Select elements by ID name using `#idname` (e.g., `#temp-button`).

4. **Pseudo-classes Selector**:

   - Syntax: `selector:pseudoclass`
   - Examples:
     - `:hover`
     - `:visited`
     - `:unvisited`
     - `:active`

5. **Multiple Selector / Grouping Selector**:

   - Combine multiple selectors separated by a comma.

#### Explore Time:

- **Universal Selector**: Selects all elements using `*`.
- **Nested Selector**: Selects child elements within a parent.
- **Attribute Selector**: Select elements based on attributes.

### How to Add Styling to HTML?

1. **Inline CSS**:

   - Configuration within the tag itself using the `style` attribute.

2. **Internal CSS**:

   - Configuration within the `<style>` tag in the `<head>` section.

3. **External CSS**:

   - Configuration in an external `.css` file linked to the HTML using the `<link>` tag.

### Specificity in CSS:

- **Order of Specificity**:
  1. Tag Selector
  2. Class Selector
  3. ID Selector
  4. Inline CSS
  5. `!important` rule

### Box Model in CSS:

- Every element is a rectangular box.
- Components:
  - Width
  - Height
  - Padding
  - Border
  - Margins

### Colors in CSS:

1. **Hexadecimal Colors**:

   - Syntax: `#RRGGBB` (e.g., `#0000FF` for blue, `#000000` for black).

2. **RGB Colors**:

   - Syntax: `rgb(0-255, 0-255, 0-255)` (e.g., `rgb(0, 0, 0)` for black).

3. **Predefined Colors**:

   - Cross-browser color names like `green`, `black`, `white`, `aqua`.

#### Explore Time:

- Experiment with color transparency using `rgba()`.

### Fonts in CSS:

- **Font Properties**:
  1. Font Family
  2. Font Weight
  3. Font Style
  4. Emphasis & Importance
- Learn how to add external fonts using `@font-face` or Google Fonts.

### Units in CSS:

1. **Absolute Units**:

   - `mm`, `cm`, `in`, `px`

2. **Percentage Units**:

   - Values relative to the parent element (e.g., `10%`, `20%`).

3. **Relative Units**:

   - **Relative to Font Size**:
     - `em`: Relative to the parent element's font size (e.g., `1em = 1x size of parent`).
     - `rem`: Relative to the root element's font size (e.g., `1rem = 1x root configuration`).
   - **Relative to Document/ViewPort**:
     - `vw`: Viewport width (e.g., `1vw = 1/100 x viewport width`).
     - `vh`: Viewport height (e.g., `1vh = 1/100 x viewport height`).

#### Quick Question:

- What is the difference between `1%` and `1vw`?

### Homework:

1. Style a tribute page using external CSS.
2. Create a card using CSS.

