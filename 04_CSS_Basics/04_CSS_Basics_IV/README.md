# CSS Basics IV: Parallax & CSS Grid

---

## 🎯 Overview

In this session, we covered two major topics:

* **CSS Grid**: A powerful two-dimensional layout system.
* **Parallax Effect**: A visual scrolling technique to create depth.

---

## 🌐 CSS Grid

### ✅ What is CSS Grid?

> CSS Grid is a **two-dimensional** layout system that handles rows, columns, and gaps (gutters). It simplifies complex layout building and offers powerful line-based placement tools.

---

### 📏 Basic Terminology

* **Grid Container**: Element with `display: grid`
* **Grid Items**: Direct children of a grid container
* **Tracks**: Rows & columns
* **Gaps**: Spaces between tracks, also called gutters

---

### 🧰 Grid Container Properties

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 equal columns */
  grid-template-rows: repeat(4, 100px);  /* 4 rows of 100px each */
  gap: 10px; /* spacing between items */
}
```

You can use values like:

* `fr` (fractional unit)
* `px`, `%`, `auto`
* `repeat()`, `minmax()`

---

### 🧱 Grid Line Placement

Used to manually place items by referencing grid lines.

```css
#item1 {
  grid-column-start: 1;
  grid-column-end: 3;

  grid-row-start: 1;
  grid-row-end: 2;
}
```

#### 🔀 Shorthand

```css
#item1 {
  grid-column: 1 / 3;
  grid-row: 1 / 2;
}
```

---

### 📐 More Grid Properties

| Property          | Applies To     | Description                                         |
| ----------------- | -------------- | --------------------------------------------------- |
| `justify-content` | Grid Container | Aligns entire grid along the inline (row) axis      |
| `align-content`   | Grid Container | Aligns grid along block (column) axis               |
| `justify-items`   | Grid Container | Aligns items inside their cells (horizontally)      |
| `align-items`     | Grid Container | Aligns items inside their cells (vertically)        |
| `justify-self`    | Grid Item      | Aligns specific item inside its cell (horizontally) |
| `align-self`      | Grid Item      | Aligns specific item inside its cell (vertically)   |
| `place-items`     | Grid Container | Shorthand for `align-items` and `justify-items`     |
| `place-self`      | Grid Item      | Shorthand for `align-self` and `justify-self`       |

---

### 💡 Grid Example

```html
<div class="container">
  <div class="box" id="box1">Box 1</div>
  <div class="box" id="box2">Box 2</div>
  <div class="box" id="box3">Box 3</div>
  <div class="box" id="box4">Box 4</div>
  <div class="box" id="box5">Box 5</div>
</div>
```

```css
.container {
  display: grid;
  grid-template-columns: 150px 1fr 1fr 150px;
  grid-template-rows: 30px 1fr 30px;
  gap: 5px;
}

#box1, #box5 {
  grid-column: 1 / 5;
}

#box2, #box4 {
  grid-row: 2 / 3;
}

#box3 {
  grid-column: 2 / 4;
  grid-row: 2 / 3;
}
```

---

## 🌄 Parallax Effect in CSS

### 💬 What is Parallax?

> Parallax is a visual technique where background and foreground images move at different speeds to create depth illusion during scrolling.

---

### ✅ Key Properties Used

| Property          | Use                                             |
| ----------------- | ----------------------------------------------- |
| `perspective`     | Sets a 3D perspective depth                     |
| `transform-style` | Preserves 3D children                           |
| `translateZ()`    | Moves elements forward/backward in 3D space     |
| `scale()`         | Scales element to simulate depth                |
| `position: fixed` | Used in background layers to stay during scroll |

---

### 🧪 Parallax HTML + CSS Example

```html
<div id="wrapper">
  <div class="container">
    <img src="images/background.png" class="background">
    <img src="images/foreground.png" class="foreground">
    <h1>Adventure</h1>
  </div>
  <section>
    <h2>Adventure Time!</h2>
    <p class="text">Long descriptive content here...</p>
  </section>
</div>
```

```css
#wrapper {
  height: 100vh;
  width: 100vw;
  overflow-x: hidden;
  perspective: 10px;
}

.container {
  position: relative;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  transform-style: preserve-3d;
}

.background {
  transform: translateZ(-20px) scale(4);
}

.foreground {
  transform: translateZ(-10px) scale(2);
}

.background, .foreground {
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  z-index: -1;
}
```

---

## 📌 Homework

* Try `grid-row` and `grid-column` placements
* Build your own parallax section with different images and text

---