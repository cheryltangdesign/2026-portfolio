# Images

Drop the artwork in here using the paths below. Until a file exists, the page
renders a grey slot labelled with the image's `alt` text, so the layout stays
intact and you can see what belongs where.

Squares on the Work and More grids are cropped to 1:1 (`object-fit: cover`),
so supply them square or close to it.

Everything marked `[done]` was generated from the originals under `mockups/` —
regenerate from those if you need a different crop or size. Grid tiles are
1000 × 1000; the Sandbox VR shots are sized to roughly 1.5× their display size.

```
logo.png                                CT monogram, header (~40 × 40)   [done]

work/                                   home page grid, square           [done]
  sandbox-vr.jpg
  hand-tracker.jpg
  nokia-earbuds.jpg
  nursery-pal-glow.jpg
  mimo.jpg
  maskfone.jpg

more/                                   more page grid, square           [done]
  netflix-house.jpg
  motorola-headphones.jpg
  hubble-scale.jpg
  hubble-grip.jpg
  high-tide-screen.jpg
  isometric-illustration.jpg

about/
  portrait.jpg                          square                           [done]
  logos/                                transparent PNG or SVG, ~3:1
    netflix.svg
    nokia.svg
    holland-and-barrett.svg
    motorola.svg
    wall-theory.svg
    hubble-connected.svg

tools/                                  app icons on the project hero, square
  solidworks.svg
  keyshot.svg
  photoshop.svg
  illustrator.svg

sandbox-vr/                             project page                     [done]
  hero.jpg                              3:2
  moodboard.jpg                         1200:809 collage
  sketches.jpg                          16:9, sits left of models.jpg
  models.jpg                            3:4 portrait
  diagram-tracking.jpg                  2:1, white ground, contained not cropped
  diagram-wireless.jpg                  2:1, white ground, contained not cropped
  feature-*.jpg                         4:3 × 6 — sliced out of one 2×3 composite
  testing-rig.jpg                       4:5
  testing-leds.jpg                      4:5
  cmf.gif                               2:1, 2-frame animation of the player LEDs
  ui-callouts.jpg                       2:1, white ground, contained not cropped
  full-set.jpg                          4:3
  context-1.jpg, -2, -4                 4:3
  context-3.jpg                         3:2

limbs-tracker/                          project page                     [done]
  hero.jpg                              3:2
  problem-a.png, problem-b.png          transparent, sit on the page ground
  concept-velcro/-watch/-magnetic.png   transparent cards incl. their own text
  sketches.jpg                          16:9
  modularity.mp4 / .webm                4:3, loops through the player colours
  anthropometry.jpg + sizing.jpg        stacked on one white sheet
  magnets-diagram.jpg                   top of the magnets white sheet
  magnets-straps.mp4 / .webm            bottom of the same sheet
  gear-up-wrist.mp4 / .webm             1:1
  gear-up-ankle.mp4 / .webm             1:1
  flap-wrist.jpg, flap-ankle.jpg        3:4
  cmf.jpg                               4:3, white ground
  branding.jpg                          4:3
  full-set.jpg                          1:1, white ground
  full-set-detail.jpg                   4:3
  context-1.jpg … context-3.jpg         4:3
```

The six Sandbox VR `feature-*.jpg` files come out of `ATH_20260525-02.png`,
which ships as a single 2 × 3 composite. The Limbs Tracker `problem-*.png`
pair and the three `concept-*.png` cards are flat artwork that includes its own
typography, so they are placed as images rather than rebuilt in HTML.

The four Limbs Tracker animations arrive as GIFs totalling ~110 MB. They are
served as MP4 + WebM `<video autoplay muted loop playsinline>` instead, which
brings them under 4 MB. Re-encode with ffmpeg if the sources change — extract
frames with Pillow first, since ffmpeg mis-composites these GIFs' partial
frames and leaves visible seams.

## Other project folders

`hubble-grip/`, `hubble-growth/`, `maskfone/`, `mimo/`, `motorola-headphones/`,
`netflix-house/`, `nokia-earbuds/`, `nursery-pal-glow/`, `urban-composition/`,
and `wall-theory/` hold assets for project pages built in earlier sessions.
Their sources came in as raw camera/render originals (some 6000–14000px,
several tens of MB each — 582 MB total). They've since been downsized in
place: JPEGs and PNGs capped to a 1800px long edge (600px for `logo-05.png`,
which only displays at 180×130) and re-saved at JPEG quality 85 / optimized
PNG, same filenames and paths so no HTML changes were needed. Total is now
~110 MB. Regenerate from `mockups/` if you need the original resolution back.

Two animated GIFs didn't survive that treatment — Pillow's GIF re-encoder
handles photographic content far worse than whatever produced the originals,
and made both files *larger*. Both were restored from `mockups/` untouched:

- `netflix-house/8c7b2dc4fdb7e111.gif` (22 MB, 68 frames) — replaced instead
  with `netflix-house/stage-wall.mp4` / `.webm` (~1.2 MB total) and the
  `<img>` in `netflix-house.html` swapped for `<video autoplay muted loop
  playsinline>`, the same treatment as the Limbs Tracker clips.
- `nursery-pal-glow/F90_hero 06.gif` (38 MB) — not referenced by any HTML
  (dead asset), so it was just restored rather than converted. Safe to delete
  if it's not needed for something not yet built.
