
## HTML Basics Part 2



### **Recap from Last Class**
- **HTML**: Defines the structure of a webpage.
- **Tags**: Used to mark up content.
- **Text Elements**: Block-level and Inline-level.
- **Attributes**: Provide additional information for elements.
- **Lists**: Ordered, unordered, and description lists.

---

### **Topics Covered Today**

#### **1. Shortcut in VS Code**
- Typing `!` and pressing `Enter` in VS Code generates a basic HTML boilerplate.

#### **2. Horizontal Rule (`<hr>` Tag)**
- Used to create a horizontal line for separating content.
- Example:
  ```html
  <hr color="blue" />
  ```

---

#### **3. Special Tags**
- **Preformatted Text (`<pre>`)**:  
  Displays text as written, preserving spaces and line breaks.
  ```html
  <pre>
  Line 1
      Line 2
  </pre>
  ```

- **Quotation and Citation Tags**:
  - `<blockquote>`: For large quotes (block-level).  
  - `<q>`: For inline quotes.  
  - `<cite>`: To cite a work.  
  - `<address>`: For contact information.

---

#### **4. Nested Lists**
- Lists can contain other lists inside them.
  ```html
  <ul>
    <li>Item 1</li>
    <li>Item 2
      <ol>
        <li>Sub-item 1</li>
        <li>Sub-item 2</li>
      </ol>
    </li>
  </ul>
  ```

---

#### **5. Tables**
- Structure:  
  ```html
  <table>
    <caption>Table Title</caption>
    <thead>
      <tr>
        <th>Heading 1</th>
        <th>Heading 2</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Data 1</td>
        <td>Data 2</td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td>Total</td>
        <td>100</td>
      </tr>
    </tfoot>
  </table>
  ```

- **Attributes**:
  - `rowspan` and `colspan` for merging cells.
  - `border-collapse` for collapsing cell borders.

---

#### **6. Forms**
- Used for user input.
- **Common Elements**:
  - `<input>`: For text, passwords, radio buttons, checkboxes.
  - `<textarea>`: For multi-line text input.
  - `<select>`: Dropdown menu.

- Example:
  ```html
  <form action="submit_url">
    <label for="username">Username: </label>
    <input type="text" id="username" />
    <label for="password">Password: </label>
    <input type="password" id="password" />
    <input type="submit" value="Login" />
  </form>
  ```

---

### **Homework Questions**

#### 1. **Why does the heading tag only go from `<h1>` to `<h6>` and not `<h7>` or beyond?**
   - HTML specifications were designed to allow six levels of headings for optimal organization and readability. Additional heading levels are unnecessary for most practical use cases.

#### 2. **Simple Webpage Homework**
   - URL: [Codehelp Tribute Webpage](https://codehelp-linus-torvalds-tribute.netlify.app/)

#### 3. **What happens when we close an empty tag?**
   - Closing an empty tag is optional in HTML5. Browsers handle it correctly either way.

---

### **Examples and Practices**

#### **Formatting Text**
```html
<p><b>Bold Text</b></p>
<p><i>Italic Text</i></p>
<p><u>Underlined Text</u></p>
<p><del>Deleted Text</del></p>
<p>Superscript: x<sup>2</sup></p>
<p>Subscript: a<sub>1</sub></p>
```

#### **Table Example**
```html
<table>
  <caption>Sample Table</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>24</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>30</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">End of Table</td>
    </tr>
  </tfoot>
</table>
```

#### **Form Example**
```html
<form>
  <label for="email">Email:</label>
  <input type="email" id="email" />
  <label for="password">Password:</label>
  <input type="password" id="password" />
  <button type="submit">Submit</button>
</form>
```

