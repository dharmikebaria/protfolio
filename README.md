# Dharmike Baria — Portfolio

Personal portfolio website for **Dharmike Baria** — AI Developer, Data Scientist, Data Analyst & Python Developer.

Live site: https://www.dharmikbaria.online

A dependency-free static site featuring:

- A pinned 3D flip-card hero animation (the portrait flips and grows in place as you scroll, then docks into the About section)
- A floating, expandable pill navigation menu
- A scroll-driven "manifesto" text-highlight section
- Services, featured projects, testimonials, thoughts, and a contact form
- Fully responsive, with `prefers-reduced-motion` support

## Structure

| Path | What it is |
|---|---|
| `index.html` | Homepage (hand-edited) |
| `project.html` | Source of the project styles and project data. Not a public page; old `project.html?p=<slug>` links redirect to the new URLs |
| `build.js` | Generates `projects/`, `404.html`, `blog/_template.html` and `sitemap.xml` |
| `projects/<slug>/index.html` | Generated, crawlable case-study pages (committed) |
| `blog/_template.html` | Starter for future articles (noindex until published) |
| `vercel.json` | Domain and legacy-URL redirects, cache headers |

## Editing projects

Edit the project text or styles in `project.html`, then regenerate the pages and sitemap (Node 18+, no dependencies):

```bash
node build.js
```

Commit the regenerated files. Vercel needs no build command.

## Run locally

Pages use root-relative links, so serve the folder rather than opening files directly:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Deploy

Deployed on Vercel as a static site from the repo root. `vercel.json` redirects the old `vercel.app` domain and the apex domain to `www.dharmikbaria.online`.

## Contact

- GitHub: [dharmikebaria](https://github.com/dharmikebaria)
- LinkedIn: [dharmike-baria](https://www.linkedin.com/in/dharmike-baria/)
- Email: dharmikkbaria712@gmail.com
