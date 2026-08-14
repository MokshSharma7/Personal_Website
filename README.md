# Moksh Sharma — Personal Website

A dark, animation-heavy personal portfolio built as two hand-coded static pages: a professional portfolio and a "beyond the resume" personal page. No framework, no build step — just HTML, CSS, and JavaScript, deployed as a static site.


## Pages

- **`index.html`** — the main portfolio. Hero, About, Leadership & Achievements, Selected Work (projects), Experience timeline, Tools I've worked with, and Contact.
- **`about-life.html`** — "Beyond the Resume," a personal page with an illustrated, interactive avatar, hobbies & interests, current goals, and a photo gallery.

## Features

- Custom cursor (dot + trailing ring) with hover states
- GSAP + ScrollTrigger-powered scroll reveals throughout
- Animated canvas gradient blobs in the hero
- A flip-card logo in the header that reveals a few personal details on hover
- Project rows with a cursor-following preview card linking out to the live GitHub repos
- A two-row, opposite-direction scrolling marquee of tools/tech
- A hand-coded SVG avatar on the Life page that blinks, tilts toward the cursor, and on hover "pops out" of the screen with a bigger grin and a speech bubble that cycles through random greetings
- A polaroid-style photo gallery with a click-to-expand lightbox
- Fully responsive down to mobile (custom cursor and some hover-only effects are disabled on touch devices)

## Tech stack

- Vanilla HTML / CSS / JavaScript (no build tools, no dependencies to install)
- [GSAP](https://gsap.com/) + ScrollTrigger, loaded via CDN, for all animation
- Plain CSS (custom properties for the color system, no CSS framework)

## File structure

```
.
├── index.html                 # main portfolio
├── about-life.html            # personal / "beyond the resume" page
├── photos/                    # gallery images used on about-life.html
│   └── photo-02.jpg ... photo-16.jpg
├── Moksh_Sharma_Resume.pdf    # downloadable resume, linked from index.html
├── favicon.svg                # primary favicon (modern browsers)
├── favicon.png                # favicon fallback
├── apple-touch-icon.png       # iOS home-screen icon
└── icon-512.png                # larger icon (PWA / social use)
```

## Running locally

No build step required — just open `index.html` in a browser. For local links between pages and images to resolve correctly, it's best to serve the folder rather than opening the file directly, e.g.:

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deployment

Deployed on [Vercel](https://vercel.com) as a static site — no framework preset or build command needed. Connect the GitHub repo to a new Vercel project and every push to the main branch redeploys automatically.

**Note:** the `photos/` folder must be uploaded as an actual nested folder in the repo (not flattened) — the site references images as `photos/photo-XX.jpg`. If uploading via GitHub's web UI, create the folder first (e.g. via "Add file → Create new file" and typing `photos/.gitkeep`), then upload into it from inside that folder view.

## Customizing

- **Colors / theme:** CSS custom properties at the top of each file's `<style>` block (`--bg`, `--accent`, `--accent2`, etc.)
- **Content:** all copy lives directly in the HTML — no CMS or data file.
- **Projects:** each project row in `index.html` has `data-url` and `data-repo` attributes that drive the hover preview card and click-through link.

## Author

**Moksh Sharma** — AI Automation Specialist, Data Analyst, Freelance Developer
[GitHub](https://github.com/MokshSharma7) · [LinkedIn](https://www.linkedin.com/in/moksh-sharma-8253b233b/) · mokshsharma02468@gmail.com
