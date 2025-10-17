# 🧠 HTML & CSS Basics — Beginner Notes

**Online Class Date:** 16 October 2025

## 🌐 1. What is HTML and CSS?

- **HTML (HyperText Markup Language):**
  Used to **structure** the content of a webpage.
  Example: Headings, paragraphs, images, buttons, etc.

- **CSS (Cascading Style Sheets):**
  Used to **style** the HTML content — controls colors, layout, fonts, and spacing.

---

## 🧩 2. Understanding HTML Attributes

HTML **attributes** provide **extra information** about elements.
They are always written **inside the opening tag**.

**Example:**

```html
<p title="This is a tooltip">Hello World!</p>
```

### Common HTML Attributes:

| Attribute     | Purpose                                       | Example                                 |
| ------------- | --------------------------------------------- | --------------------------------------- |
| `class`       | Used to group elements for CSS styling        | `<div class="card">`                    |
| `id`          | Used to uniquely identify a single element    | `<h1 id="main-heading">`                |
| `name`        | Used mostly in forms to identify input fields | `<input name="email">`                  |
| `type`        | Defines the type of input                     | `<input type="password">`               |
| `placeholder` | Adds hint text in form fields                 | `<input placeholder="Enter your name">` |
| `value`       | Defines default value in form input           | `<input value="Danish">`                |

---

## 🏷️ 3. The `class` and `id` Attributes

### 🟢 `class` Attribute

- Used to **apply the same CSS style** to **multiple elements**.
- You can have **many elements with the same class**.

**Example:**

```html
<p class="info">This is an info text.</p>
<p class="info">This is another info text.</p>
```

**CSS:**

```css
.info {
  color: blue;
  font-size: 18px;
}
```

✅ Both paragraphs will be blue and 18px.

---

### 🔵 `id` Attribute

- Used to **uniquely identify** one element.
- You can have **only one element per id** on a page.

**Example:**

```html
<h1 id="main-title">Welcome to CSS Learning</h1>
```

**CSS:**

```css
#main-title {
  color: green;
  text-align: center;
}
```

✅ Only that heading will be styled green.

---

## 🧾 4. Basic CSS Syntax

CSS uses **selectors** to target HTML elements and **properties** to style them.

**Syntax:**

```css
selector {
  property: value;
}
```

**Example:**

```css
p {
  color: red;
  font-size: 16px;
}
```

This styles all `<p>` (paragraph) tags.

---

## 🎨 5. Types of CSS

| Type             | Where it’s written               | Example                                    |
| ---------------- | -------------------------------- | ------------------------------------------ |
| **Inline CSS**   | Inside the HTML tag              | `<p style="color: red;">Text</p>`          |
| **Internal CSS** | Inside `<style>` tag in `<head>` | `<style>p { color: blue; }</style>`        |
| **External CSS** | In a separate `.css` file        | `<link rel="stylesheet" href="style.css">` |

✅ **External CSS** is best practice — easier to maintain and reuse.

---

## 🧱 6. CSS Selectors (Basic)

| Selector     | Targets                   | Example                         |
| ------------ | ------------------------- | ------------------------------- |
| `p`          | All `<p>` tags            | `p { color: red; }`             |
| `.className` | All elements with a class | `.info { color: blue; }`        |
| `#idName`    | One specific element      | `#header { background: gray; }` |
| `div p`      | Paragraphs inside div     | `div p { font-size: 14px; }`    |
| `*`          | All elements              | `* { margin: 0; }`              |

---

## 🧰 7. Common CSS Properties

| Property           | Description            | Example                     |
| ------------------ | ---------------------- | --------------------------- |
| `color`            | Text color             | `color: red;`               |
| `background-color` | Element background     | `background-color: yellow;` |
| `font-size`        | Size of text           | `font-size: 18px;`          |
| `font-weight`      | Boldness of text       | `font-weight: bold;`        |
| `text-align`       | Align text             | `text-align: center;`       |
| `margin`           | Space outside element  | `margin: 20px;`             |
| `padding`          | Space inside element   | `padding: 10px;`            |
| `border`           | Outline around element | `border: 1px solid black;`  |

---

## 🧮 8. Understanding Box Model

Every element in CSS is a **box** made up of:

```
Margin → Border → Padding → Content
```

**Example:**

```css
div {
  margin: 10px;
  border: 2px solid black;
  padding: 15px;
}
```

---

## 📝 9. Basic Form Attributes Recap

| Attribute     | Purpose                      | Example                                              |
| ------------- | ---------------------------- | ---------------------------------------------------- |
| `type`        | Input type                   | `<input type="email">`                               |
| `name`        | Identifies input for backend | `<input name="user_email">`                          |
| `placeholder` | Shows hint text              | `<input placeholder="Enter your email">`             |
| `value`       | Default value                | `<input value="Danish">`                             |
| `required`    | Makes field mandatory        | `<input required>`                                   |
| `id` + `for`  | Link label with input        | `<label for="email">Email</label><input id="email">` |

---

## 💡 10. Tips for Beginners

1. Always link your CSS file correctly:
   ```html
   <link rel="stylesheet" href="style.css" />
   ```
2. Use **classes** for groups and **IDs** for unique elements.
3. Keep your code clean and **properly indented**.
4. Use comments in CSS:
   ```css
   /* This styles the main heading */
   ```
5. Learn by experimenting — change colors, margins, and spacing.
