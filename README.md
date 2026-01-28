# Personal Portfolio Website

A clean, modern, and fully responsive portfolio website built with pure HTML, CSS, and JavaScript. Designed for analytics, product, and data professionals to showcase their work in a professional, recruiter-friendly format.

## ✨ Features

- **Modern Design**: Clean, editorial-inspired aesthetic with sophisticated typography
- **Fully Responsive**: Mobile-first design that looks great on all devices
- **Dark Mode**: Toggle between light and dark themes with localStorage persistence
- **Project Filtering**: Filter projects by category (Analytics, Product, ML/AI)
- **Smooth Animations**: Scroll-triggered animations and smooth transitions
- **SEO Optimized**: Proper meta tags and semantic HTML
- **Fast Loading**: No dependencies, lightweight and performant
- **Accessibility**: Keyboard navigation and ARIA labels

## 📁 Folder Structure

```
portfolio/
├── index.html          # Main HTML file
├── style.css           # Stylesheet with light/dark mode
├── script.js           # JavaScript for interactivity
├── resume.pdf          # Your resume (add your own)
└── README.md           # This file
```

## 🚀 Quick Start

### 1. Clone or Download

Download all files to a folder on your computer.

### 2. Customize Your Content

#### Update Personal Information in `index.html`:

1. **Replace placeholders** (search and replace):
   - `[Your Name]` → Your actual name
   - `[YN]` → Your initials for the logo
   - `your.email@example.com` → Your email
   - `linkedin.com/in/yourprofile` → Your LinkedIn URL
   - `github.com/yourusername` → Your GitHub URL

2. **Update Project Links**:
   - Replace all GitHub repository URLs with your actual project links
   - Update project descriptions, tools, and insights

3. **Modify Skills**:
   - Edit the skills lists in the About section to match your expertise

4. **Update Case Studies**:
   - Replace example case studies with your own experiences
   - Use the STAR format (Situation, Task, Action, Result)

### 3. Add Your Resume

Place your resume PDF in the same folder and name it `resume.pdf`, or update the link in the HTML file.

### 4. Test Locally

Simply open `index.html` in your web browser to preview the site. No server required!

## 🌐 Deploy to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon → "New repository"
3. Name it: `yourusername.github.io` (replace `yourusername` with your GitHub username)
4. Make it **Public**
5. Click "Create repository"

### Step 2: Upload Your Files

#### Option A: Using GitHub Website (Easiest)

1. On your repository page, click "uploading an existing file"
2. Drag and drop all your files (`index.html`, `style.css`, `script.js`, `resume.pdf`)
3. Scroll down and click "Commit changes"

#### Option B: Using Git Command Line

```bash
# Navigate to your project folder
cd path/to/your/portfolio

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial portfolio commit"

# Add remote (replace 'yourusername')
git remote add origin https://github.com/yourusername/yourusername.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" → "Pages" (in the left sidebar)
3. Under "Source", select "main" branch
4. Click "Save"
5. Wait 1-2 minutes for deployment

### Step 4: Access Your Site

Your site will be live at: `https://yourusername.github.io`

## 🎨 Customization Guide

### Colors

To change the color scheme, edit the CSS variables in `style.css`:

```css
:root {
    --color-accent: #2563eb;        /* Primary blue */
    --color-accent-hover: #1d4ed8;  /* Darker blue on hover */
    /* Modify these to match your brand */
}
```

### Fonts

Current fonts are:
- **Headings**: Crimson Pro (serif, editorial style)
- **Body**: DM Sans (clean, modern sans-serif)

To change fonts:
1. Browse [Google Fonts](https://fonts.google.com)
2. Update the `<link>` tag in `index.html`
3. Update the CSS variables in `style.css`:

```css
--font-display: 'Your Display Font', serif;
--font-body: 'Your Body Font', sans-serif;
```

### Adding More Projects

Copy this template in the projects section:

```html
<article class="project-card" data-category="analytics">
    <div class="project-number">07</div>
    <h3 class="project-title">Your Project Title</h3>
    <p class="project-problem">
        <strong>Problem:</strong> Describe the problem
    </p>
    <div class="project-tools">
        <span class="tool-tag">Tool 1</span>
        <span class="tool-tag">Tool 2</span>
    </div>
    <p class="project-insight">
        <strong>Key Insight:</strong> Your key findings
    </p>
    <a href="https://github.com/username/project" class="project-link" target="_blank">
        View on GitHub →
    </a>
</article>
```

### Adding Images

To add project screenshots or your photo:

1. Create an `images` folder
2. Add your images
3. Update HTML:

```html
<img src="images/project-screenshot.jpg" alt="Project screenshot">
```

## 🔧 Features Explained

### Dark Mode

- Toggle with the sun/moon button (top right)
- Persists across sessions using localStorage
- Keyboard shortcut: Press 'T' to toggle

### Project Filtering

- Click category buttons to filter projects
- Smooth fade animations between filters
- Shows all projects by default

### Mobile Menu

- Hamburger menu appears on mobile devices
- Closes automatically when clicking a link
- Click outside to close

### Smooth Scrolling

- Animated scroll when clicking navigation links
- Active link highlighting as you scroll

## 📊 SEO Optimization

The site includes:
- Semantic HTML5 elements
- Meta descriptions and keywords
- Open Graph tags for social sharing
- Fast loading times (no external dependencies)
- Mobile-responsive design

## 🎯 Best Practices

1. **Keep Content Updated**: Regularly update projects and skills
2. **Use Real Data**: Replace example metrics with your actual results
3. **Professional Tone**: Maintain a balance between personality and professionalism
4. **High-Quality Writing**: Proofread all content carefully
5. **Fast Loading**: Optimize any images you add (keep under 200KB)

## 🐛 Troubleshooting

### Site Not Loading on GitHub Pages

- Ensure repository is public
- Check that the file is named `index.html` (lowercase)
- Wait 5-10 minutes after first deployment
- Check GitHub Pages settings are correct

### Dark Mode Not Saving

- Ensure JavaScript is enabled in your browser
- Check browser console for errors
- Clear browser cache and try again

### Mobile Menu Not Working

- Check that `script.js` is properly linked
- Ensure there are no JavaScript errors in console
- Try different browsers

## 📝 Updating Your Site

After initial deployment, to update your site:

```bash
# Make your changes to files
# Then commit and push:

git add .
git commit -m "Updated projects section"
git push
```

Changes will appear on your live site within 1-2 minutes.

## 🎓 Learning Resources

- [HTML Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## 📧 Support

If you encounter issues:
1. Check the troubleshooting section above
2. Review browser console for errors (F12 → Console tab)
3. Ensure all files are properly uploaded
4. Verify your GitHub Pages settings

## 📄 License

This portfolio template is free to use for personal and commercial projects. Attribution is appreciated but not required.

## 🙏 Credits

Built with:
- [Google Fonts](https://fonts.google.com) - Crimson Pro & DM Sans
- Pure HTML, CSS, and JavaScript
- No external libraries or frameworks

---

**Good luck with your portfolio! 🚀**

Remember to customize everything to reflect your unique experience and personality. Your portfolio is often the first impression you make on potential employers or clients—make it count!
