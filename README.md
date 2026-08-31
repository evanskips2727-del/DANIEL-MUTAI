# Daniel Mutai, HSC — Impact Portfolio (v2)

A documented, evidence-first website for Daniel Mutai, HSC — Kenyan teacher,
humanitarian and disability advocate. Built so it can be used when applying
for teacher and humanitarian awards, approaching foundations/NGOs, and
introducing Daniel and the Daniel Mutai Foundation to partners.

## Structure

```
index.html                Homepage — identity, impact passport, pillars
pages/
  story.html               Full life story and timeline
  impact.html               The impact record and five pillars
  projects.html              Programme areas in detail
  recognition.html            Award list with verification status
  foundation.html               Daniel Mutai Foundation
  media.html                      Press and public record
  evidence.html                     Evidence Library / verification system
  contact.html                       Partner / support / media / submit evidence
projects/                   Skeleton for individual, dated project case studies
  mobility/ inclusive-education/ water-sanitation/ eye-health/
evidence/                   Skeleton for supporting documents
  awards/ certificates/ letters/ reports/
assets/
  images/                    Photographs currently on the site
  icons/ documents/            Reserved for future assets
data/
  impact.json recognition.json projects.json media.json
                              Canonical structured data behind each page —
                              update these first when a fact changes, then
                              mirror the change in the matching HTML page.
styles.css                  Shared design system (see tokens at the top of the file)
script.js                    Nav toggle, active-link highlighting, stat count-up
robots.txt / sitemap.xml     Update the domain once one is chosen (see below)
LICENSE.md                   Code: MIT. Content/photos/certificates: all rights reserved.
```

## What's real vs. what's placeholder right now

Every fact currently on the site traces back to either Daniel's public
account, the Nation Media Group feature (10 Sept 2025), or material already
supplied for v1 of this site. Nothing has been invented.

What is **not yet on the site**, because the source documents have not been
supplied:
- The HSC certificate/citation itself, and its exact date
- Teacher of the Year, county, NCPWD, TSC and parliamentary recognition
  certificates or letters
- Daniel Mutai Foundation registration/governance documents
- Individual dated project case studies (only the five programme *pillars*
  are documented in general terms so far)
- Additional photographs, broadcast interviews, and further press coverage

These are marked as "pending" / "TBC" in `pages/recognition.html`,
`pages/evidence.html` and the matching `data/*.json` files rather than
being guessed at. **Drop the real documents into `/evidence` and
`/projects/<pillar>` and update the relevant `data/*.json` + HTML page** —
that's the whole workflow for growing the site.

## Before going live

1. Replace `danielmutai.org` in `robots.txt` and `sitemap.xml` with the
   real domain (or the GitHub Pages URL, if no custom domain yet).
2. Confirm the HSC year and the exact wording of the citation before
   publishing it as fact anywhere beyond "Head of State Commendation."
3. Get written consent for any beneficiary photo or story that names or
   identifies a minor or vulnerable person, before adding it to
   `/evidence` or `/projects`.

## Local preview

No build step — open `index.html` directly in a browser, or serve the
folder with any static file server (e.g. `python3 -m http.server`) so
relative links behave the same as on GitHub Pages.
