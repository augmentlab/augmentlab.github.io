# Augment Lab - Corporate Website

A professional, responsive corporate website for Augment Lab - Expert Next.js & Flutter Development company based in Dhaka, Bangladesh.

🌐 **Live Site**: [https://augmentlab.github.io](https://augmentlab.github.io)

## 🌟 Features

- **Fully Responsive Design** - Works perfectly on all devices (mobile, tablet, desktop)
- **Modern UI/UX** - Professional corporate design with smooth animations and transitions
- **Complete Sections**:
  - Hero section with call-to-actions and statistics
  - Services showcase (Web Development, Mobile Apps, UI/UX Design, Consulting)
  - Portfolio projects with technology tags
  - Client testimonials with ratings
  - Contact form with Web3Forms integration
- **Performance Optimized** - Lazy-loaded responsive images, non-blocking styles/scripts, critical CSS inlined, preconnect to CDNs
- **PWA Ready** - Offline caching via Service Worker and `manifest.json` for app-like experience
- **SEO Friendly** - Proper meta tags, semantic HTML, and optimized for search engines
- **Accessibility** - Semantic HTML structure and keyboard navigation support

## 📁 File Structure

```
augmentlab.github.io/
├── index.html       # Main HTML file (with performance hints and SW registration)
├── styles.css       # All styling (with content-visibility and reduced-motion)
├── script.js        # Interactive functionality (deferred, includes form handling)
├── sw.js            # Service worker for caching static assets (network-first strategy)
├── manifest.json    # PWA manifest for installable web app
└── README.md        # This file
```

## 🚀 Deployment

This website is deployed on **GitHub Pages** using the `augmentlab.github.io` repository format, which automatically serves the site at `https://augmentlab.github.io`.

### Updating the Site

Simply push changes to the `main` branch:

```bash
# Make your changes, then:
git add .
git commit -m "Update website"
git push origin main
```

GitHub Pages will automatically rebuild and deploy your changes within a few minutes.

### Local Development

For local testing, use a local server (required for Service Worker to work):

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (with http-server)
npx http-server

# Using PHP
php -S localhost:8000

# Then visit http://localhost:8000
```

**Note**: Service Worker requires a secure context (https) or localhost. Use a local server to test PWA features and offline caching. Simply opening `index.html` in a browser won't work for Service Worker testing.

## 🔧 Customization

### Update Contact Information

Edit `index.html` and search for these sections to update:

1. **Email**: Search for `augmentlab.io@gmail.com` (appears in contact section and footer)
2. **Phone**: Search for `+880 1XXX-XXXXXX` (if you want to add/update phone number)
3. **Address**: Search for `Dhaka, Bangladesh`
4. **Calendly Link**: Search for `https://calendly.com/augmentlab` to update scheduling link

### Update Social Media Links

Current social links are already configured:

- **LinkedIn**: `https://www.linkedin.com/company/augmentlab/`
- **GitHub**: `https://github.com/augmentlab/`

To update, search for these URLs in `index.html` and replace with your actual URLs.

### Change Colors

Main color scheme is blue (#1d4ed8). To change:

1. Open `styles.css`
2. Search and replace `#1d4ed8` with your preferred color
3. Adjust complementary colors as needed

### Add Your Logo

Replace the text logo in `index.html`:

```html
<div class="logo">
  <a href="#hero">
    <img src="your-logo.png" alt="Augment Lab" style="height: 40px;" />
  </a>
</div>
```

## 🌐 Custom Domain

To use a custom domain with GitHub Pages:

1. Add a file named `CNAME` in the repository root with your domain:

   ```
   www.augmentlab.com
   ```

   (or just `augmentlab.com` for apex domain)

2. Configure DNS records at your domain provider:

   - For `www` subdomain: Add a CNAME record pointing to `augmentlab.github.io`
   - For apex domain: Add A records pointing to GitHub's IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153

3. Enable "Enforce HTTPS" in GitHub Pages settings (Settings → Pages → Enforce HTTPS)

4. Wait for DNS propagation (can take up to 24 hours)

## 📧 Contact Form Integration

The contact form is **already integrated** with [Web3Forms](https://web3forms.com/), a free form handling service.

### Current Setup

- Form submissions are sent to `https://api.web3forms.com/submit`
- Access key is configured in `index.html` (line 537)
- Form includes validation and success/error toast notifications
- Submissions are received via email at the configured address

### To Update Email Recipient

1. Sign up at [Web3Forms](https://web3forms.com/)
2. Get your access key
3. Update the `access_key` value in `index.html` (line 537)

### Alternative Options

If you want to switch to a different service:

- **Formspree**: Update form action to `https://formspree.io/f/your-form-id`
- **EmailJS**: Add EmailJS script and update `script.js` form handler
- **Custom Backend**: Modify the fetch call in `script.js` (lines 98-101) to point to your API endpoint

## 🎨 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📝 Notes

- **Team Section**: Currently commented out in `index.html` (lines 331-432). Uncomment to display team members.
- **Service Worker**: Implements network-first strategy for HTML, cache-first for static assets. Cache version is `augmentlab-cache-v1` - increment version in `sw.js` to force cache refresh.
- **Images**: Uses Unsplash and Pexels CDN with responsive srcsets for optimal loading.

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with CSS Grid and Flexbox
- **Vanilla JavaScript** - No frameworks, pure JS for performance
- **Service Worker API** - PWA capabilities
- **Web3Forms** - Form submission handling
- **Font Awesome** - Icons
- **Unsplash/Pexels** - Stock images

## 📄 License

This website is proprietary to Augment Lab. All rights reserved.

## 🤝 Support

For any questions or support, contact: **augmentlab.io@gmail.com**

---

Built with ❤️ by Augment Lab Team
