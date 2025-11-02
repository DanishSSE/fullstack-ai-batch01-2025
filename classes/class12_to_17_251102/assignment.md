# 📝 Bootstrap 5 Practice Assignment

**Assalam-O-Alaikum Students 👋**

**Assignment Given On:** 02 November 2025

> **Note:** Before starting your assignment, please **read and practice the class notes** carefully. Make sure you understand the concepts explained there — this will help you complete the task more easily.

## 🎯 Objective
The goal of this assignment is to help you **practice the basic concepts of Bootstrap 5**, including:
- Grid system & responsive design  
- Utility classes  
- Buttons, forms, and navbar  
- Cards and alerts  

---

## 📚 Instructions
1. Create a new project folder named **bootstrap-practice**.  
2. Inside it, create an **index.html** file.  
3. Add Bootstrap 5 using **CDN links** (CSS & JS).  
4. Complete the tasks below step by step.  
5. Once done, **open in your browser** and verify everything works correctly.

---

## 🧱 Task 1: Page Layout (Grid System)
Use the Bootstrap **12-column grid** to create the following layout:

| Row | Columns | Description |
|------|----------|-------------|
| 1 | 12 | Page Header (Centered title: “Bootstrap Practice Page”) |
| 2 | 4 - 4 - 4 | Three equal columns with background colors (`bg-primary`, `bg-warning`, `bg-success`) |
| 3 | 6 - 6 | Two columns: one for text, one for an image (use any placeholder image) |

💡 *Tip:* Use `.container`, `.row`, and `.col-md-` classes.

---

## 🎨 Task 2: Apply Utility Classes
Use Bootstrap utility classes to:
- Add margin and padding around elements (`.mt-4`, `.p-3`, etc.)
- Center text in your header using `.text-center`
- Add rounded borders and shadows to one of your columns (`.rounded`, `.shadow`)
- Change text color to `.text-white` in a colored background

---

## 🧭 Task 3: Create a Navbar
Create a **responsive navbar** using Bootstrap classes.

Navbar should include:
- Brand name: **MyBootstrapSite**
- Links: Home, About, Contact
- A toggle button that collapses on small screens

💡 *Hint:* Use `.navbar`, `.navbar-expand-lg`, `.navbar-light`, `.bg-light`, and `.collapse`.

---

## 🧾 Task 4: Add a Contact Form
Below the navbar, create a **Bootstrap form** with:
- Name (text input)
- Email (email input)
- Message (textarea)
- Submit button (`btn btn-primary`)

💡 *Bonus:* Wrap it in a card for a clean look!

---

## 🧍‍♀️ Task 5: Buttons & Alerts
Add a section below the form with three buttons:
```html
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Delete</button>
<button class="btn btn-outline-dark">Learn More</button>
```

When each button is clicked, show a corresponding **Bootstrap alert message**:
- Success → “Form submitted successfully!”
- Danger → “Are you sure you want to delete?”
- Outline → “More info coming soon!”

💡 *You can show/hide alerts manually for now (no JS needed).*

---

## 🪄 Task 6: Card Section (Portfolio)
Create a 3-column card section showing portfolio projects or services.

Each card should include:
- An image (use placeholder images)
- A title
- A short description
- A “Read More” button

💡 Use `.card`, `.card-body`, `.card-title`, `.card-text`, `.btn`.

---

## 📱 Task 7: Make It Responsive
Check your page on mobile view.  
Use Bootstrap’s **responsive column classes** (`col-sm-12`, `col-md-6`, `col-lg-4`) so that:
- Cards stack on mobile
- Columns adjust properly on tablet and desktop

---

## 🌟 Bonus Task (Optional)
Add **Bootstrap icons** beside the navbar links and buttons.  
Use the CDN:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
```

Example:
```html
<i class="bi bi-house-door"></i> Home
```

---

## ✅ Submission
- Save your project folder as **YourName_BootstrapAssignment.zip**
- Submit your zipped file to the instructor.

---

## 🧠 Tip
Refer to the official documentation whenever needed:  
🔗 [https://getbootstrap.com](https://getbootstrap.com)
