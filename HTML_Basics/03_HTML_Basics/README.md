### **HTML Basics Part 3**

---

### **Topics Covered**

#### **1. Table Basics**
- Tables are created using `<table>`, `<tr>` (table row), `<td>` (table data), and `<th>` (table header) tags.
- Styling tables:
  ```css
  table, tr, td, th {
    border: 1px solid black;
    text-align: center;
    border-collapse: collapse;
  }
  ```

#### **2. Table Attributes**
- **`colspan`**: Combines multiple columns into one.
  ```html
  <td colspan="2">Spans 2 Columns</td>
  ```

- **`rowspan`**: Combines multiple rows into one.
  ```html
  <td rowspan="2">Spans 2 Rows</td>
  ```

#### **3. Table Groups**
- **`<colgroup>`**: Defines column-specific styles.
  ```html
  <colgroup>
    <col style="background-color: yellow;" />
    <col style="visibility: collapse;" />
  </colgroup>
  ```

- **`rowgroup`**: Concept for logical grouping of rows (achieved using `<thead>`, `<tbody>`, `<tfoot>`).

---

### **Examples**

#### **1. Basic Table with `colspan` and `rowspan`**
```html
<table>
  <tr>
    <th colspan="2">Month</th>
    <td>Other Data</td>
  </tr>
  <tr>
    <th>Jan</th>
    <td colspan="2" rowspan="2">100</td>
  </tr>
  <tr>
    <th rowspan="2">Feb</th>
    <td>200</td>
  </tr>
  <tr>
    <td>300</td>
  </tr>
</table>
```

#### **2. Table with `colgroup`**
```html
<table>
  <colgroup>
    <col style="background-color: green;" />
    <col style="background-color: red;" />
    <col style="visibility: collapse;" />
  </colgroup>
  <tr>
    <td>Column 1</td>
    <td>Column 2</td>
    <td>Column 3</td>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
    <td>Data 3</td>
  </tr>
</table>
```

---

### **Upcoming Topics**
- **Links**: Hyperlinks, anchor tags, and attributes like `href`, `target`.
- **Forms in Detail**: Advanced input types, validation, and form attributes.
- **Semantic Tags**: Meaningful elements like `<header>`, `<footer>`, `<article>`, `<section>`, etc.

--- 

