# Cheryl Tang — portfolio

Static HTML/CSS site built from the desktop mockups in `mockups/`. No build
step: open `index.html` in a browser, or serve the folder
(`python3 -m http.server`) and deploy it as-is.

## Pages

| File | Mockup | Notes |
| --- | --- | --- |
| `index.html` | `mockups/home` | Intro + 3×2 grid of square project tiles |
| `more.html` | `mockups/more` | Second 3×2 grid |
| `about.html` | `mockups/about` | Bio, career list, client logos |
| `sandbox-vr.html` | `mockups/1` | Project page, linked from the first home tile |
| `nokia-earbuds.html` | `mockups/project 03` | Nokia Micro Earbuds Pro case study |

The sticky header and the footer are repeated in each file — there is no
templating, so a change to either needs to be made in all four.

## Images

The header logo, all twelve grid tiles, the Sandbox VR project shots, and the
About portrait are in place. Still missing: the six client logos and the four
software icons on the project hero. Those slots hold their shape and render
their `alt` text as a grey label so you can see what belongs where. Paths and
expected aspect ratios are listed in `images/README.md`.

## Still to fill in

- Tiles 4–6 on `index.html` and all six on `more.html` have no `href` yet.
  Search the HTML for `TODO`.
- Client logos and the project hero's tool icons.

## Fonts

Headings use Playfair Display (Google Fonts). Body copy targets Avenir Next
(installed on macOS) and falls back to Nunito Sans from Google Fonts
elsewhere — swap `--font-sans` in `css/style.css` if you licence the original.
