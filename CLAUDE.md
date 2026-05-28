# Memories Fond — CLAUDE.md

Static HTML/CSS website for Memories Fond, the children's book brand of author Andrew Abel.

## Project structure

```
index.html          — Homepage with book grid and scrolling cover ticker
about.html
contact.html
videos.html
books/              — One HTML file per book (11 books total)
css/style.css       — Single shared stylesheet
img/                — Cover images (avif, jpg, png) and button assets
```

No build step, no framework, no package.json. Pure HTML + CSS + minimal vanilla JS.

## Run locally

```bash
python3 -m http.server 8080 --directory /home/aabel/github/memoriesfond & sleep 0.5 && xdg-open http://localhost:8080
```

## Books

**Children's picture books** (secular):
- A Useless Book
- Seasons with Dad
- Big Bad Wolf's Birthday
- Finding Granny
- Adopt a Dinosaur
- I Like Earth
- Slice & Ice
- Walking with Dad

**Christian children's picture books**:
- Zac in a Santa Hat
- Zac is Back!
- The Farmer's Crop

## Conventions

- Nav and footer are duplicated in every HTML file — update all of them when adding pages or changing nav items.
- Book detail pages live in `books/` and use `../` relative paths for CSS, images, and nav links.
- Fonts: Mali (brand/headings) and Lato (body) loaded from Google Fonts.
- Icons: Font Awesome 6.5.1 via CDN.
- Images: prefer `.avif` for new covers; `.jpg`/`.png` are legacy.
- The homepage book grid is shuffled randomly on each load (JS at bottom of `index.html`).
- Brand color accent: `#e07b39` (orange).

## External data

- MySQL DB (`mybooks` on localhost:3306) holds book metadata — see memory for connection details.
- Live site: memoriesfond.com

## Original Wix site URLs (memoriesfond.com)

Most slugs match the book filename, except Big Bad Wolf's Birthday which uses `/bad-wolf-2` (other variants 404).

| Book | Slug |
|---|---|
| Zac in a Santa Hat | /zac-in-a-santa-hat |
| A Useless Book | /a-useless-book |
| Seasons with Dad | /seasons-with-dad |
| Big Bad Wolf's Birthday | /bad-wolf-2 |
| Zac is Back! | /zac-is-back |
| Finding Granny | /finding-granny |
| Adopt a Dinosaur | /adopt-a-dinosaur |
| I Like Earth | /i-like-earth |
| Slice & Ice | /slice-and-ice |
| Walking with Dad | /walking-with-dad |
| The Farmer's Crop | /the-farmers-crop |
