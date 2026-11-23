# Cynthia & Nicko — Wedding Website, v2 Exact-Replica Build

Multi-page static replica of https://www.theknot.com/us/cynthia-espinoza-and-nicko-patron-aug-2025
(Cynthia Espinoza and Nicko Patron, Friday, August 29, 2025, The View at Bluemont).
Built November 23, 2026. All assets are local; nothing hotlinks The Knot.

## Structure (URLs match the original paths)

- `index.html` — Home
- `our-story/index.html` — Our Story, 19 milestones
- `photos/index.html` — Photos, 65-photo grid with lightbox
- `wedding-party/index.html` — Wedding Party, 12 people
- `q-a/index.html` — Q + A, 9 questions
- `travel/index.html` — Travel, Dulles and Reagan
- `things-to-do/index.html` — Things to Do
- `registry/index.html` — Registry, 18 gifts with working filters and sort
- `rsvp/index.html` — RSVP overlay flow (no form submission; archive note on submit)
- `styles.css` — shared stylesheet

## Sources

- All text content (Home, Our Story, Wedding Party bios, Q+A, Travel, Things to Do)
  is verbatim from the live text crawl of the original site, reused from the v1
  clone (`~/workspace/wedding-site-clone/index.html`).
- Header images: watercolor floral spray (33daf297) and hanging garland (bc099c1a),
  downloaded from media-api.xogrp.com. Hero photo is the same UUID as the
  original hero (c824c2a6); theknot.com/tk-media is Akamai-blocked to curl, so it
  was fetched via the media-api.xogrp.com mirror of the same UUID and cropped to
  the original 2:1 crop (top half, 2880x1440).
- Venue photo (c457eb73) and wedding-party closing photo (292bae5f) downloaded
  from media-api.xogrp.com.
- Gallery: 65 photos, UUID list in /tmp/gallery.txt, in gallery order.
  Full-size versions verified 65/65 as real JPEG (all over 50 KB) and live in
  `images/gallery/full/gallery-NN.jpg`. The Photos page uses the full-size
  files for both the grid (square-cropped by CSS, lazy-loaded) and the
  lightbox; the smaller 300px thumbnails were dropped at deploy time to keep
  the upload to one set of files.
- Registry: 18 gift items, prices, and statuses came from the live browser visit
  of the original registry page, not from the text crawl (the crawl rendered
  the registry empty). Store attribution per item (The Knot Registry Store /
  Amazon / Etsy) is a best-effort assignment from that same visit so the Store
  filter has something to filter on; it was not independently verifiable per
  item. No outbound purchase links were verifiable, so "Add to cart" buttons
  are presentational only and no data is sent anywhere.
- RSVP: the original RSVP page rendered empty in the text crawl; the flow
  (full-screen overlay, progress bar, Full Name field, "Find Your Invitation")
  was replicated from the live browser visit. Submitting shows an archive note
  that RSVPs closed May 31, 2025 and the wedding has taken place. Nothing is
  submitted anywhere.

## Known differences from the original

- The Knot's own branding/navigation chrome is not reproduced beyond the
  footer "Created on The Knot" credit. The site is a personal copy, not The
  Knot itself.
- Fonts: Cormorant Garamond (Google Fonts) is used as the closest match to The
  Knot's Didone-style serif; the exact licensed font files were not available.
- The original 66-photo gallery count seen in the text crawl vs 65 verified
  gallery UUIDs: the gallery list used here is the 65 UUIDs verified with curl.
- Registry item images were not captured; gift cards use text only.
