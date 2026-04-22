# Deployment Guide - THE SENSE Bangkok Website

## Quick Deployment Options

### Option 1: Vercel (Recommended - Free & Easy)
1. Go to [vercel.com](https://vercel.com)
2. Sign up with GitHub
3. Click "New Project"
4. Import `the-sense-bangkok` repository
5. Click "Deploy"

**Vercel gives you:**
- Free hosting with HTTPS
- Automatic deployments from GitHub
- Custom domain support
- Global CDN
- Analytics

### Option 2: Netlify (Alternative Free Option)
1. Go to [netlify.com](https://netlify.com)
2. Drag and drop the `the-sense-bangkok` folder
3. Or connect GitHub repository

### Option 3: GitHub Pages (Free but Limited)
1. Push code to GitHub
2. Go to repository Settings → Pages
3. Select "Deploy from branch" → main branch
4. Save

## Custom Domain Setup

### For sensebkk.com:
1. **Register domain:** Go to Namecheap, GoDaddy, or Google Domains
2. **Configure DNS:** Add these records:
   ```
   Type: A
   Name: @
   Value: 76.76.21.21 (Vercel IP)
   
   Type: CNAME
   Name: www
   Value: cname.vercel-dns.com
   ```
3. **Add domain in Vercel:** Project Settings → Domains → Add domain

## Website Features

### Multi-Language Support
- English (EN) - Default
- Chinese (中文) - Simplified Chinese
- Japanese (日本語) - Japanese
- Korean (한국어) - Korean

### QR Code Integration
- LINE - For Thai/Japanese customers
- WeChat - For Chinese customers
- Telegram - For international customers
- WhatsApp - For all customers

### Service Menu
- SENSE Classic - ฿2,800 (90 minutes)
- SENSE Premium - ฿3,800 (120 minutes)
- SENSE Royal - ฿5,500 (150 minutes)

### Contact Information
- Phone: +66 92 777 8889
- Email: reservations@thesensebangkok.com
- Address: Silom Road, Bangkok
- Hours: 12:00 PM - 2:00 AM (Daily)

## Customization

### To Update Content:
1. **Services:** Edit `index.html` service cards
2. **Prices:** Update prices in service cards
3. **Contact:** Update phone/email in contact section
4. **QR Codes:** Replace placeholder divs with actual QR code images

### To Add Actual QR Codes:
Replace each `.qr-placeholder` div with:
```html
<img src="path/to/line-qr.png" alt="LINE QR Code" width="150" height="150">
```

### To Add Real Gallery Images:
Replace Unsplash URLs in `script.js` with your own images:
```javascript
const galleryImages = [
    {
        src: "your-image-1.jpg",
        alt: "Your description"
    },
    // ...
];
```

## Local Development

### View Locally:
```bash
# Open index.html in browser
open index.html

# Or use Python simple server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### Test Multi-Language:
Click language buttons in top-right corner to test translations.

## SEO Optimization

### Meta Tags Already Included:
- Responsive viewport
- Multi-language support
- Descriptive titles
- Image alt texts

### To Add More SEO:
1. Add meta description in `<head>`:
```html
<meta name="description" content="THE SENSE Bangkok - Premium Nuru massage experience in the heart of Bangkok. Authentic Japanese therapy with modern luxury.">
```

2. Add Open Graph tags for social media:
```html
<meta property="og:title" content="THE SENSE Bangkok">
<meta property="og:description" content="Premium Nuru massage experience">
<meta property="og:image" content="url-to-image.jpg">
<meta property="og:url" content="https://sensebkk.com">
```

## Performance

### Already Optimized:
- Lazy loading for gallery images
- Optimized CSS/JS
- Responsive design
- Fast loading times

### Further Optimization:
1. Compress images before uploading
2. Use WebP format for better compression
3. Minify CSS/JS for production

## Analytics

### To Add Google Analytics:
Add to `<head>` in `index.html`:
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## Support

### Common Issues:
1. **QR codes not showing:** Replace placeholder divs with actual QR images
2. **Language not changing:** Check browser console for errors
3. **Images not loading:** Check image URLs in `script.js`

### Contact for Help:
- Website issues: Check browser console
- Deployment issues: Vercel/Netlify documentation
- Customization: Edit HTML/CSS files

## Maintenance

### Regular Updates:
1. Update service prices as needed
2. Add new gallery images periodically
3. Update contact information if changed
4. Test language functionality regularly

### Backup:
- Keep GitHub repository updated
- Download local copies regularly
- Backup custom images and QR codes

## License

This website is proprietary for THE SENSE Bangkok business use only.