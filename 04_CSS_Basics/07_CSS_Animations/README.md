# CSS Advanced: Variables, Transitions, and Animations

Welcome to the deep dive into advanced CSS features. This document includes:

* CSS Variables (Global and Local)
* Transitions
* Animations with Keyframes
* Function usage in CSS
* Multiple real-world examples including your **"Hire Me" button** and **animated boxes**

---

## 1. CSS Variables

### What Are CSS Variables?

CSS Variables (a.k.a. custom properties) allow you to reuse values across your stylesheets with ease.

### Syntax

```css
:root {
  --primary-color: #981a2c;
  --secondary-color: aqua;
}

.box {
  background-color: var(--primary-color);
  color: var(--secondary-color);
}
```

### Global vs Local Variables

* **Global Variables**: Declared in `:root`, accessible anywhere.
* **Local Variables**: Declared inside a selector, accessible only within that scope.

```css
.box {
  --box-color: green;
  color: var(--box-color);
}
```

### Example in Your Project

```css
:root {
    --dark-red: #981a2c;
}

.container {
    background-color: var(--dark-red);
}

.box {
    color: var(--dark-red); /* local variable also defined here */
}
```

---

## 2. Transitions

### What Are Transitions?

Transitions allow CSS property changes to occur smoothly over time.

### Syntax

```css
transition: property duration timing-function delay;
```

### Example 1: Rotating Box

```css
.box {
  transition: transform 3s ease 1s;
}

.box:hover {
  transform: translateX(500px) rotate(360deg) scale(3);
}
```

### Example 2: Button Hover Effect

```css
.btn-pink {
  position: relative;
  z-index: 1;
  background-color: #e84949;
  color: white;
  transition: all 0.8s;
}

.btn-pink::before {
  content: "";
  background-color: #1f1f1f;
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  transform: scaleX(0);
  transform-origin: left;
  transition: all 0.8s;
  z-index: -1;
}

.btn-pink:hover::before {
  transform: scaleX(1);
}
```

---

## 3. Animations with Keyframes

### Animation Syntax

```css
.box {
  animation-name: exampleAnim;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-delay: 1s;
  animation-timing-function: ease-in;
  animation-direction: alternate;
  animation-fill-mode: both;
}

@keyframes exampleAnim {
  0%   { width: 200px; background-color: orange; }
  50%  { width: 50%; background-color: white; }
  100% { width: 100%; background-color: green; }
}
```

### Example 1: Expanding Box

```css
@keyframes hitesh {
  0% { width: 212px; background-color: orange; }
  50% { width: 50%; background-color: white; }
  100% { width: 100%; background-color: green; }
}

.box {
  animation-name: hitesh;
  animation-duration: 2s;
  animation-fill-mode: both;
  animation-delay: 1s;
  animation-timing-function: linear;
}
```

---

## 4. CSS Functions

### Common Functions

* `calc()`: Perform calculations
* `min()` / `max()`: Return the smallest/largest value
* `minmax()`: Used with grids
* `url()`: Link images/fonts
* `rgb()` / `rgba()` / `hsl()`
* `scale()`, `rotate()`, `translate()` for transforms

### Example

```css
.container {
  width: calc(100% - 50px);
  grid-template-rows: repeat(3, minmax(100px, auto));
}
```

---

## 5. Assignment: "Hire Me" Button

### Requirements Fulfilled:

* Button centered in screen
* Color background with text shadow
* On hover, background color slides in
* Uses transition for smooth effect

### Final Code

```html
<div class="wrapper">
  <button class="btn-pink">Hire Me</button>
</div>
```

```css
.btn-pink {
  background-color: #e84949;
  color: white;
  padding: 0.8rem 2.3rem;
  position: relative;
  z-index: 1;
  overflow: hidden;
  border: none;
}

.btn-pink::before {
  content: "";
  background-color: #1f1f1f;
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.8s ease;
  z-index: -1;
}

.btn-pink:hover::before {
  transform: scaleX(1);
}
```

---

## Summary

* Use **variables** to maintain consistent design
* Use **transitions** to animate CSS property changes
* Use **keyframes** for complex animations
* Combine all to create smooth, responsive UI elements


