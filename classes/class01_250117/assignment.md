# Assignment 01 - Build Your First Resume Page

## Due Date
Sunday, January 19, 2025 at 11:59 PM

## Objective
Create a simple HTML resume/profile page that demonstrates understanding of basic HTML structure and semantic tags.

## Requirements

### 1. HTML Structure (Required)
- [ ] Valid HTML5 document structure
- [ ] Proper DOCTYPE declaration
- [ ] Complete `<head>` section with meta tags
- [ ] Descriptive page title
- [ ] Well-structured `<body>` content

### 2. Content Sections (Required)
Your resume should include the following sections:

#### Header Section
- [ ] Your name as main heading (`<h1>`)
- [ ] Professional title or tagline
- [ ] Contact information (email, phone, LinkedIn)

#### About Me
- [ ] Brief introduction paragraph
- [ ] Your career goals or interests

#### Education
- [ ] List of educational qualifications
- [ ] Use appropriate list tags (`<ul>` or `<ol>`)
- [ ] Include institution names and years

#### Skills
- [ ] List of technical skills
- [ ] Organized using lists
- [ ] Categorize if possible (Frontend, Backend, Tools)

#### Projects/Experience (Optional)
- [ ] At least 2-3 project descriptions
- [ ] Brief description of each
- [ ] Technologies used

### 3. HTML Elements to Include
Must use at least:
- [ ] Headings (`<h1>` through `<h3>`)
- [ ] Paragraphs (`<p>`)
- [ ] Lists (`<ul>`, `<ol>`, `<li>`)
- [ ] Links (`<a>`)
- [ ] Images (`<img>`) - at least your photo or logo
- [ ] Semantic tags (`<header>`, `<main>`, `<section>`, `<footer>`)
- [ ] At least one `<div>` or `<span>` for grouping

### 4. Code Quality
- [ ] Proper indentation
- [ ] Meaningful comments
- [ ] Descriptive alt text for images
- [ ] Valid HTML (no unclosed tags)

## Bonus Points (+5% each)

1. **Navigation Menu**: Add internal links to different sections
2. **Additional Semantic Tags**: Use `<article>`, `<aside>`, `<nav>`
3. **Table**: Include a table showing your weekly schedule or skills rating
4. **Extra Content**: Add hobbies, languages, or certifications section

## Submission Instructions

### Method 1: GitHub (Recommended)
1. Create a new repository named `resume-page`
2. Upload your HTML file (name it `index.html`)
3. Upload any images to an `images` folder
4. Enable GitHub Pages in repository settings
5. Submit the GitHub Pages URL and repository link

### Method 2: File Submission
1. Create a folder named `firstname_lastname_assignment01`
2. Include your `index.html` file
3. Include an `images` folder with any images used
4. Zip the folder
5. Submit via [submission platform]

## Evaluation Criteria

| Criterion | Points | Description |
|-----------|--------|-------------|
| HTML Structure | 20 | Valid HTML5, proper document structure |
| Required Sections | 30 | All required sections present |
| Semantic HTML | 20 | Appropriate use of semantic tags |
| Code Quality | 15 | Clean, readable, well-commented code |
| Content Quality | 10 | Professional, well-written content |
| Creativity | 5 | Unique presentation and organization |
| **Total** | **100** | |

## Example Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Your Name] - Resume</title>
</head>
<body>
    <header>
        <h1>[Your Name]</h1>
        <p>[Your Professional Title]</p>
    </header>

    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>[Your introduction]</p>
        </section>

        <section id="education">
            <h2>Education</h2>
            <!-- Add your education details -->
        </section>

        <section id="skills">
            <h2>Skills</h2>
            <!-- Add your skills -->
        </section>

        <section id="projects">
            <h2>Projects</h2>
            <!-- Add your projects -->
        </section>
    </main>

    <footer>
        <p>Contact: [email] | [phone]</p>
    </footer>
</body>
</html>
```

## Common Mistakes to Avoid

1. ❌ Missing DOCTYPE declaration
2. ❌ Unclosed tags
3. ❌ Using `<br>` excessively for spacing
4. ❌ Not using semantic HTML tags
5. ❌ Missing alt attributes on images
6. ❌ Poor indentation and formatting

## Resources

- [MDN HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [HTML Validator](https://validator.w3.org/)
- [Class Examples](code/html-basics/)
- [HTML Cheatsheet](../../resources/cheatsheets/)

## Getting Help

- **Office Hours**: Wednesdays, 5:00 PM - 6:00 PM
- **Discussion Forum**: [Link]
- **Email**: [instructor@example.com]
- **Response Time**: Within 24 hours

## Academic Integrity

- Your code must be your own work
- You may reference course materials and documentation
- AI tools (like ChatGPT) can be used for learning, but you must understand the code
- Copying from classmates or online templates will result in zero credit

---

Good luck! Remember, this is your first step into web development. Focus on understanding the fundamentals rather than making it look perfect. We'll add styling with CSS in the next class!

*Assignment created: January 17, 2025*
