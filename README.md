# CMPE 789 — Special Topics: Modern Cloud Computing

Course website for CMPE 789 at RIT. Plain static HTML — no build step, no
dependencies.

## Files

| File | What it is |
|---|---|
| `index.html` | Home page — course overview, key facts, learning outcomes, class structure |
| `syllabus.html` | Full syllabus |
| `schedule.html` | Week-by-week schedule and important dates |
| `template.html` | Starting point for a new page, with the reusable blocks documented inline |
| `assets/style.css` | The single stylesheet shared by every page |
| `Syllabus.md`, `Schedule.md` | Original markdown sources the HTML pages were written from |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is instead of running Jekyll |

## Editing

Open any `.html` file, edit the text inside `<main>`, save, and reload it in a
browser. Nothing to compile.

To preview the whole site locally as it will be served:

```
python3 -m http.server 8000
```

then visit <http://localhost:8000>.

## Adding a page

1. `cp template.html newpage.html`
2. Edit the `<title>`, `<meta name="description">`, `.page-title`, and content.
3. Add a link to it in the `<nav>` block of **every** page (`index.html`,
   `syllabus.html`, `schedule.html`, and `template.html`). The nav is copied
   into each file, so it has to be updated in each one. On its own page, give
   the link `class="is-current"`.

`template.html` contains ready-made markup for tables, callouts, the key/value
facts grid, linked cards, code blocks, and quotes — delete the blocks you don't
need.

## Publishing

Push to `main` and enable GitHub Pages for the repository (Settings → Pages →
Deploy from a branch → `main` / root). The site is then served at
<https://czfteaching.github.io/CMPE789-mcc/>.

## Notes on the content

The pages follow `Syllabus.md` and `Schedule.md` closely. A few obvious typos
were corrected in the HTML but left alone in the markdown sources:
"Leanring" → "Learning", "Attendence" → "Attendance", "an 6-page" → "a 6-page",
and "will focus on involve lectures" → "will focus on lectures".
