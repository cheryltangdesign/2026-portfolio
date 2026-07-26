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
```

The six `feature-*.jpg` files come out of `ATH_20260525-02.png`, which ships as
a single 2 × 3 composite; the slice coordinates are in the git history if you
need to redo them.
