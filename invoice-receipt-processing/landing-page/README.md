# Invoice/Receipt Processing - Landing Page

Simple landing page for validating demand.

## Files

- `index.html` - Landing page
- `README.md` - This file

## Setup

### 1. Form Handler

Replace the form action in `index.html`:
```html
<form action="https://formspree.io/f/your-form-id" method="POST">
```

Sign up free at [formspree.io](https://formspree.io) to get your form ID.

### 2. Deploy to GitHub Pages

1. Go to repo Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: `main` → `/ (root)`
4. Click Save

Your page will be at: `https://yourusername.github.io/project-explorations/invoice-receipt-processing/landing-page/`

### 3. Custom Domain (Optional)

Add `CNAME` file with your domain:
```
receipts.yourdomain.com
```

Then configure CNAME in your domain provider.

## Validation Metrics

Track in Google Analytics or Formspree:
- Page visits
- Email signups
- Conversion rate (target: 5%+)

## Local Testing

```bash
# Open in browser
open index.html

# Or serve locally
npx serve .
```

## Next Steps

1. ✅ Landing page created
2. ⏳ Configure form handler (Formspree)
3. ⏳ Enable GitHub Pages
4. ⏳ Share on Reddit/social
5. ⏳ Track signups
