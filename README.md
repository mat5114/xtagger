# XTAGGER website

Website for XTAGGER, a professional laser tag system for operators (a brand of Emboscada Action Sports).

A single static page (`index.html`) with hash-routed pages:

| Route | Content |
| --- | --- |
| `#home` | Hero, audience, features, 3D tagger inspection, NFC upgrades, system, kit selection, revenue simulator |
| `#faqs` | FAQs: getting started, for operators, equipment care |
| `#play` | Arena training mini game (difficulty, player, equipment, first-person shooting with boss) |
| `#quote` | Quote and catalogue request form |

## Run locally

No build step. Serve the folder with any static server, for example:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Notes

- 3D tagger uses [three.js r128](https://cdnjs.com/libraries/three.js) from cdnjs. If WebGL or the script is unavailable, a static image is shown.
- Fonts load from Google Fonts (Barlow, Barlow Condensed, Share Tech Mono).
- The quote form is not connected to a backend yet: it validates fields and shows the contact emails.
- Animations respect `prefers-reduced-motion`.
- Images in `img/` come from the original x-tagger.com site; `img/logo.svg` is a vector trace of the logo.
