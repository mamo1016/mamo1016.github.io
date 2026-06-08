# mamo1016.github.io

Personal portfolio website for Mamoru Ueda — robotics software engineer.
Live at **https://mamo1016.github.io/**

A single static page, plain HTML + CSS, no build step. To preview locally, just open
`index.html` in a browser (or run `python -m http.server` in this folder and visit
`http://localhost:8000`).

## Files
- `index.html` — the whole page (content + structure).
- `style.css` — all styling (dark theme, responsive).
- `favicon.svg` — site icon.
- `assets/` — CV PDF, and where the demo GIF goes (`assets/demo.gif`).

## Editing
Everything is plain text. Common edits:
- **Text/links:** edit `index.html`.
- **Colours/spacing:** edit the `:root` tokens at the top of `style.css`.
- **Add the demo clip:** save a short rviz2 recording as `assets/demo.gif`. It replaces the
  placeholder automatically.
- **Add a publication link:** in `index.html`, wrap the publication title in `<a href="DOI">`.

See `DEPLOY.md` for how to publish updates.
