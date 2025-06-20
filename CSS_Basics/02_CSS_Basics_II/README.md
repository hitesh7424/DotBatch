
# 🌐 CSS Basics 02: A Bit More Advanced

### Topics Covered:

* Gradients
* Shadows
* Dimensions
* Positioning
* 2D & 3D Transforms
* Flexbox *(To be added separately)*

---

## 🎨 CSS Gradient Types

Gradients allow smooth transitions between colors.

1. **Linear Gradients**

   * Direction-based: top to bottom, left to right, or diagonally.
   * Example:

     ```css
     background: linear-gradient(to right, red, blue);
     ```

2. **Radial Gradients**

   * Radiate from the center or any defined point.
   * Example:

     ```css
     background: radial-gradient(circle, red, yellow, green);
     ```

3. **Conic Gradients**

   * Rotated around a center point.
   * Example:

     ```css
     background: conic-gradient(from 0deg, red, yellow, green, red);
     ```

---

## 🌟 CSS Shadow Effects

### 1. **Text Shadow**

* Used for adding shadow to text.
* Syntax:

  ```css
  text-shadow: h-offset v-offset blur color;
  ```
* Features:

  * Horizontal & vertical offset
  * Blur radius
  * Color support
  * Multiple shadows supported (comma-separated)

💡 **Can we create a border using shadows?**
Yes! By stacking multiple shadows creatively:

```css
text-shadow: 
  1px 1px 0 black,
 -1px 1px 0 black,
 -1px -1px 0 black,
  1px -1px 0 black;
```

---

### 2. **Box Shadow**

* Applies shadow to boxes (divs, cards, etc.)
* Syntax:

  ```css
  box-shadow: h-offset v-offset blur spread color;
  ```
* Features:

  * Default shadow color is text color (unless overridden)
  * Supports blur and spread radius
  * Multiple shadows with comma
  * Example:

    ```css
    box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.3);
    ```

---

## 📐 CSS Dimensions

Control the sizing of elements.

* `width`, `height`
* `min-width`, `min-height`
* `max-width`, `max-height`

**Example:**

```css
div {
  width: 100px;
  min-height: 200px;
  max-width: 300px;
}
```

**Overflow Example:**

```css
overflow: scroll;
```

---

## 📍 CSS Positioning

Defines how elements are placed in the document flow.

### 1. **static** (default)

* Normal flow (no positioning).

### 2. **relative**

* Positioned *relative to its normal position*.
* Supports `top`, `right`, `bottom`, `left`.

### 3. **absolute**

* Positioned *relative to the nearest positioned ancestor*.
* If no positioned ancestor, it falls back to `body`.
* Moves with scroll.

### 4. **fixed**

* Positioned relative to the *viewport*.
* Doesn't move when scrolling.

### 5. **sticky**

* Toggles between `relative` and `fixed` based on scroll.
* Example:

  ```css
  position: sticky;
  top: 0;
  ```

---

## 🔄 CSS 2D Transforms

Used to move, rotate, scale, and skew elements in 2D space.

**Properties:**

* `translate(x, y)`
* `rotate(deg)`
* `scaleX(n)` / `scaleY(n)` / `scale(n)`
* `skewX(deg)` / `skewY(deg)` / `skew(x, y)`
* `matrix(a, b, c, d, e, f)`

### 💡 `transform: matrix(a, b, c, d, e, f)`

* Combines multiple transforms into one.
* Matrix breakdown:

  ```
  | a  c  e |
  | b  d  f |
  | 0  0  1 |
  ```

  * a = scaleX
  * b = skewY
  * c = skewX
  * d = scaleY
  * e = translateX
  * f = translateY

**Example:**

```css
transform: matrix(1, 0.2, 0.3, 1, 50, 100);
```

---

## 🧊 CSS 3D Transforms

Adds depth to the 2D world — simulates Z-axis!

**Common Properties:**

* `rotateX(deg)`
* `rotateY(deg)`
* `rotateZ(deg)`
* `perspective(n)`
* `translateZ(n)`
* `scaleZ(n)`
* `transform-style: preserve-3d;`

**Example:**

```css
transform: rotateY(45deg);
```

---

## 🧪 Exercise Time:

**Task:**
Position text in all corners and center of an image using `position: absolute`.

**Hint HTML:**

```html
<div class="container">
  <img src="image.jpg" />
  <div class="top-left">Top Left</div>
  <div class="top-right">Top Right</div>
  <div class="bottom-left">Bottom Left</div>
  <div class="bottom-right">Bottom Right</div>
  <div class="center">Center</div>
</div>
```

**Hint CSS:**

```css
.container {
  position: relative;
}

.container div {
  position: absolute;
  color: white;
}

.top-left { top: 0; left: 0; }
.top-right { top: 0; right: 0; }
.bottom-left { bottom: 0; left: 0; }
.bottom-right { bottom: 0; right: 0; }
.center {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

---