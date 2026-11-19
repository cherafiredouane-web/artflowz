# ARTFLOW website

A responsive bilingual (French / Arabic) static storefront built from the supplied ARTFLOW artwork archive.

## Run locally

Because the catalog is loaded from `catalog.json`, serve this folder over HTTP rather than opening `index.html` directly.

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a GitHub repository and upload the contents of this folder (the files inside `artflow website/`, not the parent folder).
2. Open **Settings → Pages**.
3. Select **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. Wait for the deployment to finish. The site is static and does not require a server, API key, or build step.

## Included

- Full-bleed homepage hero using the supplied `Hero.png` image, optimized as WebP.
- Supplied ARTFLOW logo and favicon.
- 270 unique catalog artworks, deduplicated by exact file content while preserving category memberships.
- 18 designated bestsellers.
- Six official categories.
- French and Arabic interface with RTL support.
- Search, category and dominant-colour filters, sorting, favorites stored in local storage, artwork detail modal, size selection, and WhatsApp ordering.
- Artwork pairing and custom-artwork WhatsApp inquiry.
- Responsive layouts and reduced-motion support.

## Catalog note

The supplied archive contained artwork files but no separate product metadata file. Product reference IDs and display names are therefore generated from the asset inventory; descriptive filenames are cleaned up and non-descriptive Artboard filenames receive neutral Composition labels. Original source filenames are retained in `catalog.json`. Dominant colours are sampled from the artwork files because no colour-assignment metadata was included. The archive did not include a separate Arabic product-title translation file, so artwork titles remain in their source-language form in the Arabic interface; all interface copy and category labels are translated. No additional artwork, size, or price options were introduced. The original full-resolution artwork archive is preserved separately in the uploaded source ZIP. The three confirmed formats and prices are 60 × 40 cm (230 DH), 80 × 60 cm (280 DH), and 85 × 110 cm (342 DH).
