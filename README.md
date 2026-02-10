# Cerial Marketing Website

Static landing page for the Cerial mobile app.

## Overview

This is the marketing website for Cerial, featuring:
- Product overview and value proposition
- Waitlist signup form
- Privacy policy
- Responsive design with professional branding

## Backend Integration

This website calls Cloud Functions deployed from the [main Cerial repository](../Cerial).

**Endpoint used:**
- `addToWaitlist` - Captures email signups and sends to EmailOctopus
  - Source code: [Cerial/functions/src/waitlist.ts](../Cerial/functions/src/waitlist.ts)
  - Type: Public HTTPS endpoint (no authentication required)

The website is a static HTML site that communicates with Firebase Cloud Functions for backend operations.

## Deployment

The website is deployed as static HTML. Deployment method: [To be documented based on your hosting choice]

Options:
- Firebase Hosting
- Netlify
- Vercel
- GitHub Pages

## Local Development

1. Clone this repository
   ```bash
   git clone [repository-url]
   cd cerial-website
   ```

2. Open `index.html` in a browser
   ```bash
   open index.html
   ```

3. For waitlist testing:
   - Ensure the Cerial Cloud Functions are deployed
   - The form will submit to the production Cloud Function endpoint
   - Check the browser console for any errors

## File Structure

```
cerial-website/
├── index.html       # Main landing page with waitlist form
├── privacy.html     # Privacy policy page
├── favicon.svg      # Site favicon
└── README.md        # This file
```

## Modifying the Waitlist Flow

- **Form UI**: Edit the HTML form in `index.html`
- **Backend logic**: Edit `waitlist.ts` in the [main Cerial repository](../Cerial/functions/src/waitlist.ts)
- **EmailOctopus integration**: Configure secrets in the Cerial Firebase project

After deploying function changes, the website automatically uses the updated endpoint (no website changes needed).

## Related Repositories

- [Cerial](../Cerial) - Main mobile app and Cloud Functions backend

## Contact

For questions about the Cerial project, see the main repository.
