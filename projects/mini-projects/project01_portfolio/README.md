# Mini Project 01: Personal Portfolio Website

## Project Overview

Create a responsive personal portfolio website that showcases your skills, projects, and contact information. This project will demonstrate your understanding of HTML, CSS, and basic responsive design principles.

## Due Date
**Week 4** - February 13, 2025

## Learning Objectives

- Apply HTML5 semantic structure
- Implement responsive CSS layouts with Flexbox/Grid
- Create a multi-page website with consistent navigation
- Practice mobile-first design
- Use modern CSS techniques

## Project Requirements

### Pages Required (Minimum 3)

#### 1. Home Page (`index.html`)
- Hero section with your name and tagline
- Brief introduction
- Call-to-action buttons
- Featured projects preview

#### 2. About Page (`about.html`)
- Detailed bio
- Skills section with visual indicators
- Education and experience
- Professional photo
- Downloadable resume (PDF)

#### 3. Projects Page (`projects.html`)
- Grid/Card layout of projects
- Each project includes:
  - Project title
  - Description
  - Technologies used
  - Live demo link (if available)
  - GitHub repository link
  - Screenshot/image

#### 4. Contact Page (`contact.html`)
- Contact form (name, email, message)
- Social media links
- Email address
- Optional: Embedded map if you want to show city/region

### Technical Requirements

#### HTML
- [ ] Valid HTML5 structure
- [ ] Semantic HTML elements
- [ ] Proper heading hierarchy
- [ ] Meta tags (viewport, description)
- [ ] Favicon

#### CSS
- [ ] External stylesheet(s)
- [ ] Responsive design (mobile, tablet, desktop)
- [ ] Flexbox and/or Grid layout
- [ ] Custom color scheme
- [ ] Typography (consider Google Fonts)
- [ ] Hover effects and transitions
- [ ] Consistent styling across pages

#### Design
- [ ] Clean, professional appearance
- [ ] Consistent navigation on all pages
- [ ] Active/current page indication in nav
- [ ] Readable typography
- [ ] Good contrast and accessibility
- [ ] Mobile-friendly (320px minimum)

#### Content
- [ ] Original content (your own information)
- [ ] No "lorem ipsum" placeholder text
- [ ] Professional tone
- [ ] Proper grammar and spelling
- [ ] Optimized images

## Bonus Features (+5 points each)

1. **Dark Mode Toggle**: Implement CSS variables and JavaScript toggle
2. **Smooth Scrolling**: Navigation with smooth scroll effect
3. **Animation**: CSS animations for elements on scroll/load
4. **Blog Section**: Additional page with blog posts
5. **Testimonials**: Section with recommendations
6. **Custom 404 Page**: Styled error page
7. **Lighthouse Score**: 90+ on Performance and Accessibility

## Recommended Structure

```
portfolio/
├── index.html
├── about.html
├── projects.html
├── contact.html
├── css/
│   ├── style.css
│   └── responsive.css (optional)
├── images/
│   ├── profile.jpg
│   ├── project1.png
│   ├── project2.png
│   └── favicon.ico
├── assets/
│   └── resume.pdf
└── README.md
```

## Design Inspiration

- [Awwwards](https://www.awwwards.com/)
- [Dribbble Portfolios](https://dribbble.com/tags/portfolio)
- [Behance](https://www.behance.net/)

## Color Palette Ideas

### Option 1: Modern Blue
- Primary: `#667eea`
- Secondary: `#764ba2`
- Accent: `#f093fb`
- Dark: `#2c3e50`
- Light: `#f8f9fa`

### Option 2: Professional
- Primary: `#2c3e50`
- Secondary: `#3498db`
- Accent: `#e74c3c`
- Dark: `#1a252f`
- Light: `#ecf0f1`

### Option 3: Vibrant
- Primary: `#ff6b6b`
- Secondary: `#4ecdc4`
- Accent: `#ffe66d`
- Dark: `#1a535c`
- Light: `#f7fff7`

## Typography Suggestions

Google Fonts combinations:
- Headings: Poppins, Montserrat, Raleway
- Body: Open Sans, Roboto, Lato

## Evaluation Criteria

| Category | Points | Description |
|----------|--------|-------------|
| HTML Structure | 15 | Semantic, valid, well-organized |
| CSS Styling | 20 | Professional design, consistency |
| Responsiveness | 20 | Works well on all screen sizes |
| Content Quality | 15 | Professional, complete information |
| Code Quality | 10 | Clean, commented, organized |
| Navigation | 10 | Functional, intuitive |
| Creativity | 10 | Original design, visual appeal |
| **Total** | **100** | |

## Submission Requirements

### GitHub Repository
1. Create public repository: `portfolio-website`
2. Include all source files
3. Write a descriptive README.md
4. Commit regularly with meaningful messages

### GitHub Pages Deployment
1. Enable GitHub Pages in repository settings
2. Select main branch as source
3. Submit live URL

### Submission Checklist
- [ ] GitHub repository URL
- [ ] Live website URL (GitHub Pages)
- [ ] All pages functional
- [ ] No broken links or images
- [ ] Tested on mobile and desktop
- [ ] HTML validated
- [ ] README with project description

## Getting Started

### Step 1: Planning (30 minutes)
- Sketch wireframes for each page
- Choose color palette
- Select fonts
- Gather content (bio, projects, images)

### Step 2: HTML Structure (2-3 hours)
- Create all HTML pages
- Add semantic structure
- Insert content
- Link pages together

### Step 3: CSS Styling (4-5 hours)
- Set up base styles (colors, fonts, reset)
- Style navigation
- Style each page
- Add responsive breakpoints

### Step 4: Testing & Refinement (1-2 hours)
- Test on different devices
- Fix bugs and layout issues
- Optimize images
- Validate HTML/CSS

### Step 5: Deployment (30 minutes)
- Push to GitHub
- Enable GitHub Pages
- Test live site
- Submit

## Common Pitfalls to Avoid

1. ❌ Not testing on mobile devices
2. ❌ Using too many fonts or colors
3. ❌ Poor image optimization (large file sizes)
4. ❌ Broken links between pages
5. ❌ Inconsistent spacing and alignment
6. ❌ Forgetting alt text on images
7. ❌ Not validating HTML/CSS
8. ❌ Placeholder content instead of real information

## Resources

### Tools
- [Google Fonts](https://fonts.google.com/)
- [Coolors](https://coolors.co/) - Color palette generator
- [Unsplash](https://unsplash.com/) - Free stock photos
- [Canva](https://www.canva.com/) - Design tool
- [Font Awesome](https://fontawesome.com/) - Icons

### Validators
- [W3C HTML Validator](https://validator.w3.org/)
- [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)
- [Lighthouse](https://developers.google.com/web/tools/lighthouse)

### Learning Resources
- [MDN Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
- [CSS Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [CSS Tricks Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)

## Example Code Snippets

### Responsive Navigation
```css
nav ul {
  display: flex;
  list-style: none;
  gap: 2rem;
}

@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    gap: 1rem;
  }
}
```

### Card Layout
```css
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.project-card {
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s;
}

.project-card:hover {
  transform: translateY(-5px);
}
```

## Getting Help

- **Office Hours**: Wednesdays, 5:00-6:00 PM
- **Discussion Forum**: [Link]
- **Project Check-in**: Week 3 class session

---

This is your chance to showcase your personality and skills. Make it unique, make it professional, and have fun with it!

**Good luck!**

*Project assigned: Week 1 | Due: Week 4*
