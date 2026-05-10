Beauty Clinic website built with Astro v6.

![Astro](https://img.shields.io/badge/Astro-6.0.4-FF5D01?style=flat-square&logo=astro)
![TypeScript](https://img.shields.io/badge/TypeScript-Ready-3178C6?style=flat-square&logo=typescript)
![License](https://img.shields.io/badge/License-Commercial-green?style=flat-square)

## ✨ Key Features

- 🎨 **Premium Dark/Light Mode** - Ultra-dark theme with smooth transitions
- 🔐 **Authentication Pages** - Modern login and register pages included
- 📱 **Fully Responsive** - Mobile-first design, perfect on all devices
- ⚡ **Performance Optimized** - Lighthouse score 95+
- ♿ **Accessibility Compliant** - WCAG guidelines followed
- 🎯 **9 Complete Pages** - Ready to use out of the box
- 🌈 **Customizable Colors** - Easy to match your brand
- ✨ **Advanced Animations** - Smooth, polished interactions

## 📄 Pages Included

1. **Homepage** - Hero, services, testimonials, pricing, FAQ
2. **About** - Company story, team, values
3. **Services** - Treatment listings with details
4. **Doctors** - Team profiles and expertise
5. **Gallery** - Before/after showcase
6. **Blog** - Article listings and posts
7. **Contact** - Contact form and information
8. **Booking** - Appointment scheduling
9. **Login** - User authentication (premium design)
10. **Register** - User registration (premium design)

## 🚀 Quick Start

```bash
# 1. Extract the theme
unzip beauty-clinic-theme.zip

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev

# 4. Open browser
http://localhost:4321
```

That's it! Your theme is running. 🎉

## 📋 Requirements

- Node.js 18.14.1 or higher
- npm 9.0.0 or higher

## 🎨 Customization

### Change Colors

Edit `src/styles/design-tokens.css`:

```css
--color-primary-500: #ec4899; /* Your brand color */
```

### Update Content

Edit page files in `src/pages/`:

- `index.astro` - Homepage
- `about.astro` - About page
- And so on...

### Add Images

Place images in `public/images/` and reference:

```astro
<img src="/images/your-image.jpg" alt="Description" />
```

## 🌐 Build & Deploy

```bash
# Build for production
npm run build

# Preview production build
npm run preview
```

Deploy the `dist/` folder to:

- Vercel (recommended)
- Netlify
- GitHub Pages
- Any static hosting

## 📚 Documentation

Comprehensive documentation included:

- `INSTALLATION-GUIDE.md` - Complete setup guide
- `DOCUMENTATION.md` - Full theme documentation
- `AUTH-PAGES-DOCUMENTATION.md` - Authentication integration
- `CHANGELOG.md` - Version history

#

## 🔧 Technical Stack

- **Framework**: Astro 6.0.4
- **Styling**: CSS (Custom Properties)
- **TypeScript**: Full support
- **Icons**: SVG (inline, no dependencies)
- **Fonts**: Google Fonts (Inter + Playfair Display)

## 📊 Performance

- First paint: < 1s
- Interactive: < 1.5s
- Lighthouse score: 95+
- SEO optimized
- Accessibility: WCAG AA

### Homepage Sections

- Animated hero with statistics
- Service cards with pricing
- Why choose us features
- Before & after gallery
- Doctor profiles
- Client testimonials
- Pricing packages
- FAQ accordion
- Awards & certifications
- Call-to-action sections

### Authentication Pages

- Modern split-screen design
- Password strength indicator
- Social login ready
- Form validation
- Responsive layout
- Dark mode optimized

### Design System

- Comprehensive design tokens
- Consistent typography
- Unified spacing system
- Premium button variants
- Card component library
- Animation presets

## 📱 Responsive Breakpoints

- Mobile: < 640px
- Tablet: 640px - 1023px
- Desktop: ≥ 1024px

## 🎨 Color Schemes

4 pre-configured schemes:

- Rose (default)
- Purple
- Emerald
- Blue

## ✅ What's Included

```
beauty-clinic-theme/
├── src/
│   ├── components/      # Reusable components
│   ├── layouts/         # Page layouts
│   ├── pages/           # 9 complete pages
│   └── styles/          # Design system
├── public/              # Static assets
├── Documentation files
├── package.json
└── Configuration files
```

## 🆘 Support

- Complete documentation
- Astro community support
- Regular updates

## 📜 License

Commercial license included. See LICENSE file for details.

1. Extract the theme
2. Run `npm install`
3. Run `npm run dev`
4. Customize and deploy!

---

**Version**: 1.1.0  
**Last Updated**: March 24, 2026  
**Astro Version**: 6.0.4
