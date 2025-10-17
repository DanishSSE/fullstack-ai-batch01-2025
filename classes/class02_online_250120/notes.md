# Class 02 - January 20, 2025 (Online)

## HTML Forms & Semantic Tags

### Topics Covered

1. **HTML Forms**
   - Form structure and elements
   - Input types (text, email, password, etc.)
   - Labels and accessibility
   - Form validation attributes
   - Submit and reset buttons

2. **Advanced Semantic HTML**
   - Review of basic semantic tags
   - When to use specific semantic elements
   - Nesting semantic elements properly
   - Semantic HTML best practices

3. **HTML Attributes**
   - Global attributes (id, class, style)
   - Form-specific attributes
   - Data attributes
   - ARIA attributes (introduction)

### Key Concepts

#### Basic Form Structure
```html
<form action="/submit" method="POST">
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" minlength="8" required>

    <button type="submit">Submit</button>
</form>
```

#### HTML5 Input Types
- `text` - Single-line text input
- `email` - Email address input with validation
- `password` - Masked text input
- `number` - Numeric input
- `tel` - Telephone number
- `url` - URL input
- `date` - Date picker
- `time` - Time picker
- `color` - Color picker
- `file` - File upload
- `checkbox` - Checkbox
- `radio` - Radio button
- `range` - Slider
- `search` - Search field

#### Form Validation Attributes
- `required` - Field must be filled
- `minlength` / `maxlength` - Text length constraints
- `min` / `max` - Number range constraints
- `pattern` - Regular expression validation
- `placeholder` - Hint text
- `disabled` - Disable input
- `readonly` - Read-only field

### Semantic HTML Elements Deep Dive

#### Page Structure
```html
<header>
    <nav>
        <!-- Navigation links -->
    </nav>
</header>

<main>
    <article>
        <header>
            <h1>Article Title</h1>
        </header>
        <section>
            <!-- Article content -->
        </section>
    </article>

    <aside>
        <!-- Sidebar content -->
    </aside>
</main>

<footer>
    <!-- Footer content -->
</footer>
```

#### When to Use What
- **`<article>`**: Independent, self-contained content (blog post, news article)
- **`<section>`**: Thematic grouping of content with a heading
- **`<aside>`**: Tangentially related content (sidebar, callouts)
- **`<nav>`**: Major navigation blocks only
- **`<figure>` & `<figcaption>`**: Images with captions

### Accessibility Best Practices

1. Always use `<label>` with form inputs
2. Provide meaningful alt text for images
3. Use semantic HTML elements appropriately
4. Ensure proper heading hierarchy (h1 → h2 → h3)
5. Add ARIA labels when necessary

### Code Examples

See [code/](code/) folder for hands-on examples.

### Live Coding Session

During class, we built:
1. Contact form with validation
2. Registration form with various input types
3. Semantic blog post structure

### Resources

- [MDN Forms Guide](https://developer.mozilla.org/en-US/docs/Learn/Forms)
- [HTML5 Input Types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
- [Web Accessibility Initiative (WAI)](https://www.w3.org/WAI/)

### Common Questions from Class

**Q: What's the difference between `name` and `id` attributes?**
A: `id` is for CSS/JavaScript targeting (must be unique), `name` is for form data submission (can be duplicated for radio groups).

**Q: When should I use `<div>` vs semantic elements?**
A: Use semantic elements when the content has meaning (article, nav, header). Use `<div>` for pure layout/styling purposes.

**Q: Do I need to validate on both client and server?**
A: Yes! Client-side validation (HTML5 attributes) provides instant feedback, but server-side validation is essential for security.

### Homework

See [assignment.md](assignment.md) for details.

### Recording

Link available in [recording_link.txt](recording_link.txt)

### Next Class

- **Date**: January 24, 2025 (In-person)
- **Topic**: CSS Fundamentals, Selectors & Box Model
- **Prep**: Complete assignment and review CSS basics

---

*Class conducted by: [Instructor Name]*
*Class format: Online via Zoom*
