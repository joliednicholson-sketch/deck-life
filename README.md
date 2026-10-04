# Deck Life Service website

Static website for **decklifeservice.com**. It's plain HTML and CSS, so there's no build step.

## Files

- `index.html`: page content
- `styles.css`: styling
- `assets/`: favicon and project photos
- `CNAME`: tells GitHub Pages to serve the site at decklifeservice.com
- `.github/workflows/pages.yml`: deploys to GitHub Pages on every push to `main`

## Placeholders to replace

Search `index.html` for these:

- `(555) 555-5555` / `+15555555555`: your phone number
- `info@decklifeservice.com`: your email
- `[YOUR CITY]` / `YOUR CITY, ST`: your service area
- `[Tell your story here…]`: the About section
- `YOUR_FORM_ID`: create a free form at https://formspree.io and paste its ID so estimate requests go to your inbox
- Gallery: put photos in `assets/` and replace each `<figure class="ph">` with `<img src="assets/photo1.jpg" alt="Restored cedar deck">`

## Going live

1. Merge to `main`.
2. In the GitHub repo, open **Settings → Pages** and set **Source** to **GitHub Actions**.
3. At your domain registrar, add these DNS records for `decklifeservice.com`:
   - Four `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record for `www` pointing to `joliednicholson-sketch.github.io`
4. Back in **Settings → Pages**, check that the custom domain reads `decklifeservice.com`. Once DNS has propagated, turn on **Enforce HTTPS**.

## Local preview

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.
