# Quick Customization Guide

This guide will help you personalize your portfolio in 15 minutes or less.

## ⚡ Step-by-Step Customization

### 1. Personal Information (5 minutes)

Open `index.html` and search/replace these placeholders:

| Find | Replace With |
|------|--------------|
| `[Your Name]` | Abhishek Sharma |
| `[YN]` | Your initials |
| `your.email@example.com` | Your email address |
| `linkedin.com/in/yourprofile` | Your LinkedIn URL |
| `github.com/yourusername` | Your GitHub username |

### 2. Hero Section (2 minutes)

**Line 47-51** - Update your professional summary:
```html
<p class="hero-description">
    YOUR CUSTOM DESCRIPTION HERE
    Keep it to 2-3 sentences
</p>
```

### 3. About Me Section (3 minutes)

**Line 70-80** - Replace the about text with your story:
```html
<p class="about-intro">
    Your unique value proposition...
</p>
<p>
    Your background and experience...
</p>
```

**Line 87-115** - Update skills:
- Replace skills with your actual expertise
- Add or remove items as needed
- Keep the same HTML structure

### 4. Projects Section (5 minutes)

For each project (there are 6 examples):

1. **Change the category**: `data-category="analytics"` → Choose: `analytics`, `product`, or `ml`
2. **Update project number**: Keep sequential (01, 02, 03, etc.)
3. **Replace content**:
   - Title
   - Problem statement
   - Tools used (add/remove `<span class="tool-tag">` elements)
   - Key insights
   - GitHub link

**Template for adding new projects**:
```html
<article class="project-card" data-category="analytics">
    <div class="project-number">07</div>
    <h3 class="project-title">Project Name</h3>
    <p class="project-problem">
        <strong>Problem:</strong> What problem did you solve?
    </p>
    <div class="project-tools">
        <span class="tool-tag">Python</span>
        <span class="tool-tag">SQL</span>
    </div>
    <p class="project-insight">
        <strong>Key Insight:</strong> What did you discover/achieve?
    </p>
    <a href="https://github.com/username/repo" class="project-link" target="_blank">
        View on GitHub →
    </a>
</article>
```

## 🎨 Visual Customization

### Change Colors

Edit `style.css` (lines 7-11):
```css
:root {
    --color-accent: #2563eb;        /* Your primary color */
    --color-accent-hover: #1d4ed8;  /* Darker shade */
    --color-accent-light: #dbeafe;  /* Lighter shade */
}
```

**Color Palette Suggestions**:
- **Blue** (default): `#2563eb`
- **Purple**: `#7c3aed`
- **Green**: `#10b981`
- **Orange**: `#f59e0b`
- **Red**: `#ef4444`
- **Teal**: `#14b8a6`

### Change Fonts

