# MIX3 SOUND, INC. - WEBSITE INSTRUCTIONS

**Welcome to the Mix3 Sound Website Development Team!**

This document provides comprehensive instructions for team members working on the Mix3 Sound website. Please read this carefully before making any changes to the site.

---

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [File Structure](#file-structure)
3. [Getting Started](#getting-started)
4. [How to Edit Content](#how-to-edit-content)
5. [Adding Images](#adding-images)
6. [Best Practices](#best-practices)
7. [GitHub Workflow](#github-workflow)
8. [Future Enhancements](#future-enhancements)
9. [Common Tasks](#common-tasks)
10. [Troubleshooting](#troubleshooting)
11. [Resources](#resources)

---

## 🎯 Project Overview

**Company:** Mix3 Sound, Inc.  
**Website Purpose:** Professional live sound production services  
**Target Audience:** Event planners, tour managers, corporate clients  
**Technology:** Static HTML/CSS (no server required)  
**Status:** Initial Development Phase

### Our Goals
- Create a professional, modern website that stands out from competitors
- Showcase our expertise in live sound production
- Generate leads from corporate and touring clients
- Build credibility and trust in the industry

---

## 📁 File Structure

```
mix3sound2026/
│
├── index.html              # Homepage (main entry point)
├── about.html              # About Us page
├── services.html           # Services page
├── portfolio.html          # Portfolio/Projects page
├── contact.html            # Contact page
├── INSTRUCTIONS.MD         # This file
├── README.md               # Project readme
│
├── css/
│   ├── style.css          # Main stylesheet
│   └── responsive.css     # Mobile/tablet styles
│
└── images/                 # Image assets (create this folder)
    ├── hero/              # Hero section images
    ├── services/          # Service page images
    ├── portfolio/         # Project photos
    └── team/              # Team/about photos
```

### Page Purposes

- **index.html** - First impression, showcases key services and features
- **about.html** - Company history, mission, values, team
- **services.html** - Detailed service descriptions (tours, corporate, festivals)
- **portfolio.html** - Past projects, client testimonials
- **contact.html** - Contact form and company information

---

## 🚀 Getting Started

### Prerequisites
- Basic understanding of HTML and CSS
- Text editor (VS Code, Sublime Text, Notepad++, etc.)
- Web browser (Chrome, Firefox, Safari, Edge)
- Git installed on your computer
- GitHub account with access to the repository

### Opening the Website Locally

1. **Clone the Repository**
   ```bash
   git clone [repository-url]
   cd mix3sound2026
   ```

2. **Open in Your Browser**
   - Simply double-click `index.html` in your file explorer
   - OR right-click → "Open with" → Your browser
   - No server needed!

3. **Open in Your Code Editor**
   ```bash
   code .  # For VS Code
   ```

### Testing Your Changes
- Always test in multiple browsers (Chrome, Firefox, Safari, Edge)
- Check mobile responsiveness using browser developer tools (F12)
- Test all links before committing changes

---

## ✏️ How to Edit Content

### Editing Text Content

#### 1. Company Information
**Location:** All pages (Footer section)

```html
<!-- Search for this in any HTML file -->
<div class="footer-col">
    <h4>Contact</h4>
    <ul>
        <li>Email: info@mix3sound.com</li>      <!-- Update email here -->
        <li>Phone: (555) 123-4567</li>          <!-- Update phone here -->
        <li>USA</li>
    </ul>
</div>
```

**📝 To Update:**
- Find the footer section (near the bottom of each HTML file)
- Replace placeholder email and phone with real contact info
- Add specific address if desired

---

#### 2. Homepage Hero Section
**Location:** `index.html`

```html
<h2 class="hero-subtitle">Professional Live Sound Solutions</h2>
<h1 class="hero-title">We Make Your Events Sound Perfect</h1>
<p class="hero-description">From world-class tours...</p>
```

**📝 To Update:**
- Open `index.html` in your editor
- Find the `<section class="hero">` section
- Edit the text between the HTML tags
- Keep messaging strong and client-focused

---

#### 3. Services Descriptions
**Location:** `services.html`

Each service has its own section with an `id` attribute:
- `id="tours"` - Concert Tours
- `id="corporate"` - Corporate Events  
- `id="festivals"` - Festival Production

**📝 To Update:**
- Open `services.html`
- Find the service section you want to edit
- Update bullet points, descriptions, and highlights
- Add specific equipment brands you actually use

---

#### 4. Portfolio Projects
**Location:** `portfolio.html`

```html
<div class="portfolio-item" data-category="tours">
    <div class="portfolio-image">
        <div class="placeholder-image">
            <p>Tour Photo</p>  <!-- Replace with <img> tag -->
        </div>
    </div>
    <div class="portfolio-info">
        <h3>National Arena Tour 2025</h3>
        <p class="portfolio-category">Concert Tour</p>
        <p>50-city tour featuring...</p>
    </div>
</div>
```

**📝 To Update:**
- Add real project titles and descriptions
- Replace placeholder images (see "Adding Images" section)
- Keep `data-category` attribute for filtering ("tours", "corporate", or "festivals")

---

#### 5. Testimonials
**Location:** `portfolio.html`

```html
<div class="testimonial-card">
    <p class="testimonial-text">"Quote from client..."</p>
    <p class="testimonial-author">- Client Name, Title</p>
</div>
```

**📝 To Update:**
- Get real testimonials from satisfied clients
- Use full name and job title if client approves
- Keep testimonials authentic and specific

---

### Editing Colors and Styles

**Location:** `css/style.css` (top of file)

```css
:root {
    --primary-color: #FF4B00;      /* Main brand color (orange) */
    --secondary-color: #1a1a1a;    /* Dark backgrounds */
    --accent-color: #00D4FF;       /* Accent highlights (blue) */
    /* ... more colors ... */
}
```

**📝 To Change Brand Colors:**
1. Open `css/style.css`
2. Find the `:root` section at the top
3. Change the hex color codes
4. Save and refresh browser to see changes

**Popular Color Tools:**
- [Coolors.co](https://coolors.co) - Color palette generator
- [Adobe Color](https://color.adobe.com) - Professional color tools

---

## 🖼️ Adding Images

### Step 1: Organize Your Images

Create folders if they don't exist:
```
images/
├── hero/          # Large hero background images
├── services/      # Service-related photos
├── portfolio/     # Project/event photos
├── team/          # Team member photos
└── logo/          # Company logos
```

### Step 2: Optimize Images First

**Important:** Always optimize images before uploading!

- **Recommended sizes:**
  - Hero images: 1920x1080px (landscape)
  - Portfolio photos: 800x600px
  - Team photos: 400x400px (square)
  
- **File formats:**
  - JPEG for photos (.jpg)
  - PNG for logos/graphics (.png)
  - WebP for best compression (.webp)

- **Optimization tools:**
  - [TinyPNG.com](https://tinypng.com) - Online image compressor
  - [Squoosh.app](https://squoosh.app) - Google's image optimizer

### Step 3: Add Images to HTML

**Replace placeholder images:**

```html
<!-- BEFORE (placeholder) -->
<div class="placeholder-image">
    <p>Tour Photo</p>
</div>

<!-- AFTER (real image) -->
<img src="images/portfolio/arena-tour-2025.jpg" 
     alt="National Arena Tour 2025 - Mix3 Sound">
```

**Add hero background image:**

```html
<!-- In index.html, add style attribute to hero section -->
<section class="hero" style="background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('images/hero/live-sound-hero.jpg');">
```

### Image Best Practices
✅ Always use descriptive `alt` text for accessibility  
✅ Use lowercase filenames with hyphens: `my-image.jpg`  
✅ Keep file sizes under 500KB  
✅ Test images load on all devices  
❌ Never use spaces in filenames  
❌ Don't use huge unoptimized images

---

## 🎨 Best Practices

### Content Writing
- **Be specific:** "50-city arena tour" not "big tour"
- **Use numbers:** "500+ events" not "many events"
- **Show expertise:** Mention specific equipment brands (d&b, L-Acoustics, DiGiCo)
- **Call to action:** Every page should guide visitors to contact you
- **Professional tone:** We serve high-end clients, write professionally

### Code Organization
- **Indent properly:** Use 4 spaces for indentation
- **Comment your changes:** Add `<!-- Team member note -->` when making updates
- **One change at a time:** Don't edit everything at once
- **Test before committing:** Always preview changes in browser

### Mobile-First Thinking
- Always check how changes look on mobile
- Use Chrome DevTools (F12) → Toggle device toolbar
- Test on actual phones when possible
- Keep text readable and buttons tappable

### Performance
- Keep total page size under 3MB
- Optimize all images before uploading
- Don't add unnecessary JavaScript libraries
- Test loading speed on slow connections

---

## 🔄 GitHub Workflow

### Basic Git Commands

#### 1. **Start Your Work Session**
```bash
# Make sure you're on the main branch
git checkout main

# Get the latest code
git pull origin main

# Create a new branch for your work
git checkout -b your-name/description-of-change
# Example: git checkout -b john/update-services-page
```

#### 2. **Make Your Changes**
- Edit files in your code editor
- Save your work
- Test in browser

#### 3. **Commit Your Changes**
```bash
# See what files you changed
git status

# Add files to commit
git add index.html css/style.css
# OR add everything: git add .

# Commit with a clear message
git commit -m "Update services page with new equipment list"
```

#### 4. **Push to GitHub**
```bash
# Push your branch to GitHub
git push origin your-name/description-of-change
```

#### 5. **Create a Pull Request**
- Go to GitHub repository in your web browser
- Click "Pull Requests" → "New Pull Request"
- Select your branch
- Add description of what you changed
- Request review from team lead
- Wait for approval before merging

### Commit Message Best Practices

Good commit messages:
```
✅ "Add team photos to about page"
✅ "Update contact email and phone number"
✅ "Fix mobile menu not closing bug"
✅ "Optimize hero images for faster loading"
```

Bad commit messages:
```
❌ "Updates"
❌ "Fixed stuff"
❌ "asdfasdf"
❌ "Final version"
```

### Handling Conflicts

If you get a merge conflict:
1. Don't panic! This is normal
2. Git will mark the conflicted sections
3. Open the file and look for `<<<<<<<` markers
4. Choose which version to keep
5. Remove the conflict markers
6. Commit the resolved file
7. Ask for help if stuck!

---

## 🚀 Future Enhancements

### Phase 1 - Content (Immediate)
- [ ] Add real company photos to all pages
- [ ] Replace placeholder contact information
- [ ] Add actual client testimonials
- [ ] Write detailed portfolio project descriptions
- [ ] Add company logo to navigation
- [ ] Update team member bios and photos (about page)
- [ ] Add social media links (footer)

### Phase 2 - Functionality (Short-term)
- [ ] Integrate contact form with email service (Formspree, EmailJS)
- [ ] Add image gallery/lightbox for portfolio
- [ ] Create equipment inventory page
- [ ] Add video testimonials
- [ ] Implement analytics (Google Analytics)
- [ ] Add FAQ accordion functionality
- [ ] Create blog section for industry insights

### Phase 3 - Advanced (Long-term)
- [ ] Add online quote request calculator
- [ ] Client portal for booking management
- [ ] Integration with CRM system
- [ ] Multi-language support (Spanish)
- [ ] Interactive venue acoustic calculator
- [ ] Equipment rental e-commerce
- [ ] Live chat support widget

### SEO & Marketing
- [ ] Add meta descriptions to all pages
- [ ] Create sitemap.xml
- [ ] Set up Google Business Profile
- [ ] Add schema markup for local business
- [ ] Optimize for "live sound [city]" keywords
- [ ] Create case study pages
- [ ] Add downloadable service brochures

---

## 🛠️ Common Tasks

### Task 1: Update Contact Information
1. Open all 5 HTML files
2. Find the footer section (search for `<footer class="footer">`)
3. Update email, phone, and address in each file
4. Save all files
5. Test that email/phone links work

### Task 2: Add a New Portfolio Project
1. Open `portfolio.html`
2. Find the portfolio-grid section
3. Copy an existing `<div class="portfolio-item">` block
4. Paste it into the grid
5. Update the title, category, description
6. Add your image (see "Adding Images" section)
7. Make sure `data-category` is correct ("tours", "corporate", or "festivals")
8. Save and test the filter buttons

### Task 3: Change the Website Colors
1. Open `css/style.css`
2. Find the `:root` section
3. Change `--primary-color` (main brand color)
4. Change `--accent-color` (highlight color)
5. Save and refresh browser
6. Check all pages to ensure colors look good

### Task 4: Add a Team Member (About Page)
1. Open `about.html`
2. Find a suitable section (or create new one)
3. Add image and bio
4. Format consistently with existing content
5. Test on mobile and desktop

### Task 5: Update Service Offerings
1. Open `services.html`
2. Find the service section you want to update
3. Edit the bullet points and descriptions
4. Add or remove equipment lists
5. Update pricing information if desired
6. Test all anchor links work (e.g., `#tours`, `#corporate`)

---

## ❗ Troubleshooting

### Problem: Changes don't appear in browser
**Solution:** Hard refresh the page
- Windows/Linux: `Ctrl + Shift + R` or `Ctrl + F5`
- Mac: `Cmd + Shift + R`
- Or clear browser cache

### Problem: CSS is broken/not loading
**Solution:** Check file paths
```html
<!-- Make sure paths are correct -->
<link rel="stylesheet" href="css/style.css">
<!-- NOT: href="../css/style.css" or href="/css/style.css" -->
```

### Problem: Images not displaying
**Solution:** Check three things:
1. File path is correct: `images/portfolio/photo.jpg`
2. Filename matches exactly (case-sensitive on servers!)
3. File actually exists in the folder

### Problem: Mobile menu not working
**Solution:** Make sure JavaScript is included
- Check that the `<script>` section at bottom of page is present
- Look for browser console errors (F12 → Console tab)

### Problem: Git push rejected
**Solution:** Pull first, then push
```bash
git pull origin main
# Resolve any conflicts
git push origin your-branch-name
```

### Problem: Layout looks weird on mobile
**Solution:** Check responsive.css is loaded
```html
<!-- Both stylesheets should be in <head> -->
<link rel="stylesheet" href="css/style.css">
<link rel="stylesheet" href="css/responsive.css">
```

---

## 📚 Resources

### Learning HTML & CSS
- [MDN Web Docs](https://developer.mozilla.org) - Best web development reference
- [W3Schools](https://www.w3schools.com) - Beginner-friendly tutorials
- [CSS-Tricks](https://css-tricks.com) - Advanced CSS techniques
- [freeCodeCamp](https://www.freecodecamp.org) - Free coding courses

### Design Inspiration
- [Awwwards](https://www.awwwards.com) - Award-winning web design
- [Dribbble](https://dribbble.com) - Design inspiration
- [Behance](https://www.behance.net) - Creative portfolios
- Search "audio production website" for industry-specific inspiration

### Tools We Use
- **Code Editor:** Visual Studio Code (recommended)
- **Version Control:** Git & GitHub
- **Image Editing:** Photoshop, GIMP (free), Canva
- **Image Optimization:** TinyPNG, Squoosh
- **Browser Testing:** Chrome DevTools, Firefox Developer Tools

### Competitor Research
Study these live sound companies for ideas:
- Sound Image
- Clair Global
- Eighth Day Sound
- Britannia Row Productions
- All Access Staging & Productions

### SEO & Marketing
- [Google Search Console](https://search.google.com/search-console) - Monitor site performance
- [Google Analytics](https://analytics.google.com) - Track website visitors
- [Yoast SEO Blog](https://yoast.com/seo-blog/) - SEO best practices

### Audio Industry Resources
- ProSoundWeb - Industry news and forums
- Live Design - Production news and features
- FOH Magazine - Front of house engineering

---

## 📞 Getting Help

### Internal Team
- **Project Lead:** [Add name and contact]
- **Technical Questions:** [Add contact]
- **Content Questions:** [Add contact]

### External Resources
- **GitHub Issues:** Report bugs or request features in the repository
- **Stack Overflow:** Search/ask technical questions
- **MDN Web Docs:** Official web standards documentation

### Before Asking for Help
1. Check this instructions document
2. Search Google/Stack Overflow
3. Check browser console for errors (F12)
4. Try to isolate the problem
5. Prepare a clear description of the issue

### When Asking for Help, Include:
- What you were trying to do
- What you expected to happen
- What actually happened
- Screenshots if visual issue
- Browser and operating system
- Any error messages

---

## 🎯 Quality Checklist

Before submitting any changes, verify:

**Content**
- [ ] All text is professional and error-free
- [ ] Contact information is accurate
- [ ] No placeholder text remains (like "Lorem ipsum")
- [ ] Links all work correctly

**Design**
- [ ] Changes look good on desktop
- [ ] Changes look good on tablet
- [ ] Changes look good on mobile
- [ ] Colors match brand guidelines
- [ ] Images are optimized and load quickly

**Code**
- [ ] HTML validates (use W3C Validator)
- [ ] CSS is properly formatted
- [ ] No console errors in browser
- [ ] Code is properly indented
- [ ] Comments explain complex changes

**Testing**
- [ ] Tested in Chrome
- [ ] Tested in Firefox
- [ ] Tested in Safari/Edge
- [ ] Tested on actual mobile device
- [ ] All forms work correctly
- [ ] Page loads in under 3 seconds

**Git**
- [ ] Commit message is clear
- [ ] Only relevant files are committed
- [ ] Branch is up to date with main
- [ ] Pull request has description

---

## 🔒 Important Notes

### What NOT to Do
❌ Don't delete files without asking  
❌ Don't commit passwords or sensitive data  
❌ Don't work directly on the `main` branch  
❌ Don't copy code you don't understand  
❌ Don't ignore mobile responsiveness  
❌ Don't use copyrighted images without permission

### What TO Do
✅ Always create a new branch for changes  
✅ Test thoroughly before committing  
✅ Ask questions when unsure  
✅ Keep commits small and focused  
✅ Write clear commit messages  
✅ Review your own changes before submitting

---

## 📝 Version History

**Version 1.0** - February 2026
- Initial website structure
- Five main pages (Home, About, Services, Portfolio, Contact)
- Responsive design for all devices
- Basic interactive elements

---

## 🙏 Final Words

Thank you for being part of the Mix3 Sound web development team! Your contributions help us showcase our professional audio services and attract more clients.

Remember:
- **Quality over speed** - Take time to do it right
- **Ask questions** - No question is too small
- **Be professional** - This represents our company
- **Stay organized** - Follow the workflows
- **Have fun!** - We're building something great

If you have suggestions for improving this document, please submit a pull request or contact the project lead.

**Let's make this the best live sound website out there!**

---

*Last updated: February 5, 2026*  
*Document maintained by: Mix3 Sound Development Team*
