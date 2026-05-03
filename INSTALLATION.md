# Shopify Theme Installation Guide

## Prerequisites

Before you begin, ensure you have:
- A Shopify development store or partner account
- Node.js 16+ installed
- npm or yarn package manager
- Git installed

## Step-by-Step Installation

### 1. Clone the Repository

\`\`\`bash
git clone https://github.com/reggie9fordham-spec/-SHopofy-store.git
cd -SHopofy-store
\`\`\`

### 2. Install Shopify CLI

\`\`\`bash
npm install -g @shopify/cli @shopify/theme
\`\`\`

Verify installation:
\`\`\`bash
shopify --version
\`\`\`

### 3. Install Dependencies

\`\`\`bash
npm install
\`\`\`

### 4. Authenticate with Shopify

\`\`\`bash
shopify auth login
\`\`\`

### 5. Build CSS

\`\`\`bash
npm run build
\`\`\`

### 6. Push Theme to Shopify

\`\`\`bash
shopify theme push
\`\`\`

### 7. Preview Theme

\`\`\`bash
shopify theme dev
\`\`\`

### 8. Publish Theme

Once satisfied, go to Shopify Admin → Online Store → Themes and publish your theme.

## Development Workflow

### Making Changes

1. Edit files in \`sections/\`, \`templates/\`, or \`assets/\`
2. Changes are automatically synced during \`shopify theme dev\`
3. Refresh your browser to see updates

### Linting & Formatting

\`\`\`bash
npm run lint
npm run format
\`\`\`

## Troubleshooting

### Theme Won't Push
1. Check authentication: \`shopify auth status\`
2. Re-authenticate: \`shopify auth logout && shopify auth login\`

### CSS Not Applying
1. Rebuild CSS: \`npm run build\`
2. Clear browser cache (Cmd+Shift+R)

### Cart Not Working
1. Check browser console for errors
2. Verify Shopify routes are available

## Next Steps

1. Customize colors in \`theme.json\`
2. Add your products in Shopify Admin
3. Configure analytics
4. Set up shipping and payments

## Resources

- [Shopify Theme Development](https://shopify.dev/themes)
- [Shopify Liquid Documentation](https://shopify.dev/api/liquid)
- [Tailwind CSS Documentation](https://tailwindcss.com)
