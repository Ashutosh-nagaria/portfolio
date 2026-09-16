# anagaria.com

Personal portfolio of Ashutosh Nagaria. Static HTML, CSS and vanilla JS.
No framework, no build step, no dependencies. Edit any file and refresh.

## Run locally

    python3 -m http.server 8000
    # open http://localhost:8000

## File map

| Path                  | What it is                                    |
| --------------------- | --------------------------------------------- |
| `index.html`          | Home                                          |
| `about.html`          | About                                         |
| `work.html`           | Work index (all case studies)                 |
| `work/*.html`         | One file per case study                       |
| `writing.html`        | Writing index and posts                       |
| `cv.html`             | On-page CV plus the PDF download              |
| `contact.html`        | Contact                                       |
| `css/style.css`       | All styling. Design tokens live in `:root`    |
| `js/main.js`          | Mobile nav, active link, year, scroll reveal  |
| `assets/`             | Headshot and the CV PDF                       |

## Change the accent colour

Open `css/style.css`, edit `--accent` and `--accent-dark` in `:root`. Done site-wide.

## Add a case study

1. Copy `work/_template.html` to `work/your-slug.html`.
2. Fill in the title, the three blocks (Problem, Decision, Result) and the metrics.
3. Add a `.card` entry to `work.html`.
4. To feature it on the home page, add a card to the "Selected work" grid in `index.html`.

## Add a writing post

Posts live inline in `writing.html` by default. Clone an existing `<article class="post">`
block, newest first.

## Duplicated header and footer

Every page repeats the same `<header>` and `<footer>` markup so that the site works
with no build step. If you rename a nav item, search and replace across all `*.html`.

## Deploy

Any static host works. Simplest options:

- **GitHub Pages**: push to `main`, then Settings > Pages > Deploy from branch > `/` root. Add your domain under Custom domain.
- **Netlify / Vercel**: drag the folder in, or connect the repo. Set the publish directory to the repo root.

Add the domain's `CNAME` at your registrar once the host gives you the target.

## Notes

- Links to X, Medium and Substack are commented placeholders. Uncomment when ready.
- Case study copy is placeholder until the real write-ups are done.
