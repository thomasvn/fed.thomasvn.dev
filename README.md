# fed.thomasvn.dev

An interactive Federal Reserve architecture diagram with intro copy and an embedded Excalidraw viewer.

## Running locally

Both pages should be opened over HTTP, not by double-clicking the HTML files. This is required for `index.html` because it fetches `assets/TheFed.excalidraw`, and browsers block that request when the page is loaded as `file://`.

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then open:

- `http://127.0.0.1:8000/index.html`

## Updating content

**index.html** — edit the intro copy in the left-hand section if you want to change the project explanation. The Excalidraw panel on the right loads the static diagram asset below.

**assets/TheFed.excalidraw** — edit this in Excalidraw and save it back into the repo. `index.html` fetches and renders it automatically, so it must be served over HTTP from the repo root.

## Deploying

Push to GitHub — Netlify serves the repo root as a static site with no build step.

The published diagram assets are stored in `assets/`, including `TheFed.excalidraw` and `TheFed.png`.
