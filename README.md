# Augment Lab - Corporate Website

A professional, responsive corporate website for Augment Lab - Expert Next.js & Flutter Development company based in Dhaka, Bangladesh.

## 🌟 Features

- **Fully Responsive Design** - Works perfectly on all devices
- **Modern UI/UX** - Professional corporate design with smooth animations
- **Complete Sections**:
  - Hero section with call-to-actions
  - Services showcase
  - Portfolio projects
  - Team members
  - Client testimonials
  - Contact form with validation
- **Performance Optimized** - Lazy-loaded responsive images, non-blocking styles/scripts, critical CSS inlined
- **PWA Ready** - Offline caching via Service Worker and `manifest.json`
- **SEO Friendly** - Proper meta tags and semantic HTML

## 📁 File Structure

```
static-website/
├── index.html       # Main HTML file (with performance hints and SW registration)
├── styles.css       # All styling (with content-visibility and reduced-motion)
├── script.js        # Interactive functionality (deferred)
├── sw.js            # Service worker for caching static assets
├── manifest.json    # PWA manifest
└── README.md        # This file
```

## 🚀 Deploy to GitHub Pages

### Method 1: Using GitHub Web Interface

1. **Create a new GitHub repository**
   - Go to https://github.com/new
   - Name it: `augment-lab-website` (or any name you prefer)
   - Make it Public
   - Click "Create repository"

2. **Upload files**
   - Click "uploading an existing file"
   - Drag and drop these files:
     - `index.html`
     - `styles.css`
     - `script.js`
   - Click "Commit changes"

3. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to "Pages" section (left sidebar)
   - Under "Source", select "main" branch
   - Click "Save"
   - Your site will be live at: `https://yourusername.github.io/augment-lab-website/`

### Method 2: Using Git Command Line

```bash
# Initialize git repository
git init

# Add all files
git add index.html styles.css script.js README.md

# Commit files
git commit -m "Initial commit: Augment Lab website"

# Add your GitHub repository as remote
git remote add origin https://github.com/yourusername/augment-lab-website.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in repository settings.

## 🔧 Customization

### Update Contact Information

Edit `index.html` and search for these sections to update:

1. **Email**: Search for `hello@augmentlab.com`
2. **Phone**: Search for `+880 1XXX-XXXXXX`
3. **Address**: Search for `Dhaka, Bangladesh`

### Update Social Media Links

Search for `href="#"` in the footer and team sections, replace `#` with your actual social media URLs:

```html
<a href="https://linkedin.com/company/yourcompany" target="_blank">
```

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
        <img src="your-logo.png" alt="Augment Lab" style="height: 40px;">
    </a>
</div>
```

## 📱 Testing Locally

Simply open `index.html` in your web browser:

```bash
# On Mac
open index.html

# On Windows
start index.html

# On Linux
xdg-open index.html
```

Or use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (with http-server)
npx http-server

# Then visit http://localhost:8000

Note: Service Worker requires a secure context (https) or localhost. Use a local server to test SW caching.
```

## 🌐 Custom Domain

To use a custom domain with GitHub Pages:

1. Add a file named `CNAME` in your repository with your domain:
   ```
   www.augmentlab.com
   ```

2. Configure DNS records at your domain provider:
   - Add a CNAME record pointing to: `yourusername.github.io`
   - Or add A records pointing to GitHub's IPs

3. Enable "Enforce HTTPS" in GitHub Pages settings

## 📧 Contact Form Integration

The contact form currently shows a success message. To make it functional:

### Option 1: Formspree (Free & Easy)

1. Sign up at https://formspree.io
2. Create a new form and get your endpoint
3. Update the form in `index.html`:

```html
<form id="contactForm" action="https://formspree.io/f/your-form-id" method="POST">
```

### Option 2: EmailJS (Free tier available)

1. Sign up at https://www.emailjs.com
2. Set up email service
3. Add EmailJS script and update `script.js`

### Option 3: Custom Backend

Connect to your own API endpoint by modifying the fetch call in `script.js`.

## 🎨 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📄 License

This website template is provided as-is for Augment Lab.

## 🤝 Support

For any questions or support, contact: hello@augmentlab.com

---

Built with ❤️ by Augment Lab Team
