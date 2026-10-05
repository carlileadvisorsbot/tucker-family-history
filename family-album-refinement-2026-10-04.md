# Family album refinement — 2026-10-04

## Scope and status

Small second polish pass on the existing local `family-album-refresh-2026-10-04` branch and worktree. This is a private preview only. It was not pushed, merged, deployed, or made live.

The family facts, dates, relationships, source URLs, Pass 27 material, quoted obituary language, research vault, and photo-source manifest were preserved. Photo-reuse permission remains unproven for the two public obituary portraits and the documentary image.

## What changed

- Replaced the Georgia/Times heading treatment with the existing local/system sans-serif stack. Headings are smaller, lighter, and less tightly spaced.
- Shortened the album headline to “People in our family” and removed interface copy about placeholders, evidence, and “room to breathe.”
- Rewrote the four album cards and their profile stories as plain, source-backed family history.
- Quieted portrait/source labels and changed missing-photo labels to “Photo needed.”
- Removed the redundant “Why this matters” panel from the four featured profiles while preserving the underlying research data.
- Reduced album-card radius and shadow without changing the cream, green, and photo-led visual identity.
- Changed mobile album portraits to wide 16:10 headers with `object-fit: contain`. Jerry’s full face and portrait are visible instead of appearing in a narrow 96 px strip.
- Kept the desktop album at four cards in a two-column grid.

## Copy examples

1. **Jerry card**
   - Before: “A Kosciusko County life that moved from farm fields to Nelson Beverage to Indiana golf — without losing its small-town center.”
   - After: “Jerry farmed in Kosciusko County for nearly thirty years, bought the distributorship that became Nelson Beverage in 1984, and entered the Indiana Golf Hall of Fame in 1995.”

2. **Robert card**
   - Before: “Columbus Academy, Princeton, banking, aviation, and Northern Michigan form the public outline of Robert’s life.”
   - After: “Robert attended Columbus Academy and Princeton, served as an Air Force officer, worked in banking, and retired in Northern Michigan.”

3. **Mary profile**
   - Before: “Mary’s obituary does unusually heavy genealogical work… That makes Mary one of the strongest maternal anchors…”
   - After: “Mary was born in Claypool in 1916 to Cloyce Miller and Roxie Parker Miller. She married Edison C. Tucker in 1937 and later married C. Edward Bucher. She died in Winona Lake in 2015 and was buried at Mentone Cemetery.”

## Verification

Browser receipt: `screenshots/sans-polish-test-results.json`

Screenshots:

- `screenshots/sans-desktop-family-album.png`
- `screenshots/sans-mobile-family-album.png`
- `screenshots/sans-desktop-open-profile.png`

Playwright with the already-installed Chromium headless shell verified:

- password gate is visible and unlocks;
- Pass 27 remains present;
- four album cards render in a two-column desktop grid;
- computed heading fonts contain no Georgia or Times New Roman;
- Jerry’s mobile image is a 364 × 228 wide header using `object-fit: contain`;
- no desktop or mobile horizontal overflow;
- click and keyboard open the profile modal;
- Escape and the close button close it;
- “Their story” is present and “Why this matters” is absent from a featured profile;
- all three local media assets return 200;
- no console errors, page errors, or non-map request failures.

## Not live

No deployment, push, merge, external contact, new research, font installation, package installation, authentication change, or gateway/configuration change was performed.
