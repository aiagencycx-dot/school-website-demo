# School Website - Static Version

A simple, responsive school website built with HTML, CSS, and JavaScript. Perfect for Phase 1 of the school management system project.

## Features

- ✅ **Fully Responsive** - Works on all devices
- ✅ **Modern Design** - Clean, professional appearance
- ✅ **Fast Loading** - No frameworks, pure HTML/CSS/JS
- ✅ **Easy to Customize** - Simple file structure
- ✅ **Free Hosting** - Deploy on GitHub Pages, Vercel, or Netlify
- ✅ **SEO Ready** - Proper meta tags and structure

## Pages Included

1. **Homepage** (`index.html`) - Welcome section, features, quick links
2. **About Page** (`about.html`) - History, mission, vision, statistics
3. **More pages can be added easily**

## Quick Start

### Option 1: View Locally
```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

### Option 2: Deploy to Vercel (Recommended)
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

### Option 3: Deploy to GitHub Pages
1. Create a new GitHub repository
2. Push all files
3. Go to Settings → Pages
4. Select "Deploy from main branch"

## Customization

### 1. Change School Name
Edit `index.html` and other pages:
```html
<span>School Name</span>  <!-- Change this -->
```

### 2. Change Colors
Edit `css/style.css`:
```css
:root {
    --primary-color: #2563eb;    /* Main blue color */
    --primary-dark: #1d4ed8;     /* Darker blue */
    --secondary-color: #64748b;  /* Gray color */
    --accent-color: #10b981;     /* Green accent */
}
```

### 3. Add New Pages
1. Copy `about.html` to `newpage.html`
2. Update the content
3. Add link to navigation in all pages

### 4. Update Contact Information
Edit the footer in all HTML files:
```html
<li><i class="fas fa-phone"></i> +1 (123) 456-7890</li>
<li><i class="fas fa-envelope"></i> info@schoolname.edu</li>
```

## File Structure

```
school-website-static/
├── index.html          # Homepage
├── about.html          # About page
├── css/
│   └── style.css       # All styles (responsive design)
├── js/
│   └── script.js       # Interactive features
├── images/             # Place for images
├── README.md           # This file
└── DEPLOYMENT.md       # Detailed deployment guide
```

## What's Included

### CSS Features:
- Mobile-first responsive design
- Flexbox and Grid layouts
- CSS variables for easy theming
- Smooth animations and transitions
- Modern button and card styles

### JavaScript Features:
- Mobile navigation menu
- Smooth scrolling
- Form validation
- Image gallery (basic)
- Back to top button
- Counter animations
- Tooltips

### Design Elements:
- Hero section with call-to-action
- Feature cards grid
- Quick access links
- Professional footer
- Social media integration
- Contact information

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance

- No external dependencies (except Font Awesome icons)
- Optimized CSS and JavaScript
- Lazy loading for images
- Minimal HTTP requests

## Next Phase (Phase 2)

When ready to upgrade to a dynamic website:

1. **Convert to Next.js** for better SEO and performance
2. **Add contact forms** with email integration
3. **Create admin panel** for content management
4. **Add database** for dynamic content
5. **Implement user authentication**

## License

This template is free to use for any school or educational institution.

## Support

For issues or questions:
1. Check the `DEPLOYMENT.md` file
2. Review browser console for errors
3. Contact the development team

---

**Phase 1 Goal:** Get a professional school website live within 1-2 days.

**Success Criteria:**
- [ ] Website is accessible online
- [ ] All pages load correctly
- [ ] Mobile responsive design works
- [ ] Contact information is correct
- [ ] School branding is applied

Ready to deploy? Follow the instructions in `DEPLOYMENT.md`!