# 🌸 Beauty Clinic - Installation & Setup Guide

Welcome to Beauty Clinic, a premium Astro theme for beauty clinics, medical spas, and aesthetic medicine centers.

## 📦 Package Contents

This theme includes:
- ✅ 9 Complete Pages (Home, About, Services, Doctors, Gallery, Blog, Contact, Booking, Login, Register)
- ✅ Premium Dark/Light Mode
- ✅ Fully Responsive Design
- ✅ Advanced Animations
- ✅ Authentication Pages
- ✅ Complete Documentation

## 🚀 Quick Start (5 Minutes)

### Step 1: Extract Files
Extract the ZIP file to your desired location:
```bash
# Example location
C:\Projects\beauty-clinic-theme
# or
~/Projects/beauty-clinic-theme
```

### Step 2: Install Dependencies
Open terminal in the theme folder and run:
```bash
npm install
```

This will install all required dependencies (~2-3 minutes).

### Step 3: Start Development Server
```bash
npm run dev
```

Your site will be available at: **http://localhost:4321**

That's it! Your theme is now running. 🎉

## 📋 System Requirements

### Required
- **Node.js**: Version 18.14.1 or higher
- **npm**: Version 9.0.0 or higher (comes with Node.js)
- **Operating System**: Windows, macOS, or Linux

### Check Your Versions
```bash
node --version    # Should show v18.14.1 or higher
npm --version     # Should show 9.0.0 or higher
```

### Don't Have Node.js?
Download from: https://nodejs.org/
- Choose the **LTS (Long Term Support)** version
- Follow the installation wizard
- Restart your terminal after installation

## 🛠️ Available Commands

```bash
# Development
npm run dev          # Start dev server (http://localhost:4321)
npm run build        # Build for production
npm run preview      # Preview production build

# Utilities
npm run astro        # Run Astro CLI commands
```

## 📁 Project Structure

```
beauty-clinic-theme/
├── src/
│   ├── components/          # Reusable components
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── Hero.astro
│   │   └── ...
│   ├── layouts/
│   │   └── BaseLayout.astro # Main layout
│   ├── pages/               # All pages (routes)
│   │   ├── index.astro      # Homepage
│   │   ├── about.astro
│   │   ├── services.astro
│   │   ├── doctors.astro
│   │   ├── gallery.astro
│   │   ├── blog/
│   │   ├── contact.astro
│   │   ├── booking.astro
│   │   ├── login.astro      # Authentication
│   │   └── register.astro   # Registration
│   └── styles/              # Global styles
│       ├── design-tokens.css
│       ├── global.css
│       └── animations.css
├── public/                  # Static assets
│   ├── images/
│   └── favicon.svg
├── astro.config.mjs         # Astro configuration
├── package.json             # Dependencies
└── tsconfig.json            # TypeScript config
```

## 🎨 Customization Guide

### 1. Change Site Information

Edit `src/layouts/BaseLayout.astro`:
```astro
<title>Your Clinic Name</title>
<meta name="description" content="Your description">
```

### 2. Update Logo & Brand Name

Edit `src/components/Header.astro`:
```astro
<a href="/" class="logo">
  <span class="logo-text">Your Clinic Name</span>
</a>
```

### 3. Change Color Scheme

Edit `src/styles/design-tokens.css`:
```css
/* Primary color (Pink by default) */
--color-primary-500: #ec4899;
--color-primary-600: #db2777;

/* Secondary color (Purple by default) */
--color-secondary-500: #8b5cf6;
--color-secondary-600: #7c3aed;
```

Available color schemes:
- **Rose** (default): #ec4899
- **Purple**: #8b5cf6
- **Emerald**: #10b981
- **Blue**: #3b82f6

### 4. Modify Content

Edit page files in `src/pages/`:
- `index.astro` - Homepage content
- `about.astro` - About page
- `services.astro` - Services page
- And so on...

### 5. Add Your Images

Place images in `public/images/`:
```
public/images/
├── hero/              # Hero section images
├── services/          # Service photos
├── doctors/           # Doctor portraits
├── gallery/           # Gallery images
└── blog/              # Blog images
```

Reference images in your code:
```astro
<img src="/images/hero/hero-bg.jpg" alt="Description" />
```

## 🌐 Building for Production

### Step 1: Build the Site
```bash
npm run build
```

This creates an optimized production build in the `dist/` folder.

### Step 2: Preview Production Build (Optional)
```bash
npm run preview
```

### Step 3: Deploy

The `dist/` folder contains your complete website. Deploy it to:

**Popular Hosting Options:**
- **Vercel** (Recommended)
  - Connect your GitHub repo
  - Auto-deploy on push
  - Free SSL certificate

- **Netlify**
  - Drag & drop `dist/` folder
  - Or connect GitHub repo
  - Free SSL certificate

- **GitHub Pages**
  - Push `dist/` to gh-pages branch
  - Enable GitHub Pages in settings

- **Traditional Hosting**
  - Upload `dist/` folder via FTP
  - Point domain to the folder

### Vercel Deployment (Easiest)
1. Push code to GitHub
2. Go to https://vercel.com
3. Click "Import Project"
4. Select your repository
5. Click "Deploy"
6. Done! Your site is live.

## 📸 Image Setup (Optional but Recommended)

For the best appearance, add real photos:

### Required Images (17 total)
1. **Hero Background** (1): 1920x1080px
2. **Service Photos** (6): 800x600px each
3. **Before/After** (2): 600x600px each
4. **Doctor Portraits** (3): 500x500px each
5. **Testimonial Avatars** (3): 400x400px each
6. **CTA Background** (1): 1920x1080px
7. **Gallery Images** (1+): 800x600px each

