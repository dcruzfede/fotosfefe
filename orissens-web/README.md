# orissens-web — PROVISIONAL

Scraped from the public https://www.orissens.com on 2026-10-28 as **stand-ins** while the HQ set was
prepared by marketing.

**The HQ set arrived on 2026-10-29** (260 files, 12 categories) and is now in the curated library —
`assets/orissens/photos.json`, 172 → 319 entries. The **101** entries here whose shot it covers carry
`superseded_by` naming the curated key. The remaining 214 (blog, social, team, brand, banners) have no
counterpart in it, so this folder stays for now.

⚠️ **Do not delete a superseded file before checking `photos.json`.** The trove ships the three product
carousel slides (beneficios / ingredientes / modelo) at **1200x1200** while the site serves them at
**1800x1800** — so for **45** of them the library points at the file *here*, not at the trove's copy.
Deleting those breaks the library.

- 315 images + `web-images.json`, which records each file's source URL, byte size and dimensions.
- Normalised to the CDN **originals**: the site serves thumbor-resized variants, so 454 referenced
  URLs collapse to 315 distinct files. Stripping the transform segments (`fit-in/WxH/`,
  `filters:format(webp)/`) matters — without it, 82 of the product-carousel images come down as
  400x400 thumbnails instead of full size.
- NOT in `assets/orissens/photos.json` on purpose. That manifest is the curated set a deck build
  picks from; mixing provisional scrapes into it would let a low-res stand-in win over a real photo.
- Excluded from the scrape (see `excluded.txt` in the session notes): third-party widget assets
  (themepunch / elfsight / twitter) and FarmaOffice platform UI — not Orissens-owned.

⚠️ `blog/` holds 20 iStock images. Diana confirmed on 2026-10-28 that the licence is held. Note that
this repo is PUBLIC and served by jsDelivr, so these files are downloadable as standalone assets by
anyone — a use that a standard stock licence does not usually grant. If the licence terms are ever
revisited, `blog/` is the folder to re-check.
