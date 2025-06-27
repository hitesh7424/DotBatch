# 🖼️ CSS Image Gallery - Lecture Notes

In this session, we built a dynamic **Image Gallery** using HTML, CSS, and a little JavaScript magic to load image filenames from a `.txt` file.

---

## 🧱 HTML Structure Overview

```html
<div class="wrapper">
  <div class="container">
    <h1>My Gallery</h1>
    <div class="gallery"></div>
  </div>
</div>
```

### 📥 Dynamic Image Injection

We fetch the filenames from `images.txt` and generate image cards dynamically:

```js
fetch('images/images.txt')
  .then(response => response.text())
  .then(data => {
    const filenames = data.trim().split('\n').filter(Boolean);
    const gallery = document.querySelector(".gallery");

    filenames.forEach((filename) => {
      const figure = document.createElement("figure");
      figure.className = "card";

      const img = document.createElement("img");
      img.src = `images/${filename}`;
      img.alt = filename;

      const caption = document.createElement("figcaption");
      caption.textContent = filename.split('.')[0];

      figure.appendChild(img);
      figure.appendChild(caption);
      gallery.appendChild(figure);
    });
  })
  .catch(error => console.error('Error loading images.txt:', error));
```

---

## 🎨 CSS Concepts Covered

### ✅ Typography & Reset

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}
```

### ✅ Layout Styling

```css
.wrapper {
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow-x: hidden;
  overflow-y: auto;
}

.container {
  max-width: 1200px;
  padding: 20px;
  margin: 0 auto;
  height: 100%;
}
```

### ✅ Typography Styling

```css
.container h1 {
  font-size: 3rem;
  text-align: center;
  margin-bottom: 20px;
}
```

### ✅ Gallery Grid Layout

```css
.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.card {
  width: 32%;
  position: relative;
  border-radius: 10px;
  margin-bottom: 20px;
  overflow: hidden;
}
```

### ✅ Image Effects & Transitions

```css
.card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: grayscale(100%);
  box-shadow: 0 0 20px #333;
  transition: 0.3s;
}

.card:hover img {
  filter: grayscale(0%);
}
```

### ✅ Hover Animation

```css
.card:hover {
  transform: scale(1.03);
  filter: drop-shadow(0 0 10px #333);
  transition: 0.3s;
}
```

### ✅ Captions with Gradient

```css
.card figcaption {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  padding: 25px;
  font-size: 16px;
  font-weight: 500;
  color: #fff;
  opacity: 0;
  border-radius: 0 0 10px 10px;
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.5), transparent);
  transition: 0.3s;
}

.card:hover figcaption {
  opacity: 1;
  transform: scale(1.03);
}
```

---

## 💡 Concepts Demonstrated

| Feature                    | Explanation                            |
| -------------------------- | -------------------------------------- |
| `Flexbox`                  | Used to lay out and wrap image cards   |
| `overflow` control         | Prevents layout breaking               |
| `hover + transition`       | Smooth image zoom + caption fade-in    |
| `filter: grayscale()`      | Creates grayscale-to-color transition  |
| `object-fit: cover`        | Ensures images fill card area properly |
| `gradient backgrounds`     | Caption readability on images          |
| `box-shadow + drop-shadow` | Adds depth to UI elements              |
| `favicon` and `<title>`    | Proper webpage branding                |

---

## 📦 Image Loading via JS + `images.txt`

* Stores all image names inside a plain text file.
* Loads them dynamically into the HTML using JavaScript.
* Makes the gallery easily updatable without editing HTML.

---

## 🎓 Bonus Learning Points

* Using `.card:hover img` to selectively target image
* Using `figcaption` with `opacity + transition` to animate caption
* Clean separation of concerns between HTML, CSS, JS

---

## 🔥 What Makes This Cool?

* Full JS image injection using a text file
* Responsive layout without using any framework
* Smooth transitions, shadows, and grayscale filtering

> Your classmates are going to ask: "Bro this doesn't look like basic HTML/CSS... how??" 😎

---


