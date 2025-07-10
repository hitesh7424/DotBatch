### **HTML Basics 4: Key Topics and Questions**

#### **Key Topics**

1. **Links (Hyperlinks)**  
   - Anchor tag (`<a>`):  
     ```html
     <a href="https://facebook.com/">CLICK HERE</a>
     <a href="tel:+8130444444">CALL ME</a>
     <a href="mailto:support@example.com">MAIL ME</a>
     ```
   - Bookmark links:  
     ```html
     <a href="#resources">Go to Resources</a>  
     <div id="resources">This is the Resources Section</div>
     ```
     - To enable smooth scrolling:  
       ```css
       html {
           scroll-behavior: smooth;
       }
       ```

2. **Div vs Span**  
   - **Div tag**:  
     - A block-level generic container used for grouping elements.  
     - Renders content in separate lines.  
     - Example:  
       ```html
       <div>Block Element</div>
       <div>Another Block</div>
       ```
   - **Span tag**:  
     - An inline-level container for small portions of text or elements.  
     - Renders content in the same line unless styled differently.  
     - Example:  
       ```html
       <span>Inline Element</span>
       ```
   - Changing display properties:  
     - Div becomes inline with `display: inline;`  
     - Span becomes block with `display: block;`  

3. **Semantic Tags**  
   - **Definition**: Tags that give meaning to the content they wrap.  
     - Semantic: `<article>`, `<aside>`, `<figure>`, `<header>`, `<footer>`, `<main>`, `<nav>`, `<section>`  
     - Non-Semantic: `<div>`, `<span>`  
   - **Use Cases**:  
     - `<article>`: For independent content like blog posts.  
     - `<section>`: For grouping related content like chapters or topics.  
     - `<header>`: For page headers, brand logos, or introductory sections.  
     - `<footer>`: For footer content like copyright, terms, or contact info.  
     - `<nav>`: For navigation links.  
     - `<aside>`: For side content like ads, notes, or tips.  

4. **Favicon**  
   - Adding a favicon:  
     ```html
     <link rel="icon" type="image/x-icon" href="favicon.ico">
     ```

5. **Document Object Model (DOM)**  
   - Represents the structure of an HTML document as a tree, allowing manipulation of elements using JavaScript.

---

### **HTML Basics 4: Detailed Questions and Answers**

#### 1. **Q: What happens if we change the `display` property of a `<div>` to `inline` or a `<span>` to `block`?**  
   **A:**  
   - By default, a `<div>` is a block-level element, meaning it takes up the full width available and forces content to appear on a new line. When you change its `display` property to `inline`, it behaves like an inline element (such as `<span>`), aligning with other inline content on the same line.  
     Example:  
     ```html
     <div style="display: inline;">This is an inline div</div>
     <span>This is a span</span>
     ```
     Output: Both elements will appear side by side.  

   - Similarly, a `<span>` is an inline element that aligns with surrounding content. If you set `display: block;`, it behaves like a block element, taking up the full width and pushing the following content to the next line.  
     Example:  
     ```html
     <span style="display: block;">This is a block span</span>
     <div>This is a div</div>
     ```
     Output: Both elements will appear on separate lines.

   - However, changing the `display` property only alters their visual behavior, not their semantic meaning. A `<div>` remains a generic block container, and a `<span>` remains an inline container.

---

#### 2. **Q: Can a `<section>` tag be used inside an `<article>` tag or vice versa?**  
   **A:**  
   - Yes, a `<section>` tag can be used inside an `<article>` tag when you want to divide the content of the article into distinct sections. For instance, a news article might use `<section>` tags for an introduction, main story, and conclusion.  
     Example:  
     ```html
     <article>
       <section>
         <h2>Introduction</h2>
         <p>Welcome to our blog post.</p>
       </section>
       <section>
         <h2>Details</h2>
         <p>Here's the detailed content.</p>
       </section>
     </article>
     ```

   - Similarly, an `<article>` tag can be nested within a `<section>` if the content represents self-contained articles related to the section's theme.  
     Example:  
     ```html
     <section>
       <h1>Technology News</h1>
       <article>
         <h2>AI Breakthrough</h2>
         <p>Details about the latest AI advancements.</p>
       </article>
       <article>
         <h2>Space Exploration</h2>
         <p>Updates on recent space missions.</p>
       </article>
     </section>
     ```

---

#### 3. **Q: What is the difference between a `<p>`, `<article>`, and `<section>`?**  
   **A:**  
   - **`<p>` (Paragraph):** Used for a single paragraph of text. It is the most basic block of text content, intended for regular prose.  
     Example:  
     ```html
     <p>This is a single paragraph of text.</p>
     ```
     **Use Case:** For small, independent blocks of text.

   - **`<article>` (Independent Content):** Represents a self-contained piece of content that can stand on its own, like a blog post, news story, or forum post. An `<article>` can contain headings, paragraphs, and other nested tags.  
     Example:  
     ```html
     <article>
       <h1>Blog Title</h1>
       <p>This is an independent blog post.</p>
     </article>
     ```
     **Use Case:** For content that is independent and shareable.

   - **`<section>` (Thematic Grouping):** Represents a thematic grouping of related content, such as a chapter, a section of a report, or a part of a webpage. It organizes content hierarchically.  
     Example:  
     ```html
     <section>
       <h2>Chapter 1</h2>
       <p>This section covers Chapter 1.</p>
     </section>
     ```
     **Use Case:** For dividing content into meaningful sections within a document.

---

#### 4. **Q: Can a `<header>` tag be used inside a `<footer>` tag?**  
   **A:**  
   - Technically, yes. A `<header>` can be used inside a `<footer>` if you need to provide an introduction to the footer content. For example, you might include a heading or logo before listing footer links or legal disclaimers.  
     Example:  
     ```html
     <footer>
       <header>
         <h3>Quick Links</h3>
       </header>
       <p>Copyright © 2024</p>
     </footer>
     ```
   - However, this is an uncommon use case, as headers are typically used at the top of a page or section. It is better to use `<header>` within sections where appropriate meaning is conveyed.

---

#### 5. **Q: Can we use multiple `<header>` tags in a document?**  
   **A:**  
   - Yes, multiple `<header>` tags are valid and recommended for better semantics.  
     - **Main Page Header:** Use the `<header>` tag to define the top section of the webpage, which might include the site’s logo, navigation links, and a main heading.  
     - **Section-Specific Headers:** Use `<header>` tags inside `<section>` or `<article>` to provide headings specific to those content blocks.  
     Example:  
     ```html
     <header>
       <h1>Website Title</h1>
       <nav>Navigation Links</nav>
     </header>
     <section>
       <header>
         <h2>Section Title</h2>
       </header>
       <p>Content of the section.</p>
     </section>
     ```

---

#### 6. **Q: What is the difference between a `<body>` tag and a `<main>` tag?**  
   **A:**  
   - **`<body>`:** Represents the entire content of an HTML document that is visible on the webpage. It includes all sections, headers, footers, navigation bars, and main content.  
     Example:  
     ```html
     <body>
       <header>Header Content</header>
       <main>Main Content</main>
       <footer>Footer Content</footer>
     </body>
     ```

   - **`<main>`:** Represents the primary content of the webpage. It excludes repeated content like headers, navigation menus, and footers.  
     Example:  
     ```html
     <main>
       <h1>Welcome to Our Blog</h1>
       <p>This is the primary content of the page.</p>
     </main>
     ```
   - **Key Difference:** The `<body>` contains all content, whereas the `<main>` focuses on the core content that is unique to the page.