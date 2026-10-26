# Memories Fond

The website for **Memories Fond**, heartwarming children's books by Andrew Abel.

Live at [memoriesfond.com](https://memoriesfond.com).

## About this site

A plain static site (HTML, CSS and a little JavaScript). There is no build step and nothing to install.

```
index.html      Homepage: book grid and scrolling cover ticker
about.html      About the author
contact.html    Contact page
videos.html     Book videos
books/          One page per book
css/style.css   Shared stylesheet
img/            Book covers and other images
```

## Preview locally

From the project folder, start a local web server:

```bash
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080) in your browser.

Press `Ctrl+C` in the terminal to stop the server.

## Publishing

The site is hosted on GitHub Pages. The `CNAME` file connects it to the `memoriesfond.com` domain.