1. Go to [Google Fonts](https://fonts.google.com)
2. Select your fonts
3. Copy the `<link>` tag
4. Replace line 19-21 in `index.html`
5. Update `style.css` lines 22-23:

```css
--font-display: 'Your Heading Font', serif;
--font-body: 'Your Body Font', sans-serif;
```

**Font Pairing Suggestions**:
- **Professional**: Playfair Display + Source Sans Pro
- **Modern**: Poppins + Inter
- **Editorial**: Libre Baskerville + Open Sans
- **Tech**: JetBrains Mono + Roboto
- **Elegant**: Cormorant + Lato

## 📸 Adding Images

### Add Your Photo

1. Save your photo as `images/profile.jpg`
2. Add to About section (after line 66):

```html
<div class="about-image">
    <img src="images/profile.jpg" alt="Your Name">
</div>
```

3. Add CSS for styling:

```css
.about-image {
    text-align: center;
    margin-bottom: 2rem;
}

.about-image img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid var(--color-accent);
}
```

### Add Project Screenshots

1. Create `images/projects/` folder
2. Add images: `project1.jpg`, `project2.jpg`, etc.
3. Add to each project card:

```html
<img src="images/projects/project1.jpg" alt="Project screenshot" class="project-image">
```

4. Add CSS:

```css
.project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 1rem;
}
```

## 📊 SEO Optimization

Update meta tags in `index.html` (lines 5-13):

```html
<meta name="description" content="YOUR CUSTOM DESCRIPTION - Keep under 160 characters">
<meta name="keywords" content="your, relevant, keywords, separated, by, commas">
<meta property="og:title" content="Your Name - Job Title">
<meta property="og:description" content="Brief description">
```

## 🔗 Social Links

### Add More Social Links

Add to contact section (after line 345):

```html
<a href="https://twitter.com/yourhandle" target="_blank" class="contact-card">
    <div class="contact-icon">🐦</div>
    <h3>Twitter</h3>
    <p>@yourhandle</p>
</a>

<a href="https://medium.com/@yourhandle" target="_blank" class="contact-card">
    <div class="contact-icon">✍️</div>
    <h3>Medium</h3>
    <p>medium.com/@yourhandle</p>
</a>
```

## ⚙️ Advanced Customizations

### Add Google Analytics

Add before closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

Replace `GA_MEASUREMENT_ID` with your actual ID.

### Add Favicon

1. Create a 32x32px icon
2. Save as `favicon.ico`
3. Add to `<head>`:

```html
<link rel="icon" type="image/x-icon" href="favicon.ico">
```

### Add Custom Domain

1. Buy a domain (Namecheap, Google Domains, etc.)
2. Create file named `CNAME` (no extension)
3. Add your domain: `yourdomain.com`
4. Update DNS settings with your registrar:
   - Type: A
   - Host: @
   - Value: 185.199.108.153 (and .109, .110, .111)

## ✅ Pre-Launch Checklist

Before deploying, verify:

- [ ] All `[Placeholder]` text replaced
- [ ] All links work (especially GitHub and social media)
- [ ] Email address is correct
- [ ] Resume PDF is added and linked
- [ ] Skills reflect your actual abilities
- [ ] Project descriptions are accurate
- [ ] Case studies tell YOUR story
- [ ] Meta tags updated for SEO
- [ ] Colors match your brand (if customized)
- [ ] Tested on mobile device
- [ ] Tested in different browsers
- [ ] Dark mode works correctly
- [ ] All images load (if added)
- [ ] Grammar and spelling checked

## 🎯 Content Writing Tips

### Project Descriptions

Use this formula:
1. **Problem**: What challenge existed?
2. **Action**: What did you do?
3. **Result**: What was the impact? (Use numbers!)

Example:
> **Problem**: Customer churn was 28%, impacting ARR
> **Action**: Built predictive model with Python and Scikit-learn
> **Result**: Reduced churn by 12%, saving $2.3M annually

### Case Studies

Follow STAR format:
- **S**ituation: Context and background
- **T**ask: Your responsibility
- **A**ction: Specific steps you took
- **R**esult: Measurable outcomes

### About Me

Structure:
1. Opening hook (who you are)
2. Background and expertise
3. What drives you
4. Call to connection

Keep it conversational but professional!

## 🐛 Common Issues

| Problem | Solution |
|---------|----------|
| Dark mode not working | Check JavaScript console for errors |
| Links not working | Ensure proper `https://` prefix |
| Mobile menu stuck | Clear browser cache |
| Fonts not loading | Check Google Fonts link is correct |
| Colors not changing | Edit CSS variables, not individual elements |

## 💡 Pro Tips

1. **Keep It Simple**: Don't over-complicate the design
2. **Show Results**: Always include metrics and outcomes
3. **Be Specific**: "Increased revenue" → "Increased revenue by 34%"
4. **Update Regularly**: Add new projects every few months
5. **Get Feedback**: Ask friends or mentors to review
6. **Test Everything**: Click every link, test on mobile
7. **Be Authentic**: Let your personality show through

## 📱 Testing Checklist

Test your site on:
- [ ] Chrome (desktop)
- [ ] Firefox (desktop)
- [ ] Safari (desktop)
- [ ] Chrome (mobile)
- [ ] Safari (mobile)
- [ ] Different screen sizes (use browser dev tools)

## 🚀 Ready to Launch?

Once you've completed your customizations:

1. Double-check the Pre-Launch Checklist
2. Test thoroughly
3. Follow the GitHub Pages deployment in README.md
4. Share with your network!

---

**Need help?** Review the main README.md for deployment instructions and troubleshooting.

**Remember**: Your portfolio is never "done" - keep updating it as you grow! 🌱
