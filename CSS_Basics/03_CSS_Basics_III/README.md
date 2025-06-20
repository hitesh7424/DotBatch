# CSS Flexbox – The Complete Guide 💡

## 🧠 What is Flexbox?

Flexbox (Flexible Box Layout) is a **one-dimensional** layout model in CSS. It helps efficiently:
- Distribute space within a container
- Align items along a main or cross axis
- Adapt layouts to different screen sizes

> It works either **horizontally (row)** or **vertically (column)** — but not both at once.

---

## 📦 Key Terminology

| Term           | Meaning                                           |
|----------------|----------------------------------------------------|
| Flex Container | The parent element with `display: flex`           |
| Flex Items     | The direct children of the flex container          |
| Main Axis      | The primary layout direction (horizontal by default) |
| Cross Axis     | Perpendicular to the main axis                    |

---

## 🔧 Flex Container Properties

### `display: flex;`

```css
.container {
  display: flex;
}
````

Makes the element a flex container.

---

### `flex-direction`

Controls the **main axis** direction (row or column).

```css
.container {
  flex-direction: row; /* default */
  /* row-reverse | column | column-reverse */
}
```

---

### `flex-wrap`

Controls whether items **wrap** to the next line.

```css
.container {
  flex-wrap: wrap;
  /* nowrap | wrap-reverse */
}
```

---

### `flex-flow`

A shorthand for `flex-direction` + `flex-wrap`.

```css
.container {
  flex-flow: row wrap;
}
```

---

### `justify-content`

Aligns items **on the main axis**.

```css
.container {
  justify-content: center;
  /* flex-start | flex-end | space-between | space-around | space-evenly */
}
```

---

### `align-items`

Aligns items **on the cross axis**.

```css
.container {
  align-items: center;
  /* flex-start | flex-end | stretch | baseline */
}
```

---

### `align-content`

Aligns **multiple lines** (if wrapping) on the cross axis.

```css
.container {
  align-content: space-between;
  /* flex-start | flex-end | center | space-around | space-evenly */
}
```

---

### `gap`, `row-gap`, `column-gap`

Adds spacing between items.

```css
.container {
  gap: 10px;
  row-gap: 20px;
  column-gap: 30px;
}
```

---

## 🔩 Flex Item Properties

### `order`

Changes the **visual order** of items.

```css
.item {
  order: 2; /* default is 0 */
}
```

---

### `flex-grow`

Controls how much an item **grows** relative to siblings.

```css
.item {
  flex-grow: 1; /* takes available space */
}
```

---

### `flex-shrink`

Controls how much an item **shrinks** when needed.

```css
.item {
  flex-shrink: 2;
}
```

---

### `flex-basis`

Sets the **initial size** of an item before growing or shrinking.

```css
.item {
  flex-basis: 150px;
}
```

---

### `flex` (shorthand)

Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.

```css
.item {
  flex: 1 1 150px;
  /* grow:1, shrink:1, basis:150px */
}
```

---

### `align-self`

Overrides `align-items` for one specific item.

```css
.item {
  align-self: flex-end;
  /* flex-start | flex-end | center | stretch | baseline */
}
```



## 💎 Summary Table

| Property          | Applies To | Purpose                               |
| ----------------- | ---------- | ------------------------------------- |
| `display: flex`   | Container  | Enable Flexbox                        |
| `flex-direction`  | Container  | Main axis direction                   |
| `flex-wrap`       | Container  | Wrapping behavior                     |
| `justify-content` | Container  | Align on main axis                    |
| `align-items`     | Container  | Align on cross axis                   |
| `align-content`   | Container  | Align multi-line flex lines           |
| `flex-grow`       | Item       | Grow ratio                            |
| `flex-shrink`     | Item       | Shrink ratio                          |
| `flex-basis`      | Item       | Initial size before flexing           |
| `order`           | Item       | Visual order of the item              |
| `align-self`      | Item       | Item-specific alignment on cross axis |

---

