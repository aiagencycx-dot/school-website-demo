# School Website - Deployment Guide

## Quick Deployment Options

### Option 1: GitHub Pages (Free)
1. Create a new GitHub repository
2. Push your code:
```bash
git init
git add .
git commit -m "Initial school website"
git branch -M main
git remote add origin https://github.com/yourusername/school-website.git
git push -u origin main
```
3. Go to repository Settings → Pages
4. Select "Deploy from branch" → main branch → / (root)
5. Your site will be live at: `https://yourusername.github.io/school-website`

### Option 2: Vercel (Free, Recommended)
1. Install Vercel CLI:
```bash
npm i -g vercel
```
2. Deploy:
```bash
vercel
```
3. Follow the prompts
4. Your site will be live instantly

### Option 3: Netlify (Free)
1. Drag and drop your folder to Netlify
2. Or use Netlify CLI:
```bash
npm i -g netlify-cli
netlify deploy
```

## Local Development

### Simple HTTP Server
```bash
# Python 3
python3 -m http.server 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```

### Live Reload Development
```bash
# Install live-server
npm install -g live-server

# Start development server
live-server --port=3000
```

## Custom Domain Setup

### For GitHub Pages:
1. Buy a domain (GoDaddy, Namecheap, etc.)
2. Add CNAME file to your repository:
```
www.yourschool.edu
```
3. Configure DNS:
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```
4. Add CNAME record:
```
Type: CNAME
Name: www
Value: yourusername.github.io
```

### For Vercel/Netlify:
1. Go to project settings → Domains
2. Add your custom domain
3. Follow the DNS configuration instructions

## File Structure
```
school-website-static/
├── index.html          # Homepage
├── about.html          # About page
├── css/
│   └── style.css       # All styles
├── js/
│   └── script.js       # All JavaScript
├── images/             # Image assets (optional)
├── favicon.ico         # Website icon
└── DEPLOYMENT.md       # This file
```

## Adding More Pages

1. Create new HTML file (e.g., `contact.html`)
2. Copy the basic structure from `index.html`
3. Update navigation links
4. Add your content
5. Test locally before deploying

## SEO Optimization

### Basic Meta Tags (Add to each page):
```html
<head>
    <title>Page Title - School Name</title>
    <meta name="description" content="Brief description of page content">
    <meta name="keywords" content="school, education, learning">
    <meta name="author" content="School Name">
    
    <!-- Open Graph for social media -->
    <meta property="og:title" content="Page Title">
    <meta property="og:description" content="Brief description">
    <meta property="og:image" content="https://yourschool.edu/logo.png">
    <meta property="og:url" content="https://yourschool.edu/page.html">
    
    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary_large_image">
</head>
```

### Google Analytics:
```html
<!-- Add to head section -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## Performance Tips

1. **Optimize Images:**
   - Use WebP format when possible
   - Compress images (TinyPNG, Squoosh)
   - Add `loading="lazy"` to images

2. **Minify CSS/JS:**
   ```bash
   # Install minifier
   npm install -g css-minify js-minify
   
   # Minify CSS
   css-minify -f style.css -o css/
   
   # Minify JS
   js-minify -f script.js -o js/
   ```

3. **Enable Compression:**
   - Vercel/Netlify automatically enable gzip
   - For self-hosting, configure your server

## Security

1. **HTTPS:** Always use HTTPS (automatic on Vercel/Netlify/GitHub Pages)
2. **Security Headers:** Add to `.htaccess` or server config:
```
Header set X-Content-Type-Options "nosniff"
Header set X-Frame-Options "DENY"
Header set X-XSS-Protection "1; mode=block"
```

## Maintenance

### Regular Updates:
1. Update content regularly
2. Check for broken links
3. Update copyright year in footer
4. Test on different browsers/devices

### Backup:
```bash
# Create backup
tar -czf school-website-backup-$(date +%Y%m%d).tar.gz school-website-static/

# Restore
tar -xzf school-website-backup-20260314.tar.gz
```

## Troubleshooting

### Common Issues:

1. **Page not loading:**
   - Check file permissions
   - Verify index.html exists
   - Check server logs

2. **CSS/JS not loading:**
   - Check file paths
   - Clear browser cache
   - Check console for errors

3. **Images not showing:**
   - Check image paths
   - Verify file extensions
   - Check file permissions

### Debug Tools:
- Browser Developer Tools (F12)
- Network tab for loading issues
- Console for JavaScript errors
- Lighthouse for performance audit

## Next Steps After Deployment

1. **Submit to Google Search Console:**
   - Go to https://search.google.com/search-console
   - Add your website
   - Submit sitemap (create `sitemap.xml`)

2. **Create Social Media Accounts:**
   - Facebook page
   - Instagram account
   - Twitter/X account

3. **Email Setup:**
   - Create professional email (info@yourschool.edu)
   - Use Google Workspace or similar

4. **Analytics:**
   - Set up Google Analytics
   - Track visitor behavior
   - Monitor performance

## Support

For issues or questions:
1. Check this documentation
2. Review browser console errors
3. Search online for specific errors
4. Contact your hosting provider

---

**Remember:** This is a static site. For dynamic features (contact forms, user login, etc.), you'll need to upgrade to a dynamic platform (Next.js, WordPress, etc.) in Phase 2.