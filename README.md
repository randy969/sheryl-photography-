# Sheryl Ross — fine art photography

A single static page. No build step, no dependencies, no framework.

Seventeen photographs: close-up flowers, sunsets, and coastal landscapes.

## Deploy

Any static host serves this as-is. The publish directory is the repository root
and there is no build command.

- **Vercel** — import the repo, framework "Other", leave build empty
- **Netlify** — publish directory `.`, build command empty
- **Cloudflare Pages / GitHub Pages / S3** — same, serve the root

`vercel.json` sets clean URLs and a one-year immutable cache on `/photos`.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The entire site, styles and script inline |
| `photos/` | 17 photographs at two widths, 1400px and 2300px, plus the About portrait |
| `vercel.json` | Caching and clean URLs |

## Notes

Images are served with `srcset` so phones pull the 1400px file and larger
screens pull 2300px. The lightbox always loads the larger one.

The About portrait is a placeholder and says so on the image. Replace
`photos/portrait-grid.jpg` and `photos/portrait-full.jpg` with her photograph,
same names, no code change needed.
