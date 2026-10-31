# Simple Splash Page

A simple, static, single-page splash site for Wright Ideas LLC. It has no build step and no framework. It is plain HTML, CSS, and a little vanilla JavaScript.

## Features

- Full-screen splash layout with a dotLottie animation, logo, headline, and calls to action
- Light and dark themes, controlled by a toggle in the upper-right corner and remembered in localStorage
- Theme colors defined as CSS variables, so the look can be changed in one place
- Logo swaps automatically to match the active theme
- Contact form hosted on Cognito Forms
- Full SEO setup: meta description, canonical URL, Open Graph, Twitter Card, and JSON-LD structured data
- Reduced-motion and safe-area support for mobile devices


## Theming

All colors are CSS variables defined in the `THEME TOKENS` block of `index.html`:

- `:root` holds the light theme (default), with background `#FBBE0D` and text `#845415`.
- `[data-theme="dark"]` holds the dark theme.

To change the look, edit these variables. The whole page updates without touching the layout. The `theme-color` meta tag is updated automatically from `--color-bg` when the theme changes.

## Dependencies (loaded from CDNs)

- **Inter** font via Google Fonts
- **dotLottie web component** (`@lottiefiles/dotlottie-wc@0.6.2`) via jsDelivr

To update the dotLottie version, change the pinned version in the script tag and test the animation. Pinning avoids surprise breaking changes.

## Contact form

The "Let’s Talk" button links to a Cognito Forms inquiry form. Submissions are handled by Cognito Forms. Edit the form there, and update the link in `index.html` if the form URL changes.

## Deployment

This is static, so it can be hosted on any static host, such as Netlify, Vercel, GitHub Pages, Cloudflare Pages, or a traditional web server. Make sure:

- `index.html` is at the site root
- `assets/` and `favicon/` paths match what the HTML references
- The site is served over HTTPS
- Root-relative paths (starting with `/`) resolve correctly on your host

## Privacy notes

The site sets no tracking cookies. It stores one localStorage value (`theme`) to remember the visitor's light or dark choice, and the contact form data is collected by Cognito Forms. The privacy policy in `privacy.html` describes this. Have it reviewed before publishing, especially if you add analytics or other third-party services later.


## License

Copyright © 2026 Wright Ideas LLC. All rights reserved.
