# Big Cheese Kettle Co — NFC Dashboard

A single-page contact & social hub meant to be opened when someone taps your NFC tag.

## What's included

- **Business name** ("Big Cheese Kettle Co") at the top
- **Banner** and **profile photo** slots (placeholders shown until you add your own images)
- **Instagram**, **Facebook**, and **Venmo** links, in that order, to `bigcheesekettleco` / `@joshua-lovett-23`
- **Contact Information** button — downloads a vCard (`assets/contact.vcf`) with name, business, phone, and email so it's added straight to the visitor's phone contacts
- **Website** link to `www.bigcheesekettleco.com`

## Adding your banner and profile photo

Drop your own images into the `assets/` folder using these exact filenames — no code changes needed:

- `assets/banner.jpg` — recommended ~1200x400px (wide, landscape)
- `assets/profile.jpg` — recommended ~500x500px (square, will be cropped to a circle)

Until those files exist, placeholder graphics are shown automatically.

## Updating contact details

- Phone, email, and social links live in `index.html` (search for the `link-btn` entries) and in `assets/contact.vcf`.
- Update both places if a phone/email ever changes so the "Contact Information" download stays in sync with the page.

## Hosting it (so the NFC tag has a URL to open)

The site is plain static HTML/CSS/JS — no build step. Easiest option is GitHub Pages:

1. Push this repo to GitHub (already done if you're reading this from the repo).
2. In the repo settings, go to **Pages** and set the source to the `main` branch, root folder.
3. GitHub will give you a URL like `https://<username>.github.io/<repo>/`.

Any static host works too (Netlify, Vercel, Cloudflare Pages, S3, etc.) — just upload the folder.

## Writing the NFC tag

Once the site is live at a URL:

1. Install an NFC-writing app on your phone (e.g. **NFC Tools** on iOS/Android).
2. Add a new record → **URL/URI** → paste your site's URL.
3. Write it to the tag.
4. Tap the tag with a phone to confirm it opens the dashboard.
