# Beauty Clinic Theme - Complete Documentation

## Table of Contents
1. [Installation](#installation)
2. [Project Structure](#project-structure)
3. [Design System](#design-system)
4. [Customization Guide](#customization-guide)
5. [Components](#components)
6. [Pages](#pages)
7. [Animations](#animations)
8. [SEO Configuration](#seo-configuration)
9. [Performance Optimization](#performance-optimization)
10. [Deployment](#deployment)

---

## Installation

### Prerequisites
- Node.js 18.0 or higher
- npm, yarn, or pnpm package manager

### Setup Steps

1. **Install Dependencies**
```bash
cd beauty-clinic-theme
npm install
```

2. **Start Development Server**
```bash
npm run dev
```
The site will be available at `http://localhost:4321`

3. **Build for Production**
```bash
npm run build
```

4. **Preview Production Build**
```bash
npm run preview
```

---

## Project Structure

```
beauty-clinic-theme/
├── public/                 # Static assets
│   ├── favicon.svg        # Site favicon
│   └── robots.txt         # Search engine directives
├── src/
│   ├── components/        # Reusable components
│   │   ├── Header.astro   # Navigation header
│   │   ├── Footer.astro   # Site footer
│   │   └── Hero.astro     # Hero section
│   ├── layouts/           # Page layouts
│   │   └── BaseLayout.astro  # Base HTML structure
│   ├── pages/             # Route pages
│   │   ├── index.astro    # Homepage
│   │   ├── about.astro    # About page
│   │   ├── services.astro # Services page
│   │   └── contact.astro  # Contact page
│   └── styles/            # Global styles
│       ├── design-tokens.css  # Design variables
│       ├── global.css         # Global styles
│       └── animations.css     # Animation utilities
├── astro.config.mjs       # Astro configuration
├── package.json           # Dependencies
└── tsconfig.json          # TypeScript config
```

---

## Design System

### Color Tokens

The theme uses a comprehensive design token system defined in `src/styles/design-tokens.css`.

#### Primary Colors
```css
--color-primary-500: #e25c76  /* Main brand color */
--color-primary-600: #cd3d5e  /* Darker variant */
```

#### Color Schemes
The theme supports multiple color schemes:
- **Rose** (default): Elegant pink tones
- **Purple**: Modern purple aesthetic
- **Emerald**: Fresh green palette
- **Blue**: Professional blue theme

To change the color scheme, add the attribute to your HTML:
```html
<html data-color-scheme="purple">
```

### Typography

#### Font Families
- **Headings**: Playfair Display (serif)
- **Body**: Inter (sans-serif)

#### Font Sizes
```css
--text-xs: 0.75rem
--text-sm: 0.875rem
--text-base: 1rem
--text-lg: 1.125rem
--text-xl: 1.25rem
--text-2xl: 1.5rem
--text-3xl: 1.875rem
--text-4xl: 2.25rem
--text-5xl: 3rem
--text-6xl: 3.75rem
--text-7xl: 4.5rem
```

### Spacing System
```css
--space-1: 0.25rem   (4px)
--space-2: 0.5rem    (8px)
--space-4: 1rem      (16px)
--space-8: 2rem      (32px)
--space-16: 4rem     (64px)
--space-24: 6rem     (96px)
--space-32: 8rem     (128px)
```

### Border Radius
```css
--radius-sm: 0.25rem
--radius-md: 0.5rem
--radius-lg: 0.75rem
--radius-xl: 1rem
--radius-2xl: 1.5rem
--radius-full: 9999px
```

---

## Customization Guide

### Changing Brand Colors

1. Open `src/styles/design-tokens.css`
2. Modify the primary color values:

```css
:root {
  --color-primary-500: #YOUR_COLOR;
  --color-primary-600: #YOUR_DARKER_COLOR;
}
```

### Updating Site Information

1. **Site URL**: Edit `astro.config.mjs`
```javascript
export default defineConfig({
  site: 'https://your-domain.com',
});
```

2. **Business Information**: Edit `src/layouts/BaseLayout.astro`
```javascript
const schemaData = {
  "@type": "MedicalBusiness",
  "name": "Your Clinic Name",
  "address": {
    "streetAddress": "Your Address",
    // ...
  }
};
```

3. **Navigation Menu**: Edit `src/components/Header.astro`
```javascript
const navItems = [
  { name: 'Home', href: '/' },
  { name: 'Your Page', href: '/your-page' },
  // Add more items
];
```

### Adding New Pages

1. Create a new file in `src/pages/`:
```astro
---
import BaseLayout from '@/layouts/BaseLayout.astro';
import Header from '@/components/Header.astro';
import Footer from '@/components/Footer.astro';
---

<BaseLayout 
  title="Your Page Title"
  description="Your page description"
>
  <Header />
  <main>
    <!-- Your content -->
  </main>
  <Footer />
</BaseLayout>
```

2. Add the page to navigation in `Header.astro`

---

## Components

### Header Component

**Location**: `src/components/Header.astro`

**Features**:
- Fixed navigation with scroll effect
- Mobile responsive menu
- Theme toggle (dark/light mode)
- CTA button

**Customization**:
```astro
const navItems = [
  { name: 'Item Name', href: '/path' }
];
```

### Footer Component

**Location**: `src/components/Footer.astro`

**Features**:
- Multi-column layout
- Social media links
- Newsletter subscription form
- Copyright information

**Customization**:
```astro
const footerLinks = {
  company: [...],
  services: [...],
  support: [...]
};
```

### Hero Component

**Location**: `src/components/Hero.astro`

**Props**:
- `title`: Main headline
- `subtitle`: Supporting text
- `ctaText`: Primary button text
- `ctaLink`: Primary button URL
- `secondaryCtaText`: Secondary button text
- `secondaryCtaLink`: Secondary button URL

**Usage**:
```astro
<Hero 
  title="Your Headline"
  subtitle="Your subtitle"
  ctaText="Book Now"
  ctaLink="/booking"
/>
```

---

## Pages

### Homepage (`index.astro`)

**Sections**:
1. Hero - Main banner with CTA
2. Services - Grid of service offerings
3. About - Clinic introduction
4. Testimonials - Client reviews
5. CTA - Final call-to-action

### Services Page (`services.astro`)

**Features**:
- Service cards with pricing
- Treatment lists
- Duration information
- Booking CTAs

**Customization**:
```javascript
const services = [
  {
    id: 'service-id',
    icon: '✨',
    title: 'Service Name',
    description: 'Description',
    treatments: ['Treatment 1', 'Treatment 2'],
    price: 'From $100',
    duration: '60 min'
  }
];
```

### About Page (`about.astro`)

**Sections**:
1. Story - Clinic history
2. Values - Core principles
3. Team - Staff profiles
4. Stats - Key metrics

### Contact Page (`contact.astro`)

**Features**:
- Contact information cards
- Contact form
- Map placeholder (ready for Google Maps)
- Opening hours

---

## Animations

### Scroll Reveal Animations

**Classes**:
- `.reveal` - Fade in from bottom
- `.reveal-left` - Slide in from left
- `.reveal-right` - Slide in from right
- `.reveal-scale` - Scale in

**Usage**:
```html
<div class="reveal">Content</div>
```

### Stagger Delays

Add sequential delays to multiple elements:
```html
<div class="reveal stagger-1">First</div>
<div class="reveal stagger-2">Second</div>
<div class="reveal stagger-3">Third</div>
```

### Hover Effects

**Classes**:
- `.hover-lift` - Lift on hover
- `.hover-scale` - Scale on hover
- `.hover-glow` - Glow effect on hover

### Parallax Effect

Add parallax scrolling:
```html
<div class="parallax" data-speed="0.5">
  <!-- Content -->
</div>
```

Speed values: 0.1 (slow) to 1.0 (fast)

---

## SEO Configuration

### Meta Tags

Each page should include:
```astro
<BaseLayout 
  title="Page Title - Beauty Clinic"
  description="Page description for SEO"
  image="/images/og-image.jpg"
  article={false}
>
```

### Schema Markup

The theme includes structured data for:
- MedicalBusiness
- Organization
- LocalBusiness

Edit in `src/layouts/BaseLayout.astro`

### Sitemap

Automatically generated by `@astrojs/sitemap` integration.

Configure in `astro.config.mjs`:
```javascript
integrations: [
  sitemap()
]
```

### Robots.txt

Located at `public/robots.txt`. Update with your sitemap URL.

---

## Performance Optimization

### Built-in Optimizations

1. **CSS Minification**: Enabled in production
2. **HTML Compression**: Automatic
3. **Image Optimization**: Use Astro's Image component
4. **Code Splitting**: Automatic per-page

### Best Practices

1. **Images**: 
   - Use WebP format
   - Provide width/height attributes
   - Use lazy loading

2. **Fonts**:
   - Preconnect to Google Fonts
   - Use font-display: swap

3. **Animations**:
   - Use CSS transforms (not position)
   - Add `will-change` for animated elements
   - Respect `prefers-reduced-motion`

### Lighthouse Targets

- Performance: 90+
- Accessibility: 95+
- Best Practices: 95+
- SEO: 100

---

## Deployment

### Build Command
```bash
npm run build
```

Output directory: `dist/`

### Deployment Platforms

#### Netlify
1. Connect your repository
2. Build command: `npm run build`
3. Publish directory: `dist`

#### Vercel
1. Import project
2. Framework: Astro
3. Build command: `npm run build`
4. Output directory: `dist`

#### Cloudflare Pages
1. Connect repository
2. Build command: `npm run build`
3. Build output directory: `dist`

### Environment Variables

If needed, create `.env` file:
```
PUBLIC_SITE_URL=https://your-domain.com
```

---

## Browser Support

- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)

---

## Troubleshooting

### Common Issues

**Issue**: Animations not working
**Solution**: Check that JavaScript is enabled and `reveal` classes are applied

**Issue**: Theme toggle not persisting
**Solution**: Ensure localStorage is available and not blocked

**Issue**: Mobile menu not opening
**Solution**: Check that the mobile toggle script is loaded

---

## Support & Updates

For issues or questions:
1. Check this documentation
2. Review the code comments
3. Open an issue on the repository

---

## License

MIT License - Free for personal and commercial use

---

**Version**: 1.0.0  
**Last Updated**: 2026  
**Astro Version**: 6.0.0
