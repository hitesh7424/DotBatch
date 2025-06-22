# 🛍️ Product Card - Homework Breakdown

This is a detailed breakdown and explanation of the **Product Card** I created as part of my CSS homework. The goal was to build a clean, responsive UI component that mimics a modern e-commerce product card.

---

## 🧱 HTML Structure

```html
<div class="wrapper">
  <div class="container">
    <img class="image" src="mug.png" alt="Coffee Mug">
    <div class="text">
      <p class="product">Coffee Mug</p>
      <p class="product_title">White Coffee Mug</p>
      <p class="description">Coffee Mugs are designed to express emotions...</p>
      <p class="price">
        <span class="price_new green-text">₹149</span>
        <span class="price_old green-text strike">₹230</span>
      </p>
      <button class="btn">
        <img class="btn-img" src="https://bit.ly/3Q6Adni" alt="Cart">
        <span class="btn_text description">Add to Cart</span>
      </button>
    </div>
  </div>
</div>
```

### ✅ Key Elements:

* **`.wrapper`**: Outer flex container to center the card on the page.
* **`.container`**: Actual card — holds image + text content.
* **`.image`**: Displays the product image.
* **`.text`**: Contains title, description, pricing, and button.

---

## 🎨 CSS Concepts Used

### 1. **CSS Variables** (`:root`)

```css
:root {
  --darkGreen: hsl(158, 36%, 37%);
  --cream: hsl(30, 38%, 92%);
  --gray: hsl(228, 12%, 48%);
  --white: hsl(0, 0%, 100%);
  --head: 2rem;
  --text: 1rem;
}
```

Used to manage colors and font sizes efficiently for a consistent theme.

---

### 2. **Centering with Flexbox**

```css
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: var(--cream);
}
```

This makes sure the product card is **centered both vertically and horizontally**.

---

### 3. **Card Design (`.container`)**

```css
.container {
  display: flex;
  background-color: var(--white);
  border-radius: 1.5em;
  overflow: hidden;
  max-width: 700px;
}
```

The card uses:

* **Flexbox** for layout
* **Rounded corners**
* **Overflow hidden** to clip image edges neatly

---

### 4. **Typography**

* **Google Fonts** used: `Fraunces`, `Montserrat`, and `Poppins`
* Semantic hierarchy:

  * `.product` is uppercase and spaced out
  * `.product_title` uses serif font with a larger size
  * `.description` uses a sans-serif for readability

---

### 5. **Responsive Pricing**

```css
.price_new {
  font-family: "Fraunces", serif;
  font-size: var(--head);
}

.price_old {
  font-size: var(--text);
  text-decoration: line-through;
  margin-left: 1rem;
}
```

Shows discounted pricing effectively:

* Current price in bold green
* Old price struck through

---

### 6. **Add to Cart Button**

```css
.btn {
  background-color: var(--darkGreen);
  color: var(--white);
  border-radius: 0.7em;
  padding: 1em;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
```

* Button is full-width, styled for modern look
* Contains an image and text inline

---

## 🔍 Highlights

| Feature             | Explanation                                |
| ------------------- | ------------------------------------------ |
| `Flexbox`           | Used to center and layout card and content |
| `CSS Variables`     | Easy theme control and readability         |
| `Google Fonts`      | Professional-looking typography            |
| `Button Design`     | Styled with image + text                   |
| `Strike Price`      | Indicates old price visually               |
| `Responsive Widths` | Makes card visually balanced               |

---

## 💥 Showoff Points

* ✨ Used **3 fonts** in perfect harmony
* 🎯 Layout done fully with **Flexbox**
* 🎨 Colors managed with **CSS variables**
* 🧠 Typography hierarchy built with **semantic intent**
* 🛒 Responsive button includes image + text


