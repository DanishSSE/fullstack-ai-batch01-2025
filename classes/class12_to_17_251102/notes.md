# 🧭 Bootstrap 5 – Basic Notes

## 🧩 1. What is Bootstrap?
**Bootstrap** is a **CSS framework** that helps you build **responsive** and **mobile-friendly** websites quickly.  
It includes ready-made:
- CSS classes (for design)
- JavaScript components (for interactivity)
- Grid system (for layout)

✅ **Key point:** You can build professional websites without writing CSS from scratch!

---

## ⚙️ 2. How to Add Bootstrap

There are **two ways** to include Bootstrap in your project:

### A. Using CDN (Recommended for Beginners)
Add this inside your HTML `<head>` tag:
```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
```

And before closing `</body>` tag:
```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
```

### B. Using Local Files
Download Bootstrap → Link the CSS and JS files from your project folder.

---

## 🧱 3. Bootstrap Layout – The Grid System

Bootstrap uses a **12-column grid system** to arrange content.

Example layout:
```html
<div class="container">
  <div class="row">
    <div class="col-6">Half Width</div>
    <div class="col-6">Half Width</div>
  </div>
</div>
```

### Key Classes:
| Class | Meaning |
|-------|----------|
| `.container` | Centers and gives padding to your layout |
| `.row` | Creates a horizontal group (row) |
| `.col` | Creates a column inside the row |
| `.col-4` / `.col-8` | Defines how many columns to take (out of 12) |

---

## 📱 4. Responsive Design

Bootstrap has **breakpoints** to make websites work on all devices.

| Device Size | Class Prefix | Example |
|--------------|---------------|----------|
| Extra Small (phones) | none | `.col-12` |
| Small (≥576px) | `sm` | `.col-sm-6` |
| Medium (≥768px) | `md` | `.col-md-4` |
| Large (≥992px) | `lg` | `.col-lg-3` |
| Extra Large (≥1200px) | `xl` | `.col-xl-2` |

💡 Example:
```html
<div class="col-12 col-md-6 col-lg-4">Responsive Column</div>
```
→ Full width on mobile, half on tablet, one-third on desktop.

---

## 🎨 5. Common Utility Classes

Bootstrap provides **ready CSS classes** to style things fast.

| Purpose | Class Examples |
|----------|----------------|
| Text color | `.text-primary`, `.text-danger` |
| Background color | `.bg-success`, `.bg-light` |
| Spacing (Margin/Padding) | `.m-3`, `.p-2`, `.mt-5`, `.px-4` |
| Text alignment | `.text-center`, `.text-start`, `.text-end` |
| Display | `.d-block`, `.d-flex`, `.d-none` |
| Border | `.border`, `.border-0`, `.rounded`, `.rounded-circle` |

---

## 🧍‍♀️ 6. Buttons

Bootstrap buttons come in various colors and styles:
```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
<button class="btn btn-outline-dark">Outline</button>
```

You can also change size:
```html
<button class="btn btn-primary btn-lg">Large</button>
<button class="btn btn-primary btn-sm">Small</button>
```

---

## 🧾 7. Forms

Bootstrap makes form design neat and consistent:
```html
<form>
  <div class="mb-3">
    <label class="form-label">Email address</label>
    <input type="email" class="form-control" placeholder="Enter email">
  </div>
  <div class="mb-3">
    <label class="form-label">Password</label>
    <input type="password" class="form-control">
  </div>
  <button class="btn btn-primary">Submit</button>
</form>
```

---

## 🧭 8. Navigation Bar (Navbar)

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container">
    <a class="navbar-brand" href="#">BrandName</a>
    <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#menu">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="menu">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About</a></li>
      </ul>
    </div>
  </div>
</nav>
```

---

## 🪄 9. Cards

Cards are used to show info neatly:
```html
<div class="card" style="width: 18rem;">
  <img src="image.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card Title</h5>
    <p class="card-text">Some description text.</p>
    <a href="#" class="btn btn-primary">Read More</a>
  </div>
</div>
```

---

## 🎚️ 10. Alerts

Used to show messages:
```html
<div class="alert alert-success">Success! Your form was submitted.</div>
<div class="alert alert-danger">Error! Please try again.</div>
```

---

## 🧠 11. Bootstrap Icons

You can use free icons with:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
```

Example:
```html
<i class="bi bi-alarm"></i>
<i class="bi bi-heart-fill text-danger"></i>
```

---

## 🪄 12. Helpful Tips

- Always use `.container` to wrap content.
- Use **responsive classes** (`col-md-`, `col-lg-`) to control layout on different devices.
- Combine utility classes to save time instead of writing custom CSS.
- Explore Bootstrap documentation: [https://getbootstrap.com](https://getbootstrap.com)
