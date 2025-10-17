# Assignment 02 - Contact Form & Semantic Blog Page

## Due Date
Sunday, January 26, 2025 at 11:59 PM

## Objective
Create two separate HTML pages demonstrating understanding of HTML forms and semantic HTML structure.

## Part 1: Contact Form (50 points)

### Requirements

Create a file named `contact.html` with a comprehensive contact form.

#### Form Must Include:
- [ ] Full name input (required)
- [ ] Email address input with email validation (required)
- [ ] Phone number input (optional)
- [ ] Subject dropdown/select menu with at least 3 options
- [ ] Message textarea (required, minimum 10 characters)
- [ ] Preferred contact method (radio buttons: Email, Phone, Either)
- [ ] Newsletter subscription checkbox
- [ ] Submit button
- [ ] Reset button

#### Additional Requirements:
- [ ] All inputs must have associated labels
- [ ] Use appropriate input types (email, tel, etc.)
- [ ] Add placeholder text where appropriate
- [ ] Include proper form validation attributes
- [ ] Organize form using fieldset and legend (optional but recommended)

#### Example Structure:
```html
<form action="#" method="POST">
    <fieldset>
        <legend>Personal Information</legend>
        <!-- Name, email, phone inputs -->
    </fieldset>

    <fieldset>
        <legend>Your Message</legend>
        <!-- Subject, message inputs -->
    </fieldset>

    <!-- Preferences and buttons -->
</form>
```

## Part 2: Semantic Blog Page (50 points)

### Requirements

Create a file named `blog.html` with a properly structured blog post.

#### Must Include:
- [ ] Page header with site title and navigation
- [ ] Main content area with blog post
- [ ] Article with proper semantic structure
- [ ] At least 3 sections within the article
- [ ] Sidebar with "About" or "Related Posts"
- [ ] Footer with copyright information

#### Article Content Requirements:
- [ ] Article title (h1)
- [ ] Author name and publication date
- [ ] At least 3 paragraphs of content
- [ ] At least one image with caption (use `<figure>` and `<figcaption>`)
- [ ] At least one blockquote
- [ ] Ordered or unordered list
- [ ] Internal navigation links to sections

#### Semantic Elements to Use:
- [ ] `<header>`
- [ ] `<nav>`
- [ ] `<main>`
- [ ] `<article>`
- [ ] `<section>` (at least 2)
- [ ] `<aside>`
- [ ] `<footer>`
- [ ] `<figure>` and `<figcaption>`

## Bonus Points (+10 points total)

### Contact Form Bonuses (+5 points each)
1. Add a date picker for "Preferred contact date"
2. Include a file upload input for attachments
3. Add a range slider for "Urgency level" (1-5)

### Blog Page Bonuses (+5 points each)
1. Create a table of contents with jump links
2. Add multiple related articles in the sidebar with images
3. Include proper meta tags in `<head>` (description, keywords, author)

## Code Quality Requirements

- [ ] Valid HTML5 structure
- [ ] Proper indentation (2 or 4 spaces, be consistent)
- [ ] Meaningful comments explaining sections
- [ ] Descriptive IDs and meaningful attributes
- [ ] No inline styles (we'll add CSS in next class)

## Submission Instructions

### File Structure:
```
firstname_lastname_assignment02/
├── contact.html
├── blog.html
├── images/
│   └── (any images you use)
└── README.txt (optional: notes about your work)
```

### Submission Methods:

#### Method 1: GitHub (Recommended)
1. Create repository named `html-forms-blog`
2. Upload both HTML files
3. Enable GitHub Pages
4. Submit repository URL and live page URLs

#### Method 2: Direct Upload
1. Create folder as shown above
2. Zip the folder
3. Submit via [submission platform]

## Evaluation Criteria

### Contact Form (50 points)
| Criterion | Points |
|-----------|--------|
| All required inputs present | 15 |
| Proper labels and associations | 10 |
| Validation attributes | 10 |
| Semantic form structure | 10 |
| Code quality | 5 |

### Blog Page (50 points)
| Criterion | Points |
|-----------|--------|
| All required content present | 15 |
| Proper semantic HTML usage | 15 |
| Correct element nesting | 10 |
| Content organization | 5 |
| Code quality | 5 |

## Example Screenshots

### Contact Form Example:
```
+----------------------------------+
| Contact Us                        |
+----------------------------------+
| Name: [____________]              |
| Email: [____________]             |
| Phone: [____________]             |
|                                   |
| Subject: [Dropdown ▼]            |
|                                   |
| Message:                          |
| [____________________________]    |
| [____________________________]    |
|                                   |
| Preferred contact: ○ Email        |
|                    ○ Phone        |
|                    ○ Either       |
|                                   |
| ☐ Subscribe to newsletter         |
|                                   |
| [Submit] [Reset]                  |
+----------------------------------+
```

## Testing Your Work

### Contact Form Testing:
1. Try submitting without required fields
2. Enter invalid email format
3. Test all input types
4. Verify radio buttons work correctly
5. Check that reset button clears the form

### Blog Page Testing:
1. Validate HTML at [https://validator.w3.org/](https://validator.w3.org/)
2. Check that jump links work correctly
3. Ensure all images have alt text
4. Verify semantic structure makes sense

## Common Mistakes to Avoid

### Contact Form:
- ❌ Forgetting `for` attribute in labels
- ❌ Not using appropriate input types
- ❌ Missing `name` attributes (needed for form submission)
- ❌ No validation attributes

### Blog Page:
- ❌ Using `<div>` instead of semantic elements
- ❌ Multiple `<main>` elements (only one per page)
- ❌ Improper heading hierarchy (h1 → h3, skipping h2)
- ❌ Using `<section>` without a heading

## Resources

- [MDN Form Controls](https://developer.mozilla.org/en-US/docs/Learn/Forms/Basic_native_form_controls)
- [MDN Semantic HTML](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantics_in_html)
- [HTML5 Input Types Reference](https://www.w3schools.com/html/html_form_input_types.asp)
- [Class Code Examples](code/)

## Getting Help

- **Office Hours**: Wednesdays, 5:00 PM - 6:00 PM
- **Discussion Forum**: [Link]
- **Email**: [instructor@example.com]
- **Class Recording**: Review the form examples we built together

## Academic Integrity Reminder

- Write your own HTML code
- You may reference documentation and class materials
- AI tools can help explain concepts, but you must understand the code
- Don't copy from classmates or online templates

---

**Tips for Success:**
1. Start with the structure, add details later
2. Test frequently in your browser
3. Use the HTML validator to catch errors
4. Review class examples for reference
5. Ask questions early if you're stuck!

Good luck! This assignment builds on Class 01 and introduces important concepts we'll use throughout the course.

*Assignment created: January 20, 2025*
