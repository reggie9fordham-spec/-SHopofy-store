# Customization Guide

## Color Customization

### Update Primary Colors

Edit \`theme.json\`:

\`\`\`json
{
  "color_schemes": {
    "primary": {
      "background": "#ffffff",
      "text": "#000000",
      "accent": "#000000"
    }
  }
}
\`\`\`

### CSS Variables

Modify \`assets/styles.css\`:

\`\`\`css
:root {
  --color-primary: #000000;
  --color-secondary: #ffffff;
  --color-accent: #f4f4f5;
  --color-text: #000000;
}
\`\`\`

## Typography Customization

### Change Font Family

Update \`tailwind.config.js\`:

\`\`\`js
theme: {
  extend: {
    fontFamily: {
      sans: ['Your Font Family', 'sans-serif'],
    },
  },
}
\`\`\`

### Adjust Font Sizes

Modify \`config.json\`:

\`\`\`json
{
  "typography": {
    "heading_size": 48,
    "body_size": 16
  }
}
\`\`\`

## Component Customization

### Update Product Title

Edit \`sections/hero.jsx\`:

\`\`\`jsx
const defaultProduct = {
  title: 'Your Product Title',
  price: 2999, // in cents
  originalPrice: 5999,
};
\`\`\`

### Modify Reviews

Change review data:

\`\`\`jsx
const reviews = [
  {
    name: 'Customer Name',
    role: 'Customer Role',
    review: 'Customer testimonial...',
    rating: 5,
  },
];
\`\`\`

### Edit FAQs

Update FAQ items:

\`\`\`jsx
const faqs = [
  {
    q: 'Your question?',
    a: 'Your answer...',
  },
];
\`\`\`

## Product Settings

### Enable/Disable Features

Modify \`config.json\`:

\`\`\`json
{
  "product": {
    "show_reviews": true,
    "show_inventory": true,
    "enable_quick_shop": true
  }
}
\`\`\`

## Analytics Integration

### Google Analytics

Add your GA4 ID:

\`\`\`json
{
  "marketing": {
    "google_analytics_id": "G-XXXXXXXXXX"
  }
}
\`\`\`

### Facebook Pixel

Add pixel ID:

\`\`\`json
{
  "marketing": {
    "facebook_pixel_id": "YOUR_PIXEL_ID"
  }
}
\`\`\`

## Performance Optimization

### Image Optimization

\`\`\`json
{
  "performance": {
    "lazy_load_images": true,
    "minify_css": true,
    "minify_js": true
  }
}
\`\`\`

## Deployment

### Push Changes

\`\`\`bash
npm run build
shopify theme push
\`\`\`

### Preview Changes

\`\`\`bash
shopify theme dev
\`\`\`

## Support

For help with customization:
1. Check [Shopify Theme Development Docs](https://shopify.dev/themes)
2. Review [Tailwind CSS Docs](https://tailwindcss.com)
3. Open an issue on [GitHub](https://github.com/reggie9fordham-spec/-SHopofy-store/issues)
