# Family album refresh — 2026-10-04

## Outcome

Built a local, non-deployed family-album layer on top of Pass 27. The existing research vault, family tree, maps, profile system, sources, password screen, and Pass 27 narrative remain in place.

- Branch: `family-album-refresh-2026-10-04`
- Worktree: `/Users/openclaw/.openclaw/workspace/genealogy/tucker-family-site-album-refresh-2026-10-04`
- Base: `369d83d` (`Pass 27`)
- Public deployment: **not performed**

## What changed

1. Added a new **Family Album** navigation item and section with four core profiles.
2. Added two contextually verified public portraits:
   - Jerry D. Nelson — Titus Funeral Home obituary image.
   - Allene “Lena” Turpin Carlile — portrait printed with her 2021 Grosse Pointe News obituary.
3. Added honest initials/photo-needed states for Robert H. Carlile and Mary E. Miller Tucker Bucher rather than using stock faces.
4. Added portrait thumbnails to the grandparent tree row and the existing Jerry/Mary/Robert/Allene narrative cards.
5. Reworked the existing profile modal into a clearer reading order:
   - Their story
   - Short timeline
   - Key facts / places
   - Why this matters
   - Family connections
   - Sources & confidence
   - Documents & gallery
   - Still researching
6. Added one clearly labeled documentary image: Allene’s commemorative public-safety gym plaque.
7. Improved typography, spacing, mobile cards, button hierarchy, focus visibility, and portrait/placeholder behavior without replacing the existing visual system.

## New human-readable stories

### Jerry D. Nelson

Compact story connects his Burket/Beaver Dam farm upbringing, nearly thirty years of farming, Nelson Beverage, a late start in golf at 23, Indiana Golf Hall of Fame recognition, and the award later carrying his name.

Sources: Titus Funeral Home obituary; Indiana Golf sources already preserved in Pass 8/profile data.

### Allene “Lena” Turpin Carlile

Compact story connects Richmond, Grosse Pointe, and Northern Michigan, then adds the newly verified civic chapter: as Grosse Pointe Park Foundation president, she spearheaded funding for a modern first-responder fitness facility. The department requested $35,000; the foundation committed $50,000; the gym was later dedicated in her memory.

Sources: Grosse Pointe News, Dec. 16, 2021 obituary (physical PDF page 16 / printed 4B); Grosse Pointe News, Jan. 12, 2023 feature (physical PDF page 3 / printed 3A).

### Robert H. Carlile

Shorter public-life narrative emphasizes Columbus Academy, Princeton, Air Force service, banking, aviation, and Northern Michigan. No new genealogy claim was introduced.

Sources: Robert’s existing Princeton Alumni Weekly and Stone Funeral Home links already in Pass 27.

### Mary E. Miller Tucker Bucher

Shorter bridge narrative explains why her obituary is such a strong maternal anchor: it ties her Miller/Parker parents and marriages to the JoAnn → Tara line and the Claypool/Mentone geography.

Source: Hartzler obituary and existing Fulton County index link.

## Photo provenance and permission

Full required fields, identity matching, access notes, captions, source image URLs/pages, and unmatched-photo inventory are in:

- `content/photo-source-manifest-2026-10-04.md`

Counts:

- Authentic, contextually verified portraits: **2**
- Documentary images: **1**
- Core deceased placeholders: **2**
- Living/private photo states: **4**
- Additional interactive deceased/couple anchors left unmatched: **5**

The included images are suitable for this private local review only. Their pages do not state public-republication permission. Before shipping publicly, replace them with family-owned copies or obtain permission from the family/source rights holder.

## Screenshots

Before:

- `screenshots/before-desktop-family-cards.png`
- `screenshots/before-mobile-family-cards.png`

After:

- `screenshots/after-desktop-family-album.png`
- `screenshots/after-mobile-family-album.png`
- `screenshots/after-desktop-open-profile.png`

Machine-readable browser test receipt:

- `screenshots/visual-test-results.json`

## Verification

Playwright using an already-installed Chromium headless shell checked the local site at desktop and mobile viewports.

Passed:

- Password screen is initially visible and unlock flow works.
- Pass 27 text is still present.
- Four album cards render.
- Two album portraits and two core placeholders render.
- Profile modal opens by click and keyboard.
- “Their story” is present.
- Escape and close button close the modal.
- All three local media assets respond successfully.
- No browser console errors, page errors, or non-map request failures were observed.
- Desktop/mobile before-and-after screenshots were visually inspected; no blocker-level clipping or readability defect was found.

Additional static checks are recorded in the final branch verification/commit state.

## Local preview

From the worktree root:

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Then open:

- `http://127.0.0.1:8765/`

No deploy, push, merge, account change, or external contact occurred.

## Known blockers / next decision

1. **Photo rights:** current authentic images have unclear public-republication rights.
2. **Missing portraits:** Robert and Mary remain intentionally unmatched; family-owned images are the best next source.
3. **Older anchors:** five interactive deceased/couple profiles still use text-only profiles because no uniquely attributable image was verified tonight.
4. **Shipping:** branch is local only. Public deployment should wait for Tucker’s explicit shipping decision and photo-rights resolution.
