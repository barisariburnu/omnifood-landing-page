# Contributing to Omnifood Landing Page

First off, thank you for considering contributing to Omnifood Landing Page! It's people like you that make this project better for everyone.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Pull Requests](#pull-requests)
- [Development Setup](#development-setup)
- [Style Guidelines](#style-guidelines)
  - [HTML Guidelines](#html-guidelines)
  - [CSS Guidelines](#css-guidelines)
  - [JavaScript Guidelines](#javascript-guidelines)
  - [Git Commit Messages](#git-commit-messages)
- [Project Structure](#project-structure)

## Code of Conduct

This project and everyone participating in it is governed by respect and professionalism. By participating, you are expected to uphold this standard. Please report unacceptable behavior to the project maintainers.

### Our Standards

- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

**Bug Report Template:**

```markdown
**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Environment:**
 - OS: [e.g. Windows 10, macOS 12.0]
 - Browser: [e.g. Chrome 96, Firefox 95]
 - Screen Size: [e.g. 1920x1080, Mobile 375x667]

**Additional context**
Add any other context about the problem here.
```

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. Create an issue and provide the following information:

**Enhancement Template:**

```markdown
**Is your feature request related to a problem? Please describe.**
A clear and concise description of what the problem is.

**Describe the solution you'd like**
A clear and concise description of what you want to happen.

**Describe alternatives you've considered**
A clear and concise description of any alternative solutions or features you've considered.

**Additional context**
Add any other context or screenshots about the feature request here.
```

### Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following our style guidelines
3. **Test your changes** thoroughly across different browsers and devices
4. **Update documentation** if you changed functionality
5. **Write clear commit messages** following our guidelines
6. **Submit a pull request** with a clear description of your changes

**Pull Request Template:**

```markdown
**Description**
Brief description of what this PR does.

**Related Issue**
Fixes #(issue number)

**Type of Change**
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

**How Has This Been Tested?**
- [ ] Desktop Chrome
- [ ] Desktop Firefox
- [ ] Desktop Safari
- [ ] Mobile Safari (iOS)
- [ ] Mobile Chrome (Android)

**Checklist:**
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have tested on multiple browsers and screen sizes
```

## Development Setup

1. **Clone your fork:**
```bash
git clone https://github.com/YOUR-USERNAME/omnifood-landing-page.git
cd omnifood-landing-page
```

2. **Create a branch:**
```bash
git checkout -b feature/your-feature-name
```

3. **Start a local server** (optional but recommended):
```bash
# Python 3
python -m http.server 8000

# Or use any other local server
npx http-server
```

4. **Make your changes** and test thoroughly

5. **Commit and push:**
```bash
git add .
git commit -m "Add: your descriptive commit message"
git push origin feature/your-feature-name
```

6. **Create a Pull Request** on GitHub

## Style Guidelines

### HTML Guidelines

- Use HTML5 semantic elements (`<header>`, `<nav>`, `<section>`, `<footer>`, etc.)
- Indent with 4 spaces (no tabs)
- Always use lowercase for element names
- Always quote attribute values
- Always include `alt` attributes for images
- Keep lines under 120 characters when possible
- Use meaningful IDs and classes

**Example:**
```html
<section class="section-features" id="features">
    <div class="row">
        <h2>Section Title</h2>
        <p class="long-copy">
            Description text goes here.
        </p>
    </div>
</section>
```

### CSS Guidelines

- Use consistent indentation (4 spaces)
- Group related properties together
- Use shorthand properties when appropriate
- Always end declarations with semicolons
- Use meaningful class names (BEM methodology preferred)
- Add comments for major sections
- Keep selectors specific but not overly complex
- Mobile-first approach for media queries

**Example:**
```css
/* ------------------------------ */
/* SECTION NAME */
/* ------------------------------ */

.section-name {
    /* Box model */
    padding: 20px;
    margin: 0 auto;
    
    /* Typography */
    font-size: 16px;
    line-height: 1.5;
    
    /* Visual */
    background-color: #fff;
    color: #000;
    
    /* Transforms & Transitions */
    transition: all 0.3s;
}
```

### JavaScript Guidelines

- Use `const` and `let` instead of `var` (if adding ES6 code)
- Use meaningful variable and function names
- Add comments for complex logic
- Follow jQuery best practices for this project
- Keep functions small and focused
- Use event delegation when appropriate

**Example:**
```javascript
// Smooth scrolling for navigation links
$('.js--scroll-to-section').click(function() {
    const target = $(this).data('target');
    $('html, body').animate({
        scrollTop: $(target).offset().top
    }, 1000);
});
```

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Start with a capital letter
- Limit the first line to 72 characters or less
- Reference issues and pull requests after the first line

**Commit Message Prefixes:**
- `Add:` - Adding new features or files
- `Fix:` - Bug fixes
- `Update:` - Updating existing features
- `Remove:` - Removing code or files
- `Refactor:` - Code refactoring
- `Style:` - Code style changes (formatting, etc.)
- `Docs:` - Documentation changes
- `Test:` - Adding or updating tests

**Examples:**
```
Add: Mobile navigation toggle functionality
Fix: Sticky navigation not appearing on scroll
Update: Hero section background image
Docs: Add installation instructions to README
```

## Project Structure

When adding new features, please maintain the existing project structure:

```
omnifood-landing-page/
├── index.html              # Main HTML file
├── resources/              # Project-specific assets
│   ├── css/               # Custom stylesheets
│   ├── js/                # Custom scripts
│   ├── img/               # Images
│   └── favicons/          # Favicon files
└── vendors/               # Third-party libraries
    ├── css/
    ├── js/
    └── fonts/
```

**Guidelines:**
- Custom code goes in `resources/`
- Third-party libraries go in `vendors/`
- Keep assets organized in their respective folders
- Optimize images before committing (compress, appropriate format)
- Use relative paths for all assets

## Testing Checklist

Before submitting your PR, please ensure:

- [ ] Code works on Chrome (latest)
- [ ] Code works on Firefox (latest)
- [ ] Code works on Safari (latest)
- [ ] Code works on Edge (latest)
- [ ] Responsive design works on mobile (320px - 480px)
- [ ] Responsive design works on tablet (481px - 1024px)
- [ ] Responsive design works on desktop (1024px+)
- [ ] All animations work smoothly
- [ ] No console errors
- [ ] Images are optimized
- [ ] Code is properly formatted
- [ ] Documentation is updated

## Questions?

Feel free to create an issue with the `question` label if you have any questions about contributing!

---

Thank you for contributing to Omnifood Landing Page! 🎉
