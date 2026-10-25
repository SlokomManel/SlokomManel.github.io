# slokommanel.github.io

Personal academic website of **Manel Slokom**, Lecturer & Researcher at Hotelschool The Hague. Built with Jekyll and hosted on GitHub Pages.

## Structure

- `_config.yml`: site title, tagline, and profile links (Scholar, LinkedIn, ORCID, GitHub, email). Edit this file to update contact info.
- `_data/*.yml`: all editable content, no HTML required:
  - `publications.yml`: publications grouped by theme
  - `talks.yml`: invited talks
  - `news.yml`: news and updates feed (newest first)
  - `experience.yml`: work experience
  - `education.yml`: degrees
  - `supervision.yml`: teaching and student supervision
  - `service.yml`: academic service (co-organizing, reviewing, volunteering)
  - `skills.yml`: technical skills and languages
- `index.html`, `publications.html`, `talks.html`, `teaching.html`, `news.html`: the five pages. You shouldn't need to touch these for routine updates.
- `assets/img/profile.jpg`: your photo.
- `assets/cv/MSLOKOM-CV.pdf`: your CV, linked from the "CV" button in the header.

## Updating content

To add a new publication, talk, or news item, just add an entry to the matching file in `_data/`, following the existing format. No HTML knowledge needed.

To replace your CV or photo, overwrite the file at the same path (keep the same filename, or update the path in `_config.yml` / `index.html`).

## Run locally

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000 in your browser. Jekyll will auto-reload as you edit files.

(Requires Ruby and Bundler. On macOS: `brew install ruby`, then `gem install bundler`.)

## Publish on GitHub Pages

1. Create a **public** repository on GitHub named exactly `SlokomManel.github.io`.
2. Add it as the remote and push:
   ```bash
   git remote add origin https://github.com/SlokomManel/SlokomManel.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. In the repo's **Settings → Pages**, make sure the source is set to "Deploy from a branch" → `main` / `/ (root)`. For a `username.github.io` repo this is usually already the default.
4. Your site will be live at **https://slokommanel.github.io** within a minute or two of pushing.

Any future `git push` to `main` will automatically redeploy the site.
