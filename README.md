# B&B Premier Cleaning website

A fast, mobile-first site (home page + 8 service pages) for B&B Premier Cleaning, serving Spring Hill, KS and surrounding areas.

## Files
- `index.html` - all home page content and SEO metadata
- `services/<service>/index.html` - one page per service (8 total)
- `css/styles.css` - styles (Style 3 editorial look: deep teal #0f5257 + warm gold #c5a059, Playfair Display headings, Inter body)
- `js/main.js` - mobile nav, scroll effects, and the quote form handler
- `assets/` - images and favicon
- `robots.txt`, `sitemap.xml`, `site.webmanifest` - search engine and PWA files

## Clean URLs (no .html)
Each page is served from an `index.html`. On any standard static host
(Netlify, Vercel, Cloudflare Pages, GitHub Pages, or Apache/Nginx), `index.html`
is served automatically for its folder, so visitors only ever see:

    https://bbpremiercleaning.com/
    https://bbpremiercleaning.com/services/deep-cleaning/

No `.html` ever appears in the address bar. Just deploy the whole folder and point
the domain at it.

## Before you go live
The domain, email and booking link use B&B Premier Cleaning placeholders and should be
confirmed before launch. Search the whole folder for `bbpremiercleaning` and update if
the final domain differs:
   - `https://bbpremiercleaning.com` (canonicals, Open Graph, JSON-LD, `sitemap.xml`, `robots.txt`)
   - `hello@bbpremiercleaning.com` (all pages + `js/main.js`)
   - `bbpremiercleaning.bookingkoala.com` (the booking iframe + preconnect in `index.html`).
1. Phone number: replace the placeholder `(913) 000-0000` in `index.html` and every
   `services/*/index.html` (contact section + footer, and the `tel:` links).
2. Email: `hello@bbpremiercleaning.com` is set as the contact address. Create that
   inbox on the domain, or change it in `index.html`, the service pages and `js/main.js`.
3. Quote form: it currently opens the visitor's email app pre-filled. To collect
   submissions automatically, create a free form at formspree.io and add
   `action="https://formspree.io/f/XXXXXXX" method="POST"` to the `<form id="quoteForm">`.
4. Photos: swap the stock images in `assets/` with real job photos when available.
5. Add the site to Google Business Profile and Google Search Console for local SEO.

## SEO included
- Location-focused title, description, and keywords for Spring Hill, KS
- Open Graph + Twitter cards
- Geo meta tags and `HouseCleaningService` JSON-LD structured data (services,
  service areas, reviews, hours, geo)
- Per-service `Service` and `BreadcrumbList` structured data
- `robots.txt` and `sitemap.xml`
