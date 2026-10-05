# Approved portrait additions — 2026-10-04

## Scope

Local-only implementation of the three approved portrait additions on branch `family-portrait-additions-2026-10-04`, based on main commit `ea08c4e4bb3fa9bd084ab1d77d834e9bb5b15670`.

No push, merge, deployment, parent-photo guess, living-person data change, canonical-vault write, gate/auth/config change, package install, or new download was performed.

## Added

- Robert H. Carlile: `assets/people/robert-carlile-princeton.jpg` (303×404), sourced to his Princeton Alumni Weekly memorial.
- Mary E. Miller Tucker Bucher: `assets/people/mary-tucker-bucher-inkfreenews.jpg` (207×207), sourced to her archived InkFreeNews obituary.
- Jerry D. Nelson: `assets/people/jerry-nelson-rozella-ford-2019.jpg` (500×389), added as a profile-gallery alternate sourced to the 2019 InkFreeNews interview. The Titus obituary portrait remains Jerry’s primary portrait.

The watermarked 2012 Toledo Blade Lena image was not copied or hotlinked. A plain link to the licensed-image gallery was added with an explicit “not reproduced” label; Lena’s existing Grosse Pointe News portrait remains primary.

## UI and source updates

- Replaced Robert and Mary initials states in the album, tree/history thumbnails, and profile media.
- Removed Robert/Mary “photo needed” UI copy and updated the album introduction to describe four source-labeled primary portraits.
- Added source links and rights-neutral captions to Robert and Mary profiles.
- Extended gallery rendering so opening the local image and opening the source article are separate actions.
- Added Mary’s archived obituary link to her profile/history card and the site source list.
- Preserved all established stories, facts, dates, relationships, source data, and Pass 27 research.
- Updated release metadata to `2026-10-04-portraits` and handoff cache marker to `?v=27-portraits`; research remains Pass 27.
- Updated `content/photo-source-manifest-2026-10-04.md` with dated source/image URLs, identity basis, dimensions/checksums, rights status, exclusions, and current counts.

## Verification

Receipt: `screenshots/portraits-test-results.json`

Screenshots:

- `screenshots/portraits-desktop-album.png`
- `screenshots/portraits-mobile-album.png`
- `screenshots/portraits-robert-modal.png`
- `screenshots/portraits-mary-modal.png`
- `screenshots/portraits-jerry-gallery.png`

Existing Playwright Core and the existing Chromium headless shell verified:

- gate appears and unlocks without changing gate policy;
- Pass 27 remains present;
- four album cards load four primary portraits;
- Robert and Mary modal images have expected intrinsic dimensions and correct source links;
- Jerry’s Titus portrait remains primary;
- Jerry’s 2019 alternate loads at 500×389, opens the full local image, and has a separate correct source-article link;
- Enter opens a profile, Escape closes it, and focus returns to the trigger;
- all six local media assets return HTTP 200 with image content types;
- computed album heading uses the sans stack;
- mobile album images retain `object-fit: contain`;
- no horizontal overflow, console errors, page errors, or non-map request failures;
- final screenshots were visually inspected for faces, framing, captions, and layout. Mary remains at source resolution with no upscaling/retouching performed.

## Rights status

All copied portraits are source-labeled. Their source pages do not state republication permission, and this change does not claim permission. The site manifest carries the specific status for each image.
