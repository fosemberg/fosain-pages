# fosain-pages

Static build of **Fosain** — a mobile-first 3D co-op rail-building game (Unrailed-like) on raw
WebGL2 with serverless peer-to-peer WebRTC multiplayer.

- Sources: https://github.com/fosemberg/fosain
- This repository only hosts the build output in [`docs/`](docs/) for GitHub Pages
  (Settings → Pages → *Deploy from a branch* → `main` / `/docs`).
- Live: https://fosemberg.github.io/fosain-pages/

## Updating the build

From a checkout of `fosain` next to this repository:

```bash
bun run publish:pages     # builds with VITE_BASE=/fosain-pages/ and copies into ../fosain-pages/docs
cd ../fosain-pages
git add docs && git commit -m "Publish build" && git push
```

`docs/.nojekyll` keeps GitHub from running Jekyll on the assets and `docs/404.html` is a copy of
`index.html` so deep links fall back to the app.
