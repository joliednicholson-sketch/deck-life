# Deck Life Service website

Static website for **decklifeservice.com**, the site for Deck Life Service LLC, a boat decking company in Wilmington, NC. It's plain HTML and CSS, so there's no build step.

## Files

- `index.html`: page content
- `styles.css`: styling
- `assets/`: favicon and project photos
- `CNAME`: tells GitHub Pages to serve the site at decklifeservice.com
- `.github/workflows/pages.yml`: deploys to GitHub Pages on every push to `main`

## Placeholders to replace

Search `index.html` for these:

- `matt@decklifeservice.com`: your email (change it if you use a different address)
- `YOUR_FORM_ID`: create a free form at https://formspree.io and paste its ID so booking requests go to your inbox
- Gallery: photos live in `assets/gallery/`. To add one, copy a `<figure class="g …">` block in the gallery section and point it at the new file
- Hours (`Mon–Sat, 8am–5pm`) and the services and materials lists, if they differ from what you offer

If you'd rather have customers pick an exact time slot, the booking form can be swapped for a Calendly (or similar) embed.

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
