# october

A 32-seed bracket of 21st-century American political gaffes, scandals and October surprises. Lives at https://october.stuckhe.re.

One static page (`index.html`), with no build step and no backend.

- Picks autosave to `localStorage` in the visitor's browser.
- **Save & share** builds a link like `https://october.stuckhe.re/#b=<31 picks>&n=<name>`. Whoever opens it sees that bracket read-only and can start their own or copy those picks.
- Picks encoding: one character per matchup, `0` = top slot won, `1` = bottom, `-` = unpicked. The order is Round of 32 (16), Sweet 16 (8), Elite 8 (4), Final Four (2), then the Championship (1).

## Editing the field

The entries are the `FIELD` array near the top of the script in `index.html`: eight per region, in seed order. Changing the *order* invalidates existing share links, but editing text doesn't.

## Deploy

Netlify builds from `main`, publishing the repo root (see `netlify.toml`). DNS: `october` is a CNAME on Cloudflare (DNS only) pointing at the Netlify site.

Fonts (Lora, Martian Mono) are borrowed from stuckhe.re.