### Where to Get Images
- **Unsplash**: https://unsplash.com (Free, high-quality)
- **Pexels**: https://pexels.com (Free, high-quality)
- **Your Own Photos**: Best for authenticity

### Image Optimization Tips
- Use JPG for photos (smaller file size)
- Use PNG for graphics with transparency
- Optimize images before uploading (use TinyPNG.com)
- Recommended max size: 500KB per image

## 🎯 Page Routes

Your theme includes these pages:

| Page | URL | Description |
|------|-----|-------------|
| Home | `/` | Homepage with hero, services, testimonials |
| About | `/about` | About the clinic and team |
| Services | `/services` | All services overview |
| Doctors | `/doctors` | Doctor profiles |
| Gallery | `/gallery` | Before/after photos |
| Blog | `/blog` | Blog listing |
| Contact | `/contact` | Contact form and info |
| Booking | `/booking` | Appointment booking |
| Login | `/login` | User login |
| Register | `/register` | User registration |

## 🔐 Authentication Pages

The theme includes premium login and register pages:

### Features
- Modern split-screen design
- Password strength indicator
- Social login buttons (ready for integration)
- Form validation
- Responsive design

### Backend Integration
To make authentication functional, you need to:

1. Set up a backend API (Node.js, PHP, etc.)
2. Create authentication endpoints:
   - `POST /api/auth/login`
   - `POST /api/auth/register`
3. Update form handlers in:
   - `src/pages/login.astro`
   - `src/pages/register.astro`

See `AUTH-PAGES-DOCUMENTATION.md` for detailed integration guide.

## 🌙 Dark Mode

The theme includes a premium dark mode:

### Default Theme
- Default: **Dark Mode**
- Users can toggle between light/dark
- Preference saved in localStorage

### Change Default Theme
Edit `src/layouts/BaseLayout.astro`:
```javascript
// Change 'dark' to 'light' for light mode default
const theme = localStorage.getItem('theme') || 'dark';
```

## 📱 Responsive Design

The theme is fully responsive:
- **Mobile**: < 640px
- **Tablet**: 640px - 1023px
- **Desktop**: ≥ 1024px

All components automatically adapt to screen size.

## 🎨 Design Tokens

Customize the entire design system in `src/styles/design-tokens.css`:

```css
/* Colors */
--color-primary-500: #ec4899;

/* Typography */
--font-primary: 'Inter', sans-serif;
--font-heading: 'Playfair Display', serif;

/* Spacing */
--space-4: 1rem;
--space-8: 2rem;

/* Border Radius */
--radius-lg: 0.75rem;
--radius-xl: 1rem;

/* Shadows */
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
--shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
```

## 🔧 Troubleshooting

### Issue: "npm: command not found"
**Solution**: Install Node.js from https://nodejs.org

### Issue: Port 4321 already in use
**Solution**: 
```bash
# Kill the process using port 4321
# Windows:
netstat -ano | findstr :4321
taskkill /PID <PID> /F

# Mac/Linux:
lsof -ti:4321 | xargs kill -9
```

### Issue: Build errors
**Solution**:
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
npm run build
```

### Issue: Images not showing
**Solution**: 
- Check image paths start with `/` (e.g., `/images/hero.jpg`)
- Ensure images are in `public/` folder
- Check file names match exactly (case-sensitive)

### Issue: Styles not applying
**Solution**:
```bash
# Clear browser cache
# Or hard refresh: Ctrl+Shift+R (Windows) / Cmd+Shift+R (Mac)
```

## 📚 Additional Documentation

Included documentation files:
- `README.md` - Theme overview and features
- `DOCUMENTATION.md` - Complete theme documentation
- `AUTH-PAGES-DOCUMENTATION.md` - Authentication guide
- `CHANGELOG.md` - Version history
- `LICENSE` - License information

## 🆘 Support

### Getting Help
1. Check documentation files
2. Review Astro documentation: https://docs.astro.build
3. Check GitHub issues (if applicable)

### Common Resources
- **Astro Docs**: https://docs.astro.build
- **Astro Discord**: https://astro.build/chat
- **CSS Tricks**: https://css-tricks.com
- **MDN Web Docs**: https://developer.mozilla.org

## ✅ Pre-Launch Checklist

Before deploying to production:

### Content
- [ ] Update all text content
- [ ] Replace placeholder images
- [ ] Update contact information
- [ ] Set correct social media links
- [ ] Review all page content

### SEO
- [ ] Update page titles
- [ ] Update meta descriptions
- [ ] Add Open Graph images
- [ ] Create sitemap
- [ ] Submit to Google Search Console

### Technical
- [ ] Test all pages
- [ ] Test all forms
- [ ] Test on mobile devices
- [ ] Test in different browsers
- [ ] Check loading speed
- [ ] Optimize images
- [ ] Set up analytics (Google Analytics)

### Legal
- [ ] Update privacy policy
- [ ] Update terms of service
- [ ] Add cookie consent (if needed)
- [ ] Check GDPR compliance (if EU)

## 🎉 You're Ready!

Your Beauty Clinic theme is now set up and ready to customize.

### Next Steps
1. ✅ Customize content and images
2. ✅ Update colors and branding
3. ✅ Test all features
4. ✅ Build for production
5. ✅ Deploy to hosting

### Need More Help?
- Review the included documentation
- Check Astro's official docs
- Join the Astro community

---

**Theme Version**: 1.1.0  
**Astro Version**: 6.0.4  
**Last Updated**: March 24, 2026

**Thank you for choosing Beauty Clinic! 🌸**

We hope you create something amazing with this theme.
