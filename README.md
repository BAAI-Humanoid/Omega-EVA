# omega-EVA Project Page

Static project page for:

> omega-EVA: Envision, Verify, and Act with Latent Interactive World Models

## Local preview

Run a static server from this directory:

```bash
cd webpage
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

The site has no build step, package dependencies, analytics, backend, or external
CDN resources. Opening `index.html` directly also works, although a local HTTP
server more closely matches GitHub Pages.

## GitHub Pages

The contents of this directory can be published as the root of a GitHub Pages
repository:

1. Copy or push everything in `webpage/` to the repository's publishing branch.
2. In **Settings → Pages**, select **Deploy from a branch**.
3. Select the publishing branch and `/ (root)`.

All site resources use relative paths, so the page works both at a user site
(`owner.github.io`) and a project subpath (`owner.github.io/repository/`).
`.nojekyll` is included to keep deployment behavior purely static.

## Updating release links

The Paper button already points to the arXiv page. Code and Dataset are disabled
buttons in `index.html`. When those resources are released, replace each
`<button disabled>` with an `<a href="...">` using the same `button` classes and
remove the `Coming Soon` status text.

## Public assets

Images in `assets/` are copied from the omega-EVA paper and the project
presentation. The diagnostic decoder visualizations are analysis aids only:
omega-EVA performs consequence reasoning in latent feature space and does not
generate future videos during policy inference.
