# TurboKit Landing Page

Public marketing website for TurboKit SaaS boilerplate.

## Structure

```
landing-page/
├── pages/              # Landing page routes
│   ├── index.vue      # Homepage
│   ├── pricing.vue    # Pricing page
│   ├── features.vue   # Features page
│   └── docs.vue       # Redirect to docs
├── components/        # Landing-specific components
│   ├── Hero.vue
│   ├── Features.vue
│   ├── Pricing.vue
│   ├── Testimonials.vue
│   └── CTA.vue
├── assets/           # Images, videos
└── public/           # Static files
```

## Pages

### Homepage (`pages/index.vue`)
- Hero section with main CTA
- Problem/solution section
- Feature highlights
- Social proof (maker avatars, badges)
- Testimonials
- Final CTA before footer

### Pricing (`pages/pricing.vue`)
- Three-tier pricing table
- Feature comparison
- FAQ section
- Contact/support links

### Features (`pages/features.vue`)
- Detailed feature breakdowns
- Integration partners
- Time-saving metrics
- Use case examples

## Components

### Hero
Main value proposition with CTA button.

```vue
<Hero
  title="Ship your SaaS in days, not weeks"
  subtitle="Modern boilerplate with Nuxt, Stripe, and Resend"
  :cta="{ text: 'Get Started', href: '/docs' }"
/>
```

### Features
Showcase key features with icons.

```vue
<Features
  :items="[
    { icon: 'zap', title: 'Lightning Fast', desc: '100 Lighthouse score' },
    { icon: 'lock', title: 'Secure by Default', desc: 'Built-in auth & payments' },
  ]"
/>
```

### Pricing
Display pricing tiers.

```vue
<Pricing
  :tiers="[
    { name: 'Starter', price: 199, features: [...] },
    { name: 'All-in', price: 249, features: [...] },
  ]"
/>
```

### Testimonials
Customer quotes and logos.

```vue
<Testimonials
  :quotes="[
    { author: 'John', company: 'Acme', text: 'Saved us weeks!' },
  ]"
/>
```

## Content

Update text in components to match your brand:

1. **Title & Description** - In `pages/index.vue`
2. **Features List** - In `components/Features.vue`
3. **Pricing Plans** - In `components/Pricing.vue`
4. **Testimonials** - In `components/Testimonials.vue`
5. **Colors** - In `tailwind.config.ts`

## Links

Update these links throughout:

- `/docs` → Your documentation site
- `/purchase` → Stripe checkout or product link
- Contact email
- Social media links

## Assets

Place in `assets/`:

- `logo.svg` - Your brand logo
- `hero.png` - Hero section image
- `feature-*.png` - Feature screenshots
- `testimonial-*.jpg` - Customer photos

## SEO

Meta tags configured in:

```vue
<script setup>
useHead({
  title: 'TurboKit - Ship Your SaaS Fast',
  meta: [
    { name: 'description', content: '...' },
    { property: 'og:image', content: '/og-image.png' },
  ]
})
</script>
```

## Customization Checklist

- [ ] Update hero title and subtitle
- [ ] Add your logo to public/
- [ ] Update feature descriptions
- [ ] Set pricing tiers
- [ ] Add testimonials
- [ ] Update footer links
- [ ] Set brand colors in Tailwind
- [ ] Add product images
- [ ] Setup analytics
- [ ] Submit sitemap to Google

## Performance

- Auto-optimized images
- 100 Lighthouse score target
- Static prerendering for fast loads
- CDN-ready

## Analytics

Add your tracking:

```vue
<script setup>
// Google Analytics
useHead({
  script: [
    {
      src: 'https://www.googletagmanager.com/gtag/js?id=GA_ID',
      async: true
    }
  ]
})
</script>
```

## Deployment

Deploy to same platform as boilerplate:

```bash
# Build
npm run build

# Deploy to Vercel
vercel deploy --prod
```

Or create separate landing page project for A/B testing.

---

See main [SETUP.md](../SETUP.md) for full project documentation.
