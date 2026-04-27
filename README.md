# fed.thomasvn.dev

Two interactive views of the Federal Reserve architecture.

| Page | Approach | Best for |
|---|---|---|
| `index.html` | Intro copy + Excalidraw embed | A publishable explainer page with editable prose beside the live diagram |
| `panzoom.html` | HTML cards + panzoom | A more custom visual treatment and drill-in detail panels |

## Running locally

Both pages should be opened over HTTP, not by double-clicking the HTML files. This is required for `index.html` because it fetches `assets/TheFed.excalidraw`, and browsers block that request when the page is loaded as `file://`.

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then open:

- `http://127.0.0.1:8000/index.html`
- `http://127.0.0.1:8000/panzoom.html`

## Updating content

**index.html** — edit the intro copy in the left-hand section if you want to change the project explanation. The Excalidraw panel on the right loads the source diagram file below.

**assets/TheFed.excalidraw** — edit this in Excalidraw and save it back into the repo. `index.html` fetches and renders it automatically, so it must be served over HTTP from the repo root.

**panzoom.html** — edit this file directly if you still want to maintain the alternative card-based view.

## Deploying

Push to GitHub — Netlify serves the repo root as a static site with no build step.

The published diagram assets live in `assets/`, including `TheFed.excalidraw` and `TheFed.png`.
