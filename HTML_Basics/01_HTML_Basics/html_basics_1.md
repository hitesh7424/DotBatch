
## HTML Basics - I  

### What is HTML?  
- **HTML**: **HyperText Markup Language**  
- It is the **skeleton of a webpage**.  
- **Markup**: Using annotations or tags to structure content.  

---

### Why is HTML Needed?  
- It is the **basic building block** of a website.  
- Describes the structure and content of a webpage.  
- Enables browsers to render web content (HTML document → Browser → Webpage).  
- Combined with **CSS** (appearance) and **JavaScript** (functionality), it forms a **Full-Stack Application**.

---

### HTML Tags  
- Tags tell the browser **how to render different elements**.  
- Tags have two main types:  
  1. **Opening tag**: `<h1>`  
  2. **Closing tag**: `</h1>`  
  - **Content**: Text or elements between the opening and closing tags.  

**Example**:  
```html
<h1>Namaste Duniya</h1>
```
- `<h1>`: Opening Tag  
- `Namaste Duniya`: Content  
- `</h1>`: Closing Tag  

---

### Types of HTML Elements  
#### 1. **Block Elements**:  
Take up the full width of their container.  
Examples:  
- `<p>` (Paragraph)  
- `<h1>` (Heading)  
- `<ul>` `<ol>` (Lists)  
- `<article>`  
- `<section>`  

#### 2. **Inline Elements**:  
Take up only as much width as necessary.  
Examples:  
- `<strong>`  
- `<a>` (Link)  
- `<em>`  

---

### Empty Tags (Self-Closing Tags)  
Do not require a closing tag.  
Examples:  
- `<br/>`  
- `<img/>`  
- `<input/>`  

---

### Lists in HTML  
1. **Ordered List**: Items with numbers or letters.  
   ```html
   <ol>
     <li>Item 1</li>
     <li>Item 2</li>
   </ol>
   ```
2. **Unordered List**: Items with bullets.  
   ```html
   <ul>
     <li>Item A</li>
     <li>Item B</li>
   </ul>
   ```
3. **Description List**: Describes terms or items.  
   ```html
   <dl>
     <dt>HTML</dt>
     <dd>HyperText Markup Language</dd>
   </dl>
   ```

---

### Attributes  
Attributes provide additional information about an element and are declared in the **opening tag**.  

#### Common Attributes:  
1. `src`: Used in `<img>` to specify the image source.  
2. `href`: Used in `<a>` to specify the link.  
3. `id`: Unique identifier for an element.  
4. `class`: Specifies a class for an element (used in CSS).  

**Example**:  
```html
<img src="tofu.jpeg" alt="Tofu" width="100" height="100">
<div id="Ramesh">This is a DIV tag</div>
```

---

### Special HTML Tags  
1. **`<!DOCTYPE html>`**: Declares the document as HTML5.  
2. **`<html>`**: Root tag of an HTML document.  
   - Example: `<html lang="en">` (Specifies the language of the document).  
3. **`<head>`**: Contains metadata, title, and links to external resources.  
   - Example:  
     ```html
     <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Document</title>
     </head>
     ```
4. **`<body>`**: Contains the visible content of the webpage.  

---

### Meta Tags  
Meta tags store **information about the website** (metadata).  
Examples:  
- `<meta charset="UTF-8">` (Specifies character encoding).  
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` (Responsive design).

---

### Useful Links  
1. [MDN Web Docs on HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)  
2. [W3Schools HTML Tutorial](https://www.w3schools.com/html/default.asp)  

---

### Homework  
- What happens when you close an empty tag?  

--- 

### Homework Answer:  

**What happens when you close an empty tag?**  

If you close an empty tag (e.g., `<br>`, `<img>`, `<input>`), it will have no negative effect in modern HTML.  

- **Valid Syntax**:  
  Empty tags can be written in two ways:  
  1. Without a closing slash:  
     ```html
     <br>
     <img src="image.jpg" alt="Image">
     ```  
  2. With a self-closing slash (optional in HTML5):  
     ```html
     <br/>
     <img src="image.jpg" alt="Image"/>
     ```  

- **Impact**:  
  Browsers interpret both styles the same way. The closing slash (`/`) is optional in HTML5 but required in older XHTML documents.  

### Conclusion:  
Closing an empty tag will not cause errors, but it is unnecessary in HTML5.