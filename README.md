# Cynthia & Nicko — Wedding Website Archive

Personal archive copy of the wedding website of Cynthia Espinoza and Nicko Patron,
originally at https://www.theknot.com/us/cynthia-espinoza-and-nicko-patron-aug-2025
Wedding: Friday, August 29, 2025, 5:00–11:00 PM, The View at Bluemont,
19729 Ridgeside Road, Bluemont, VA 20135. Archived November 23, 2026.

## What was copied

Source pages were read on 2026-11-23 (all confirmed live that day) and their
text was copied verbatim into this single-page static site (`index.html`,
`styles.css`). No The Knot branding, logos, or navigation chrome was copied.
The design is a simple, clean original layout.

| Section | Source page | Status |
|---|---|---|
| Home | `/` | Copied in full: date, venue, attire, white-dress note, reception, banner + venue photos |
| Our Story | `/our-story` | Copied in full: all 19 milestones (2013 meet → 2024 proposal) with text and all 23 photos |
| Photos | `/photos` | Partial — see below |
| Wedding Party | `/wedding-party` | Copied in full: 6 bridesmaids + 6 groomsmen, names, roles, bios, all 13 photos |
| Q + A | `/q-a` | Copied in full: all 9 questions and answers |
| Travel | `/travel` | Copied in full: Dulles + Reagan National airports with addresses, phones, drive times |
| Things to Do | `/things-to-do` | Copied as-is: the page only said "Things to Do coming soon!" |
| Registry | `/registry` | Not readable — see below |
| RSVP | `/rsvp` | Not readable as a form (and past deadline) — presented as archive text only, no form, nothing submits anywhere |

## Photos

40 image files saved locally in `images/` (13 MB total), all downloaded from
The Knot's media CDNs (`theknot.com/tk-media` and `media-api.xogrp.com`) at
the quality the source pages served. Nothing is hotlinked to The Knot.

- `banner.jpg` — homepage banner; `theme-1.png`, `theme-2.jpg` — theme images
- `venue.jpg` — The View at Bluemont photo from the homepage
- `story-01` … `story-23` — all Our Story photos, in page order
- `party-alejandra.jpg`, `party-faviola.jpg`, `party-claudia.jpg`,
  `party-cadence.jpg`, `party-carolina.jpg`, `party-jen.jpg`,
  `party-mohmeet.jpg`, `party-jared.jpg`, `party-aaron.jpg`,
  `party-rory.jpg`, `party-james.jpg`, `party-abraham.jpg`, `party-group.jpg`

## What could not be captured (honest gaps)

1. **Photo gallery (66 photos):** the `/photos` page lists 66 gallery photos
   (Gallery Photo 1–66), but the text crawl of the page and of individual
   photo pages (`/photos/<id>`) never exposed their image URLs, and direct
   fetches of theknot.com pages are blocked by Akamai (HTTP 403, "Access
   Denied"). The Photos section here therefore reuses the 40 saved photos
   (banner, venue, story, wedding party) as the gallery. If the couple still
   has the originals, they can be added to `images/` and the gallery grid.
2. **Registry links:** the `/registry` page rendered empty in the text crawl
   (its content loads via JavaScript). No registry retailer or link could be
   verified, so none is listed here; the page links back to the original
   registry URL instead.
3. **RSVP form:** the `/rsvp` page rendered empty in the text crawl. The
   wedding already happened and the RSVP deadline (May 31, 2025, per Q&A)
   had passed, so no form was rebuilt. The RSVP deadline is preserved in
   the Q&A section.

## Deployment

Deployed to Vercel as a static site (see project name / URL in the delivery
report). To redeploy: create a Vercel project from this folder as a static
site (no build command) or run a static deploy of `index.html`,
`styles.css`, and `images/`.
